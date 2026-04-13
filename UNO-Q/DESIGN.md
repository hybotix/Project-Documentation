# UNO-Q — Design

## Repo Scope

UNO-Q contains **Arduino applications only**. All bin commands, scripts, and tooling live in the HybX Development System repo.

## App Structure

Each Arduino app:
- Uses `hybx_config.py` for shared configuration
- Follows sensor code conventions (include, instance, function, Bridge.provide active; only `begin()` commented for unconnected sensors)
- Bridge function names use full part numbers

## AI Inference Pipeline

```
Camera (front pan/tilt)
  └── PCA9685 servo controller (I2C/QWIIC)
  └── Frame capture
        └── Edge Impulse ImpulseRunner (.eim)
              └── YOLOv11-nano / YOLOv5 Pico
                    └── Detections: people, dropped items
```
