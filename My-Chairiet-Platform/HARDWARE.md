# My Chairiet Platform — Hardware

## Wheelchair

| Item | Detail |
|---|---|
| Model | Pride Mobility Jazzy EVO |
| Nickname | My Chairiet |

## Compute Nodes

| Node | Board | RAM | Role |
|---|---|---|---|
| Headrest Pi | Raspberry Pi 5 | 16GB | Display driver, MQTT broker, rear camera |
| Basket Pi | Raspberry Pi 5 | 16GB | AI brain, sensor hub, HDMI console |

## Headrest Pi 5 Peripherals

| Component | Part | Interface |
|---|---|---|
| RGB LED Matrix | 64×32 RGB Matrix | GPIO |
| Matrix HAT | Adafruit RGB Matrix HAT | GPIO |
| Rear Camera | Pan/tilt camera | CSI / USB |

## Basket Pi 5 Peripherals

| Component | Part | Interface |
|---|---|---|
| AI Accelerator | Raspberry Pi AI HAT+ (Hailo-10H, 40 TOPS) | FFC PCIe |
| Console Display | 15.6" Waveshare HDMI | HDMI |
| Proximity Sensor | ToF (TBD) | I2C |

## Networking

| Link | Protocol |
|---|---|
| Headrest ↔ Basket | Ethernet (MQTT/Mosquitto) |
