# Arduino / Nano Matter

## Overview

The Arduino Nano Matter is built around the Silicon Labs MGM240S multiprotocol wireless SoC (Cortex-M33). It is the first Arduino board with native Matter protocol support, alongside Thread, Zigbee, and Bluetooth LE — making it an ideal node for smart home, IoT mesh, and distributed sensor networks.

## Key Specs

| Feature | Detail |
|---|---|
| MCU | Silicon Labs MGM240S (Cortex-M33 @ 78MHz) |
| RAM | 256KB |
| Flash | 1536KB |
| Connectivity | Matter, Thread, Zigbee, Bluetooth 5.3 LE (all native, multiprotocol) |
| FQBN | `SiliconLabs:silabs:nano_matter` |

## Current Role

Not yet acquired. Planned purchase.

## Potential Use Cases

- Matter/Thread sensor node for My Chairiet Platform (HSP mesh networking)
- Distributed environmental sensor nodes (HSP standardized stack)
- Smart home / IoT integration bridge

## Notes

- Native Matter support is unique in the Arduino ecosystem — no external co-processor needed
- Thread provides IPv6 mesh networking; nodes can relay data without WiFi infrastructure
- Multiprotocol radio: can run BLE alongside Thread simultaneously
- 3.3V logic — not 5V tolerant
- Requires Silicon Labs board package: `SiliconLabs:silabs`
