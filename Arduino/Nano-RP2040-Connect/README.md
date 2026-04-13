# Arduino / Nano RP2040 Connect

## Overview

The Arduino Nano RP2040 Connect is built around the Raspberry Pi RP2040 (dual Cortex-M0+) with an onboard u-blox NINA-W102 module providing WiFi and Bluetooth, plus an onboard IMU and microphone.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | Raspberry Pi RP2040 (dual Cortex-M0+ @ 133MHz) |
| RAM | 264KB SRAM |
| Flash | 16MB |
| Connectivity | WiFi 802.11 b/g/n, Bluetooth 4.2 (via u-blox NINA-W102) |
| FQBN | `arduino:mbed_nano:nanorp2040connect` |

## Onboard Sensors

| Sensor | Part | Measures |
|---|---|---|
| IMU | LSM6DSOX | 6-DOF accel/gyro |
| Microphone | MP34DT05 | PDM audio |

## Current Role

Not yet assigned to a specific project.

## Notes

- RP2040 is programmable via Arduino framework (mbed core) or MicroPython
- WiFi/BLE handled by NINA co-processor via SPI; use `WiFiNINA` library
- 3.3V logic — not 5V tolerant
- Dual-core: both M0+ cores available via Arduino mbed threading
