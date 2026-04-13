# Arduino / Giga R1 WiFi (+ Display Shield)

## Overview

The Arduino Giga R1 WiFi is a high-performance dual-core board based on the STM32H747XI (Cortex-M7 + Cortex-M4). Paired with the Arduino GIGA Display Shield, it provides a 800×480 capacitive touch display, making it suitable for HMI, dashboards, and data visualization applications.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | STM32H747XI (Cortex-M7 @ 480MHz + Cortex-M4 @ 240MHz) |
| RAM | 1MB SRAM + 8MB SDRAM (via shield) |
| Flash | 2MB internal + 16MB QSPI |
| Connectivity | WiFi (Murata), Bluetooth 5.1, USB-A host |
| I2C | Multiple (Wire, Wire1, Wire2) |
| UART | Multiple hardware UARTs |
| FQBN | `arduino:mbed_giga:giga` |

## Display Shield

| Feature | Detail |
|---|---|
| Display | 800×480 capacitive touch LCD |
| Connector | DSI |
| Touch | Capacitive multi-touch |
| Camera connector | Yes (MIPI CSI) |
| Library | `Arduino_H7_Video`, `Arduino_GigaDisplay_GFX` |

## Current Role

Not yet assigned to a specific project.

## Notes

- M7 core runs the main sketch; M4 core can run a separate sketch via RPC
- Use `RPC` library for inter-core communication
- Display requires `Arduino_H7_Video` library and `ArduinoGraphics`
