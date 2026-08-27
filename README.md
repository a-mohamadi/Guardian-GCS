<p align="center">
  <img src="docs/media/icon.png" alt="Guardian GCS" width="96">
</p>

<h1 align="center">Guardian GCS</h1>

<p align="center">
  Windows ground control station for operating and monitoring a remote robot.
</p>

<p align="center">
  <a href="https://github.com/a-mohamadi/Guardian-GCS/releases/latest"><img src="https://img.shields.io/github/v/release/a-mohamadi/Guardian-GCS?include_prereleases" alt="Release"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="License"></a>
  <img src="https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-0078D4?logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/UI-English%20%7C%20Persian-informational" alt="Languages">
</p>

<p align="center">
  <img src="docs/media/hero.png" alt="Guardian GCS main window" width="920">
</p>

Guardian GCS is a WPF desktop application that puts live telemetry, map, camera, teleoperation, event logging, and settings in a single operator window. English and Persian (including right-to-left layout) are supported out of the box.

This public beta ships with a built-in simulator so the full interface can be used without a physical robot. Interfaces for a real TCP / UDP / serial transport are in place; that transport is not implemented yet.

## Download

| Asset | Platform | Size |
| --- | --- | --- |
| [Guardian_GCS.Setup.v0.1.0.beta.exe](https://github.com/a-mohamadi/Guardian-GCS/releases/download/v0.1.0-beta/Guardian_GCS.Setup.v0.1.0.beta.exe) | Windows 10 / 11 | ~11.2 MB |

All builds are published on the [Releases](https://github.com/a-mohamadi/Guardian-GCS/releases) page.

## Screenshots

<p align="center">
  <img src="docs/media/dashboard.png" alt="Live dashboard" width="48%">
  <img src="docs/media/map.png" alt="Map panel" width="48%">
</p>
<p align="center">
  <img src="docs/media/camera.png" alt="Camera panel" width="48%">
  <img src="docs/media/telemetry.png" alt="Telemetry charts" width="48%">
</p>
<p align="center">
  <img src="docs/media/event-log.png" alt="Event log" width="48%">
  <img src="docs/media/settings.png" alt="Settings and themes" width="48%">
</p>

## Features

- **Dashboard** — battery, speed, signal, mode, depth, voltage, current, motor and GPS status, emergency stop, and safety reset
- **Map** — WebView2 map with robot / home / route state, plus a fullscreen view
- **Camera** — live feed with snapshot, recording, and fullscreen
- **Telemetry** — record, replay, and expandable charts
- **Event log** — search, severity filter, export, and notification priority
- **Teleoperation** — keyboard and gamepad bindings, drive-arm, hold-to-drive, deadzone, turn scale, and gimbal keys
- **Safety** — hold-to-drive, stop-on-disconnect, motion lock while panels are open
- **Security** — optional app lock, password change, and session management
- **Settings** — language and region, theme, fonts, sounds, storage paths, backup and restore
- **Localization** — `en-US` and `fa-IR`, with additional `Languages/<culture>.json` packs discovered at runtime
- **Themes** — Dark, Light, Glass, High Contrast
- **Demo mode** — `FakeRobotConnection` / `FakeServerConnection` so the UI runs without hardware

## Requirements

- Windows 10 or Windows 11
- .NET Framework 4.7.2 (included with current Windows)

## Status

v0.1.0 is an early public beta.

| Ready | Not ready |
| --- | --- |
| Full UI in Demo Mode | Real robot transport (TCP / UDP / serial) |
| Local install and bilingual UI | Production-grade server connectivity |

## Reporting issues

Open an [issue](https://github.com/a-mohamadi/Guardian-GCS/issues) and include:

- Steps to reproduce
- Expected vs actual behavior
- Windows version
- Demo Mode or a real connection

## License

[MIT](LICENSE)
