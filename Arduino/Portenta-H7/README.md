# Arduino / Portenta H7

## Overview

The Arduino Portenta H7 is a high-performance industrial-grade board based on the STM32H747XI (dual Cortex-M7 + M4). It is designed for demanding edge computing, computer vision, and ML inference workloads. Supports MicroPython, JavaScript (via Luat), and OpenMV in addition to Arduino.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | STM32H747XI (Cortex-M7 @ 480MHz + Cortex-M4 @ 240MHz) |
| RAM | 1MB SRAM + 8MB SDRAM |
| Flash | 2MB internal + 16MB QSPI |
| Connectivity | WiFi 802.11 b/g/n, Bluetooth 5.1 (via Murata LBAD0ZZ1WE) |
| Video out | MIPI DSI, 8-bit parallel |
| Camera in | MIPI CSI (via Vision Shield or carrier) |
| FQBN | `arduino:mbed_portenta:envie_m7` (M7) / `arduino:mbed_portenta:envie_m4` (M4) |

## Current Role

Not yet assigned to a specific project.

## Notes

- M7 core is primary; M4 core runs a separate sketch via RPC
- Shares the same STM32H747XI as the Giga R1 — many libraries are compatible
- High-Density connector (80-pin ×2) for carrier boards and shields
- Portenta Vision Shield adds camera (320×240 HM01B0) and dual PDM mics
- Well-suited for OpenMV machine vision workloads
- 3.3V logic
