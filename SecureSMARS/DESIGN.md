# SecureSMARS — Design

## System Architecture

```
┌──────────────────────────────────┐
│         Arduino UNO-Q            │
│    (UNO R4 WiFi — Sensor Hub)    │
│                                  │
│  mux1 (TCA9548A)                 │
│  mux2 (TCA9548A) — ch0–ch7      │
│  PCA9685 (pan/tilt servos, QWIIC)│
│         │                        │
│         │ UART (JSON)            │
│         ▼                        │
│      Portenta C33                │
│   (Locomotion Controller)        │
└──────────────────────────────────┘
         │
         │ USB / WiFi
         ▼
    Edge Impulse
   YOLOv11-nano inference
   (Linux AARCH64 .eim)
```

## Bridge Function Naming

All Bridge function names use full part numbers (e.g., `bridge_scd30_`, `bridge_sht45_`, `bridge_bme688_`).

## Sensor Compensation Chain

```
SHT45 (temp/humidity)
  └── feeds compensation → ENS161 (air quality)
  └── feeds compensation → SCD30 (CO₂)
```

## SCD30 Calibration

- Calibration logic lives on the Python side
- Flag file persisted via `$HOME` bind-mount in Docker container
- Ensures calibration survives container restarts

## AI Inference

- Framework: Edge Impulse Linux Python SDK
- Model format: `.eim` (ImpulseRunner)
- Target architecture: Linux AARCH64
- Model candidates: YOLOv11-nano, YOLOv5 Pico
- Dataset: ~15–25 classes (people + dropped workshop items at category level)
