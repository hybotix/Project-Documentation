# Arduino / Nano ESP32

## Overview

The Arduino Nano ESP32 is built around the u-blox NORA-W106 module (ESP32-S3 core), making it the first Arduino Nano with native ESP32 support. It supports both Arduino and MicroPython firmware.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | ESP32-S3 (dual Xtensa LX7 @ 240MHz, via u-blox NORA-W106) |
| RAM | 512KB SRAM + 2MB PSRAM |
| Flash | 16MB |
| Connectivity | WiFi 802.11 b/g/n, Bluetooth 5.0 BLE |
| FQBN | `arduino:esp32:nano_nora` |

## Current Role

Not yet assigned to a specific project.

## Notes

- Supports Arduino ESP32 core and MicroPython
- 3.3V logic — not 5V tolerant
- Has USB-C with native USB (CDC, HID, MSC via ESP32-S3 USB OTG)
- Pin numbering differs from classic Nano — refer to official pinout diagram
- ESP32-S3 includes vector instructions for ML workloads (TensorFlow Lite Micro)
