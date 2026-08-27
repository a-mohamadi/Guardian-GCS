<div align="center">

<img src="docs/media/icon.png" width="88" alt="Guardian GCS">

# Guardian GCS

**A modern Windows Ground Control Station for monitoring, controlling, and managing robotic systems.**

[![Release](https://img.shields.io/github/v/release/a-mohamadi/Guardian-GCS?include_prereleases&label=release)](https://github.com/a-mohamadi/Guardian-GCS/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/a-mohamadi/Guardian-GCS/total)](https://github.com/a-mohamadi/Guardian-GCS/releases/latest)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078D4?logo=windows&logoColor=white)](#requirements)
[![Localization](https://img.shields.io/badge/UI-English%20%7C%20Persian%20(RTL)-informational)](#localization)

<img src="docs/media/hero.png" alt="Guardian GCS — main window" width="860">

</div>

<br>

## Overview

Guardian GCS is a WPF desktop application for Windows that consolidates live telemetry, mapping, camera monitoring, teleoperation, event logging, and system configuration into a single operator console. It is designed for teams that need a reliable, professional interface to supervise and command a remote robotic platform.

The application ships with complete **English and Persian** localization, including native right-to-left layout support, making it suitable for international and regional deployments alike.

> **Beta notice.** This release includes a fully functional built-in simulator, allowing every panel of the interface to be evaluated without physical hardware. The architecture already defines the interfaces required for a live TCP/UDP/serial robot connection; this transport layer is under active development and not yet available. See [Project Status](#project-status) for details.

<br>

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Requirements](#requirements)
- [Project Status](#project-status)
- [Localization](#localization)
- [Security Notice](#security-notice)
- [Source Code Availability](#source-code-availability)
- [Support and Issue Reporting](#support-and-issue-reporting)
- [License](#license)

<br>

## Features

| Category | Capabilities |
|---|---|
| **Dashboard** | Battery, speed, signal, mode, depth, voltage, current, motor and GPS status, emergency stop, safety reset |
| **Mapping** | WebView2-based map with robot, home, and route tracking; dedicated fullscreen view |
| **Camera** | Live video feed with snapshot, recording, and fullscreen support |
| **Telemetry** | Live recording, replay, and expandable data charts |
| **Event Log** | Full-text search, severity filtering, export, and notification prioritization |
| **Teleoperation** | Configurable keyboard and gamepad bindings, drive-arm mode, hold-to-drive, deadzone and turn-scale tuning, gimbal control |
| **Safety** | Hold-to-drive interlock, automatic stop on disconnect, motion lock while configuration panels are open |
| **Security** | Optional application lock, password management, and session control |
| **Customization** | Dark, Light, Glass, and High Contrast themes; adjustable fonts and sounds; configurable storage paths and backup/restore |
| **Localization** | English (`en-US`) and Persian (`fa-IR`) included; additional language packs auto-discovered at runtime |
| **Simulation** | Built-in `FakeRobotConnection` / `FakeServerConnection` for full offline evaluation |

<br>

## Screenshots

<table>
<tr>
<td width="50%"><img src="docs/media/dashboard.png" alt="Dashboard"></td>
<td width="50%"><img src="docs/media/map.png" alt="Map panel"></td>
</tr>
<tr>
<td align="center"><sub>Live dashboard</sub></td>
<td align="center"><sub>Map panel</sub></td>
</tr>
<tr>
<td width="50%"><img src="docs/media/camera.png" alt="Camera panel"></td>
<td width="50%"><img src="docs/media/telemetry.png" alt="Telemetry charts"></td>
</tr>
<tr>
<td align="center"><sub>Camera panel</sub></td>
<td align="center"><sub>Telemetry charts</sub></td>
</tr>
<tr>
<td width="50%"><img src="docs/media/event-log.png" alt="Event log"></td>
<td width="50%"><img src="docs/media/settings.png" alt="Settings and themes"></td>
</tr>
<tr>
<td align="center"><sub>Event log</sub></td>
<td align="center"><sub>Settings and themes</sub></td>
</tr>
</table>

<br>

## Installation

| Release | File | Platform | Size |
|---|---|---|---|
| [v0.1.0-beta](https://github.com/a-mohamadi/Guardian-GCS/releases/tag/v0.1.0-beta) *(latest)* | [Guardian_GCS.Setup.v0.1.0.beta.exe](https://github.com/a-mohamadi/Guardian-GCS/releases/download/v0.1.0-beta/Guardian_GCS.Setup.v0.1.0.beta.exe) | Windows 10 / 11 (x64) | ~11.2 MB |

All current and past builds are available on the [Releases](https://github.com/a-mohamadi/Guardian-GCS/releases) page.

**Setup steps**

1. Download the installer from the table above.
2. Run the installer and follow the setup wizard.
3. Launch Guardian GCS. The application starts in **Demo Mode**, connected to the built-in simulator, so every panel is immediately usable.
4. Open **Settings → Language & Region** to switch between English and Persian at any time.

<br>

## Requirements

- Windows 10 or Windows 11 (x64)
- .NET Framework 4.7.2 (included in current Windows updates)
- A display driver with WebView2 support (installed automatically if not already present)

<br>

## Project Status

Guardian GCS v0.1.0 is an early public beta focused on the operator interface and offline evaluation experience.

| Available now | Planned |
|---|---|
| Full interface in Demo Mode | Live robot transport (TCP / UDP / serial) |
| Local installation and bilingual UI | Production-grade server connectivity |
| Themes, teleoperation bindings, event log, telemetry replay | Code-signed installer |

<br>

## Localization

Guardian GCS supports full UI localization out of the box:

- `en-US` — English
- `fa-IR` — Persian, including native right-to-left layout

Additional languages can be added by dropping a `Languages/<culture>.json` file into the application directory; new packs are automatically detected at startup.

<br>

## Security Notice

The current installer is not yet code-signed. As a result, Windows SmartScreen may display an "unrecognized app" warning on first run. If the source is trusted, select **More info → Run anyway** to proceed. Code signing is planned for an upcoming release.

<br>

## Source Code Availability

This repository currently distributes pre-built Windows installers and supporting documentation. The application source is not public while the project is under active development. Bug reports and feature requests are welcomed and tracked through [Issues](https://github.com/a-mohamadi/Guardian-GCS/issues).

<br>

## Support and Issue Reporting

To report a problem, please open an [issue](https://github.com/a-mohamadi/Guardian-GCS/issues) and include:

- Steps to reproduce the issue
- Expected behavior vs. observed behavior
- Windows version
- Whether Demo Mode or a live connection was in use

<br>

## License

This project is distributed under the [MIT License](LICENSE).

<br>

<div align="center">
<sub>© 2026 Guardian GCS. All rights reserved.</sub>
</div>
