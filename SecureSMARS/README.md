# SecureSMARS

## Overview

SecureSMARS is a sensor-rich autonomous robot platform built on the Arduino UNO-Q (UNO R4 WiFi). It features a full environmental and spectral sensor stack via dual TCA9548A I2C multiplexers, with planned locomotion control via a Portenta C33 communicating over high-speed UART with a JSON protocol.

## Status

🟡 Active development — sensor stack integration phase

## Key Architecture

- **Sensor hub:** Arduino UNO-Q (UNO R4 WiFi)
- **Locomotion controller:** Portenta C33 (~1400 lines of existing code)
- **Communication:** High-speed UART, JSON protocol (UNO-Q ↔ C33)
- **I2C mux:** TCA9548A ×2 (mux1 + mux2)
- **Camera:** Front-mounted pan/tilt via PCA9685 I2C servo controller (QWIIC)
- **AI inference:** Edge Impulse YOLOv11-nano / YOLOv5 Pico on Linux AARCH64

## mux2 Sensor Layout

| Channel | Sensor | Notes |
|---|---|---|
| ch0 | SCD30 | CO₂; calibration on Python side, flag file via $HOME bind-mount |
| ch1 | SHT45 | Temp/humidity; feeds ENS161 + SCD30 compensation |
| ch2 | PMSA003I | Particulate matter (replaced SGP41) |
| ch3 | BME688 | Temp/humidity/pressure/gas |
| ch4 | ENS161 | Air quality index; fed by SHT45 compensation |
| ch5 | AS7343 | 14-channel spectral sensor (replaced VEML7700) |
| ch6 | APDS9999 | Proximity/color/gesture |
| ch7 | BNO055 | 9-DOF IMU |
