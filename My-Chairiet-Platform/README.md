# My Chairiet Platform

## Overview

My Chairiet ("My Chairiet" — a portmanteau of CHAIR and CHARIOT) is a distributed computing platform built into a Pride Mobility Jazzy EVO power wheelchair. It transforms the wheelchair into an AI-capable, sensor-rich mobile computing node with real-time environmental monitoring, camera systems, and an HDMI console.

## Status

🟡 Architecture defined — hardware procurement and software stack in progress

## Architecture

Two-node Raspberry Pi 5 16GB system communicating over Ethernet via Mosquitto MQTT.

### Headrest Pi 5 — Display Driver & Broker

| Role | Component |
|---|---|
| MQTT broker | Mosquitto |
| Display driver | 64×32 RGB LED matrix |
| Matrix HAT | Adafruit RGB Matrix HAT |
| Camera | Rear pan/tilt |

### Basket Pi 5 — AI Brain & Sensor Hub

| Role | Component |
|---|---|
| AI acceleration | Raspberry Pi AI HAT+ |
| Console display | 15.6" Waveshare HDMI |
| Sensor hub | Environmental + ToF proximity sensors |

## Hybrid RobotiX Standardized Sensor Platform (HSP)

Identical sensor stacks deployed across My Chairiet, scout robot, and portable units. MQTT topics are namespaced per device. Redundant sensors deployed at minimum ×2.

## Data Products

GPS-tagged, blockchain-verified environmental data is a planned commercial data product. Target stack: Go or Elixir for the data pipeline layer.
