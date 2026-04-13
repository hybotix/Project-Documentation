# UNO-Q

## Overview

UNO-Q is the Arduino application suite for Hybrid RobotiX projects, running on the Arduino UNO R4 WiFi. The repo was split from the original combined repo: UNO-Q contains Arduino apps only; the HybX Development System contains all bin commands and tooling.

## Status

🟡 Active development — sensor platform integration ongoing

## Repository

Part of the Hybrid RobotiX GitHub organization.

## Key Components

- Arduino apps for SecureSMARS sensor platform
- `hybx_config.py` shared config (from HybX Development System)
- Edge Impulse AI inference pipeline (planned)

## AI Inference (Planned)

- Framework: Edge Impulse Linux Python SDK
- Model: YOLOv11-nano or YOLOv5 Pico
- Format: `.eim` (ImpulseRunner)
- Target: Linux AARCH64
- Dataset: ~15–25 classes (people + dropped workshop items)
