# SecureSMARS — Hardware

## Compute

| Component | Part | Notes |
|---|---|---|
| Sensor Hub | Arduino UNO R4 WiFi (UNO-Q) | Main controller |
| Locomotion Controller | Portenta C33 | ~1400 lines existing code |

## I2C Mux — mux2 (TCA9548A)

| Channel | Sensor | Library | Notes |
|---|---|---|---|
| ch0 | SCD30 | Adafruit SCD30 | CO₂; Python-side calibration |
| ch1 | SHT45 | Adafruit SHT4x | Temp/humidity; compensation source |
| ch2 | PMSA003I | Adafruit PM25AQI | Particulate matter |
| ch3 | BME688 | Adafruit BME680 | Env sensor |
| ch4 | ENS161 | ScioSense ENS160 | Air quality index |
| ch5 | AS7343 | Adafruit AS7343 v1.1.0 | 14-channel spectral |
| ch6 | APDS9999 | Adafruit APDS9960 | Proximity/color/gesture |
| ch7 | BNO055 | Adafruit BNO055 | 9-DOF IMU |

## Camera / Servo

| Component | Part | Interface |
|---|---|---|
| Pan/Tilt Servo Controller | PCA9685 | I2C / QWIIC |
| Front Camera | TBD | USB |

## Communication

| Link | Protocol | Notes |
|---|---|---|
| UNO-Q ↔ Portenta C33 | UART (JSON) | High-speed |
| UNO-Q ↔ Host | USB / WiFi | |
