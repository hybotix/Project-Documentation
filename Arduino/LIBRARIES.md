# Arduino Libraries — Hybrid RobotiX

Shared library registry for all Arduino projects. Authoritative versions are tracked in `~/.hybx/libraries.json` and managed via the `libs` command.

## Sensor Libraries

| Library | Version | Sensor | Project |
|---|---|---|---|
| Adafruit SCD30 | latest | SCD30 (CO₂) | SecureSMARS |
| Adafruit SHT4x | latest | SHT45 (temp/humidity) | SecureSMARS |
| Adafruit PM25AQI | latest | PMSA003I (particulate) | SecureSMARS |
| Adafruit BME680 | latest | BME688 (env) | SecureSMARS |
| ScioSense ENS160 | latest | ENS161 (air quality) | SecureSMARS |
| Adafruit AS7343 | 1.1.0 | AS7343 (14-ch spectral) | SecureSMARS |
| Adafruit APDS9960 | latest | APDS9999 (proximity/color) | SecureSMARS |
| Adafruit BNO055 | latest | BNO055 (9-DOF IMU) | SecureSMARS |

## I2C / Mux Libraries

| Library | Version | Purpose |
|---|---|---|
| Adafruit TCA9548A | latest | I2C multiplexer |
| Adafruit PWMServoDriver | latest | PCA9685 pan/tilt servos |

## Communication Libraries

| Library | Version | Purpose |
|---|---|---|
| ArduinoJson | latest | JSON serialization for UART protocol (C33) |

## Notes

- Library removal via `libs remove` is **hard-blocked** (exit code 3) if any project or dependent library uses the target
- All library installs go through `libs install` — never install manually outside the registry
- Pin specific versions in `~/.hybx/libraries.json` when stability is critical (e.g., AS7343 pinned to 1.1.0)
