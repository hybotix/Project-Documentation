# Arduino — Hybrid RobotiX

Central reference for all Arduino hardware, libraries, and development standards across Hybrid RobotiX projects.

## Board Directories

| Directory | Board | Role |
|---|---|---|
| [UNO-Q/](./UNO-Q/README.md) | Arduino UNO R4 WiFi | Sensor hub — SecureSMARS |
| [Portenta-C33/](./Portenta-C33/README.md) | Arduino Portenta C33 | Locomotion controller — SecureSMARS |

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
