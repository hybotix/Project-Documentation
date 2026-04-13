# HybX Development System

## Overview

The HybX Development System is the core CLI toolchain powering Hybrid RobotiX development workflows. It provides a unified set of bin commands for managing Arduino projects, libraries, boards, builds, and deployment — all callable from both the command line and the `hybx-dev` VSCode extension.

## Repository

https://github.com/hybotix/HybX-Development-System.git

## Status

🟢 Active development

## Bin Commands

| Command | Description |
|---|---|
| `board` | Board definitions via `~/.hybx/config.json` |
| `build` | Compile Arduino projects; delegates library authority to `libs check` pre-flight |
| `clean` | Remove build artifacts |
| `libs` | Library management (replaces `addlib`) |
| `list` | List projects/boards/libraries |
| `logs` | View build and runtime logs |
| `project` | Scaffold new Arduino app |
| `restart` | Restart connected board |
| `setup` | Install environment (nano syntax highlighting, etc.) |
| `start` | Start monitoring/runtime (v0.0.10) |
| `stop` | Stop monitoring/runtime |

## Key Files

- `hybx_config.py` — Shared config used across all bin commands
- `~/.hybx/config.json` — Board definitions
- `~/.hybx/libraries.json` — Global library registry (backing `libs` command)

## VSCode Extension

`hybx-dev` (reached v0.1.7) wraps all bin commands over SSH. Recommended SSH client: Termius (Mac/Windows/Linux/iOS/Android).

## Notes

- `newrepo.bash` is never modified
- All new sensor code must be fully present (include, instance, function, Bridge.provide active); only `begin()` calls are commented out for unconnected sensors
- Library removal is hard-blocked (exit code 3) if any project or dependent library uses the target library
