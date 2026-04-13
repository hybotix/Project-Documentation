# Arduino / Portenta X8

## Overview

The Arduino Portenta X8 is a hybrid Linux + real-time microcontroller board. It combines an NXP i.MX 8M Mini (quad Cortex-A53 running Linux) with an STM32H747XI (Cortex-M7 + M4 running Arduino/RTOS). The two processors communicate via a hardware RPC bridge (RPC over shared memory / virtio).

## Key Specs

| Feature | Detail |
|---|---|
| Linux SoC | NXP i.MX 8M Mini (quad Cortex-A53 @ 1.8GHz) |
| M7/M4 MCU | STM32H747XI (Cortex-M7 @ 480MHz + Cortex-M4 @ 240MHz) |
| RAM | 2GB LPDDR4 (Linux) + 1MB SRAM + 8MB SDRAM (MCU) |
| Storage | 16GB eMMC |
| Connectivity | WiFi 802.11 b/g/n/ac, Bluetooth 5.1, Gigabit Ethernet |
| OS | Yocto Linux (Arduino-maintained) |
| FQBN | `arduino:mbed_portenta:envie_m7` (M7 side) |

## Architecture

```
┌─────────────────────────┐        ┌──────────────────────────┐
│   NXP i.MX 8M Mini      │        │   STM32H747XI            │
│   (Linux — A53 ×4)      │◄──────►│   (Arduino — M7 + M4)    │
│   Python, Docker,        │  RPC   │   Real-time I/O          │
│   ML inference, etc.     │        │   Sensor reading         │
└─────────────────────────┘        └──────────────────────────┘
```

## Current Role

Not yet assigned to a specific project.

## Notes

- Linux side runs a full Yocto stack; Python, Docker, and standard Linux tooling available
- M7/M4 handle real-time sensor and I/O tasks; results passed to Linux via RPC
- Extremely powerful platform for edge AI: run PyTorch/TFLite on A53 + real-time sensor fusion on M7
- High-Density connector compatible with Portenta H7 shields and carriers
- Strong candidate for future My Chairiet or scout robot AI brain roles
