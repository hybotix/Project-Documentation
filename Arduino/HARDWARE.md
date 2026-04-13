# Arduino Hardware Reference — Hybrid RobotiX

Board pinouts, I2C maps, and wiring standards for all Arduino hardware in the Hybrid RobotiX ecosystem.

## Boards

### Arduino UNO R4 WiFi (UNO-Q)

| Feature | Detail |
|---|---|
| MCU | Renesas RA4M1 |
| Connectivity | WiFi (ESP32-S3 co-processor), USB |
| I2C | SDA=A4, SCL=A5 (Wire) |
| UART | TX=1, RX=0 (Serial); also Serial1, Serial2 |
| FQBN | `arduino:renesas_uno:unor4wifi` |

### Arduino Portenta C33

| Feature | Detail |
|---|---|
| MCU | Renesas RA6M5 |
| Connectivity | WiFi, Bluetooth, USB-C |
| I2C | SDA=SDA, SCL=SCL |
| UART | Multiple hardware UARTs |
| Role | Locomotion controller — high-speed UART to UNO-Q |

## I2C Map — SecureSMARS mux2 (TCA9548A)

| Channel | Sensor | I2C Address | Notes |
|---|---|---|---|
| ch0 | SCD30 | 0x61 | CO₂; calibration on Python side |
| ch1 | SHT45 | 0x44 | Temp/humidity; compensation source |
| ch2 | PMSA003I | 0x12 | Particulate matter |
| ch3 | BME688 | 0x76 or 0x77 | Env sensor |
| ch4 | ENS161 | 0x52 or 0x53 | Air quality |
| ch5 | AS7343 | 0x39 | 14-channel spectral |
| ch6 | APDS9999 | 0x39* | Proximity/color/gesture |
| ch7 | BNO055 | 0x28 or 0x29 | 9-DOF IMU |

*APDS9999 and AS7343 share address 0x39 — isolated on separate mux channels.

## I2C Devices (Direct / QWIIC)

| Device | Address | Interface | Notes |
|---|---|---|---|
| TCA9548A mux2 | 0x70 | I2C | 8-channel mux for sensor stack |
| PCA9685 | 0x40 | I2C / QWIIC | Pan/tilt servo controller |

## UART Wiring — UNO-Q ↔ Portenta C33

| Signal | UNO-Q Pin | C33 Pin | Notes |
|---|---|---|---|
| TX | Serial1 TX | RX | UNO-Q → C33 |
| RX | Serial1 RX | TX | C33 → UNO-Q |
| GND | GND | GND | Common ground required |

## Wiring Standards

- All I2C devices use 3.3V logic unless explicitly noted
- QWIIC connectors use standard SparkFun/Adafruit QWIIC pinout (3.3V, GND, SDA, SCL)
- All sensor `begin()` calls use default I2C address unless address pin is set
