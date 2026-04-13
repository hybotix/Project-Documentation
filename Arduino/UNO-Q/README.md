# Arduino / UNO-Q (UNO R4 WiFi)

## Overview

The Arduino UNO R4 WiFi (UNO-Q) is the primary sensor hub board for SecureSMARS. It manages the full mux2 sensor stack, pan/tilt camera servos, and communicates with the Portenta C33 locomotion controller via high-speed UART.

## Role

Sensor hub — SecureSMARS platform

## Key Connections

- mux2 (TCA9548A) — 8-channel I2C sensor stack (ch0–ch7)
- PCA9685 — pan/tilt servo controller (QWIIC)
- Serial1 UART — JSON protocol to Portenta C33

## Apps

Arduino apps for UNO-Q live in the [UNO-Q repo](../../UNO-Q/README.md).

## Full Hardware Reference

See [HARDWARE.md](../HARDWARE.md) for pinouts, I2C addresses, and wiring.
