# My Chairiet Platform — Design

## Node Architecture

```
┌─────────────────────────┐        ┌──────────────────────────┐
│    Headrest Pi 5        │        │      Basket Pi 5         │
│                         │        │                          │
│  Mosquitto MQTT Broker  │◄──────►│  MQTT Client             │
│  64×32 RGB LED Matrix   │  Eth   │  AI HAT+ (Hailo-10H)     │
│  Adafruit RGB Matrix HAT│        │  Environmental Sensors   │
│  Rear Pan/Tilt Camera   │        │  ToF Proximity           │
│                         │        │  15.6" Waveshare HDMI    │
└─────────────────────────┘        └──────────────────────────┘
```

## MQTT Topic Namespace (HSP)

Proposed schema: `hybx/{device}/{sensor}/{measurement}`

Examples:
- `hybx/chairiet/scd30/co2`
- `hybx/chairiet/sht45/temperature`
- `hybx/scout/bno055/orientation`

## Sensor Fusion

- Weighted averaging across redundant sensors (minimum ×2 per measurement)
- Kalman filtering for noise reduction
- Cascading calibration: SHT45 feeds compensation inputs to ENS161 and SCD30

## Environmental Data Pipeline

```
Sensors → MQTT → Aggregator → GPS tag → Blockchain verify → Data product API
```
Target languages: Go or Elixir for the aggregation/pipeline layer.
