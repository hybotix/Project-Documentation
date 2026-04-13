# SecureSMARS — Changelog

## [Unreleased]

- VEML7700 replaced by AS7343 (Adafruit AS7343 v1.1.0, 14-channel spectral)
- SGP41 replaced by PMSA003I (went out of stock)
- APDS9999 API corrected
- SCD30 calibration moved to Python side with flag file via $HOME bind-mount
- Bridge function names updated to use full part numbers

## Earlier History

- Initial mux2 channel layout defined
- Portenta C33 selected as locomotion controller
- High-speed UART JSON protocol designed for UNO-Q ↔ C33 communication
- PCA9685 pan/tilt camera added via QWIIC
