# Ham System / Ham-SDR-Radio

## Overview

The Ham System is an amateur radio and SDR (Software Defined Radio) infrastructure built on a Raspberry Pi 5 named "hammer" running Raspberry Pi OS Trixie. It provides a fully from-source software stack for radio operations, SDR signal processing, and rig control — with no dependency on hamlib.

## Repository

https://github.com/hybotix/Ham-SDR-Radio.git

## Operator

- **Callsign:** N7PKT
- **Current license:** Technician
- **Studying for:** General class (via hamstudy.org adaptive flashcards + Kindle books)
- **Long-term goal:** Extra class; claim callsign KI6EM

## Status

🟡 Init sequence under development and testing

## Key Design Decisions

- **No hamlib ever** — direct CI-V via pyserial
- All software built from source into `/usr/local`
- Python 3.14.3 in venv at `~/Virtual/Ham-SDR-Radio`
- `license_advisor-v0.0.1.py` warns but never blocks operations

## Active Operations

- 10M FT8 DX at 20W into Hamstick antennas
- All-time DX record: 7,414 miles (Australia)
- Contacts: Australia, South Korea, Indonesia, Japan, South America, Europe
