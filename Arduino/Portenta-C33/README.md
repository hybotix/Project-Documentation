# Arduino / Portenta C33

## Overview

The Arduino Portenta C33 is the planned locomotion controller for SecureSMARS. It receives commands from the UNO-Q sensor hub over high-speed UART using a JSON protocol and drives the motors/locomotion subsystem.

## Role

Locomotion controller — SecureSMARS platform

## Status

~1,400 lines of existing C33 code. Integration with UNO-Q UART protocol in progress.

## Key Connections

- Serial UART — JSON protocol from UNO-Q (RX)
- Motor driver outputs — locomotion subsystem (TBD)

## Protocol

All messages are newline-terminated JSON objects over UART. See [CODING-STANDARDS.md](../CODING-STANDARDS.md) for the full protocol spec.

## Full Hardware Reference

See [HARDWARE.md](../HARDWARE.md) for pinouts and UART wiring.
