# Arduino / Nano 33 BLE Sense Rev2

## Overview

The Arduino Nano 33 BLE Sense Rev2 is a compact, sensor-rich board built around the Nordic nRF52840 (Cortex-M4). It features an extensive onboard sensor suite and is a first-class Edge Impulse target for on-device ML inference.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | Nordic nRF52840 (Cortex-M4 @ 64MHz) |
| RAM | 256KB |
| Flash | 1MB |
| Connectivity | Bluetooth 5.0 BLE |
| FQBN | `arduino:mbed_nano:nano33ble` |

## Onboard Sensors

| Sensor | Part | Measures |
|---|---|---|
| IMU | BMI270 + BMM150 | 6-DOF accel/gyro + magnetometer |
| Temp / Humidity | HS3003 | Temperature, humidity |
| Pressure | LPS22HB | Barometric pressure |
| Microphone | MP34DT06JTR | PDM audio |
| Proximity / Color / Gesture | APDS9960 | Proximity, RGB, gesture |

## Current Role

Not yet assigned to a specific project.

## Notes

- Rev2 uses BMI270 IMU (Rev1 used LSM9DS1 — libraries differ)
- Excellent Edge Impulse target: audio, motion, and sensor fusion models
- All onboard sensors accessible via Adafruit or Arduino libraries
- 3.3V logic — not 5V tolerant
