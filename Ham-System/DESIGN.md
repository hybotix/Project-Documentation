# Ham System — Design

## Init Sequence (`init-v0.0.1.py`)

15-step initialization sequence:

1. License validation (FCC/ISED/Ofcom via callook.info)
2. System dependency installation
3. OpenSSL 3.4.x from source
4. Python 3.14.3 from source
5. venv creation at `~/Virtual/Ham-SDR-Radio`
6. SDR++ from source
7. FlRig from source
8. Symlink creation
9. Config scaffolding
10–15. (Additional setup steps)

## License Advisor

`license_advisor-v0.0.1.py` validates the operator's callsign against FCC/ISED/Ofcom databases. It **warns** when operating outside licensed privileges but **never blocks** operations — operator responsibility.

## Rig Control

- **No hamlib** — ever
- Direct CI-V control via pyserial
- FlRig used for rig abstraction where needed

## Software Stack

| Component | Source | Install Location |
|---|---|---|
| OpenSSL | from source | `/usr/local` |
| Python 3.14.3 | from source | `/usr/local` |
| SDR++ | from source | `/usr/local` |
| FlRig | from source | `/usr/local` |
| venv | pip | `~/Virtual/Ham-SDR-Radio` |
