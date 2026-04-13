# Master TODO — Hybrid RobotiX

Cross-project task tracker. Each project also maintains its own `TODO.md`.

---

## 🔴 HybX Development System

- [ ] Update `DESIGN.md` to reflect replacement of `addlib` with `libs` command
- [ ] Commit and push all outstanding changes
- [ ] Verify `libs check` pre-flight integration in `build` command
- [ ] Document all `libs` subcommands: list, search, install, remove, upgrade, show, use, unuse, update, sync, check

## 🔴 SecureSMARS

- [ ] Complete mux2 sensor wiring validation (all 8 channels)
- [ ] Finalize SCD30 Python-side calibration with flag file persistence
- [ ] Document Portenta C33 JSON UART protocol
- [ ] Integrate PMSA003I (replaced SGP41) into full sensor stack
- [ ] Confirm AS7343 v1.1.0 integration (replaced VEML7700)

## 🟡 My Chairiet Platform

- [ ] Finalize Headrest Pi 5 software stack (MQTT broker, RGB matrix, rear camera)
- [ ] Finalize Basket Pi 5 software stack (AI HAT+, sensors, HDMI console)
- [ ] Define HSP (Hybrid RobotiX Standardized Sensor Platform) MQTT topic namespace
- [ ] Implement Kalman filtering for sensor fusion layer
- [ ] Document blockchain-verified environmental data pipeline design

## 🟡 Ham System

- [ ] Complete `init-v0.0.1.py` 15-step sequence testing on "hammer" Pi 5
- [ ] Validate OpenSSL 3.4.x and Python 3.14.3 builds from source
- [ ] Test SDR++ and FlRig from-source builds
- [ ] Document CI-V pyserial integration (no hamlib)

## 🟢 MicropythonOS / ESP32-S3

- [ ] Receive and inspect Waveshare ESP32-S3-Touch-LCD-2 (B0DTTL56ZR)
- [ ] Flash MicropythonOS and verify boot
- [ ] Explore MicropythonOS app model / Android-inspired architecture

## 🟡 UNO-Q

- [ ] Audit all Arduino apps post-repo split
- [ ] Confirm `hybx_config.py` shared config compatibility across all apps
- [ ] Document pan/tilt camera PCA9685 wiring and QWIIC setup
- [ ] Finalize Edge Impulse YOLOv11-nano dataset plan (~15–25 classes)

## 🟢 The Accessibility Files

- [ ] Define current scope and active deliverables
- [ ] Document Dark Reader compatibility contributions to Delta Robotics Protoboard
- [ ] Identify next accessibility feature targets

---

## Legend

| Symbol | Meaning |
|---|---|
| 🔴 | High priority / actively blocked |
| 🟡 | In progress |
| 🟢 | Lower priority / exploratory |

---

*Last updated: 2026-04-13*
