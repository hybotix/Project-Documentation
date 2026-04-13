# HybX Development System — Hardware

The HybX Development System is software-only tooling. Hardware context is relevant only in terms of the target boards it manages.

## Supported Board Targets

Board definitions are stored in `~/.hybx/config.json`.

| Board | Notes |
|---|---|
| Arduino UNO-Q (UNO R4 WiFi) | Primary target for SecureSMARS sensor stack |
| Portenta C33 | Planned locomotion controller for SecureSMARS |

## Development Machine

| Component | Detail |
|---|---|
| Primary workstation | MacBook Air 8GB/250GB (current constraint) |
| Planned workstation | MS-A2 (AMD Ryzen 9 9955HX, 16-core Zen 5) |
| Planned GPU | RTX A2000E ADA 16GB |
| SSH client | Termius |
| Editor | VSCode + hybx-dev extension |

## Target Deployment Environment

- Debian-based Linux systems only
- Builds from source into `/usr/local`
- Repos cloned into `~/Repos/GitHub/hybotix/`
