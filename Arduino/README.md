# Arduino — Hybrid RobotiX

Central reference for all Arduino hardware, libraries, and development standards across Hybrid RobotiX projects.

## Board Directories

| Directory | Board | MCU | Role |
|---|---|---|---|
| [UNO-Q/](./UNO-Q/README.md) | Arduino UNO R4 WiFi | Renesas RA4M1 | Sensor hub — SecureSMARS |
| [Portenta-C33/](./Portenta-C33/README.md) | Arduino Portenta C33 | Renesas RA6M5 | Locomotion controller — SecureSMARS |
| [Portenta-H7/](./Portenta-H7/README.md) | Arduino Portenta H7 | STM32H747XI (M7+M4) | Unassigned |
| [Portenta-X8/](./Portenta-X8/README.md) | Arduino Portenta X8 | i.MX 8M Mini + STM32H747XI | Unassigned — Linux+MCU hybrid |
| [Giga-R1/](./Giga-R1/README.md) | Arduino Giga R1 WiFi + Display Shield | STM32H747XI (M7+M4) | Unassigned — HMI candidate |
| [Nano-33-BLE-Sense-Rev2/](./Nano-33-BLE-Sense-Rev2/README.md) | Arduino Nano 33 BLE Sense Rev2 | Nordic nRF52840 | Unassigned — Edge ML candidate |
| [Nano-RP2040-Connect/](./Nano-RP2040-Connect/README.md) | Arduino Nano RP2040 Connect | RP2040 (dual M0+) | Unassigned |
| [Nano-ESP32/](./Nano-ESP32/README.md) | Arduino Nano ESP32 | ESP32-S3 | Unassigned |
| [Nano-Matter/](./Nano-Matter/README.md) | Arduino Nano Matter | Silicon Labs MGM240S (M33) | Planned — Matter/Thread sensor node |
| [Nano-R4/](./Nano-R4/README.md) | Arduino Nano R4 | TBD | Planned — pending board confirmation |

## Reference Documents

| Document | Description |
|---|---|
| [LIBRARIES.md](./LIBRARIES.md) | Shared library registry and version pins |
| [CODING-STANDARDS.md](./CODING-STANDARDS.md) | Coding conventions for all Arduino apps |
| [HARDWARE.md](./HARDWARE.md) | Board pinouts, wiring standards, and I2C map |

## Toolchain

All Arduino apps are managed by the HybX Development System. See [HybX-Development-System/](../HybX-Development-System/README.md) for CLI toolchain docs.

- **Build:** `build` command (delegates pre-flight to `libs check`)
- **Library management:** `libs` command (backed by `~/.hybx/libraries.json`)
- **Board definitions:** `~/.hybx/config.json`
- **Project scaffolding:** `project` command
