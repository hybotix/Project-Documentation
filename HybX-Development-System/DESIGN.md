# HybX Development System — Design

## Architecture Overview

The HybX Development System is a set of Python CLI tools installed as unversioned symlinks in a shared `bin/` directory. All commands share configuration via `hybx_config.py`.

## Library Management (`libs`)

The `libs` command replaced `addlib` as the authoritative library management subsystem. It is backed by a global registry at `~/.hybx/libraries.json`.

### Subcommands

| Subcommand | Description |
|---|---|
| `list` | List all registered libraries |
| `search` | Search registry by keyword |
| `install` | Install a library into the registry |
| `remove` | Remove a library (hard-blocked if in use) |
| `upgrade` | Upgrade a library to latest version |
| `show` | Show details for a specific library |
| `use` | Mark a library as used by the current project |
| `unuse` | Remove library association from current project |
| `update` | Update registry metadata |
| `sync` | Synchronize registry with installed state |
| `check` | Pre-flight check; called by `build` before compilation |

### Exit Codes

| Code | Meaning |
|---|---|
| 0 | Success |
| 1 | General error |
| 2 | Library not found |
| 3 | Removal blocked (library in use by project or dependency) |

## Build Pipeline

```
build
  └── libs check         ← pre-flight: validates all libraries present and compatible
  └── compile            ← Arduino CLI compilation
  └── logs               ← capture output
```

## Configuration

- `~/.hybx/config.json` — Board definitions (name, FQBN, port, etc.)
- `~/.hybx/libraries.json` — Global library registry

## File Versioning Convention

All scripts use `filename-vX.Y.Z.py` suffix format. Active commands are unversioned symlinks pointing to the current version.

## Sensor Code Convention

All new sensor code must be fully present:
- `#include` statement
- Instance declaration
- Function implementation
- `Bridge.provide()` active

Only `begin()` calls are commented out for sensors not yet physically connected.
