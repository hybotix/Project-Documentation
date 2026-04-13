# HybX Development System — Changelog

## [Unreleased]

- Replaced `addlib` command with `libs` command backed by `~/.hybx/libraries.json` global registry
- Added GUI-callable code paths to `libs`
- Added meaningful exit codes including exit code 3 (blocked removal)
- `build` now delegates library authority to `libs check` as pre-flight
- Deleted `addlib` command

## [v0.0.10] — start command

- Bumped `start` from v0.0.9 to v0.0.10

## [v0.1.7] — hybx-dev VSCode extension

- Latest released version of the VSCode extension wrapping all bin commands over SSH

## Earlier History

- Split UNO-Q repo into UNO-Q (Arduino apps) and HybX-Development-System (bin commands, scripts, docs)
- Added `board` command with `~/.hybx/config.json` board definitions
- Added `project` command for scaffolding new Arduino apps
- Added `setup` command installing nano syntax highlighting
