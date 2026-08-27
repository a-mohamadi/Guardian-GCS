# Guardian GCS

A modern Windows Ground Control Station for monitoring, controlling, and managing robotic systems.

Guardian GCS is a WPF desktop application that provides operators with a single-window interface for live robot monitoring and control. It includes a dashboard, interactive map, camera feed, telemetry, event log, teleoperation, security controls, and full bilingual support (English and Persian).

> **Current status:** The connection layer ships with a built-in simulator (`FakeRobotConnection` / `FakeServerConnection`). The full UI can be used without physical hardware. Interfaces for real TCP/UDP/serial transport are already in place.

---

## Screenshots

<!-- Replace the placeholders below with actual screenshots of the application -->

| Dashboard | Map | Camera |
|-----------|-----|--------|
| ![Dashboard](docs/screenshots/dashboard.png) | ![Map](docs/screenshots/map.png) | ![Camera](docs/screenshots/camera.png) |

| Telemetry & Charts | Settings & Themes | Event Log |
|--------------------|-------------------|-----------|
| ![Telemetry](docs/screenshots/telemetry.png) | ![Settings](docs/screenshots/settings.png) | ![Event Log](docs/screenshots/event-log.png) |

> Place your screenshots in a `docs/screenshots/` folder and update the image paths above.

---

## Features

- **Live dashboard** — Battery, speed, signal, mode, depth, voltage, current, motor and GPS status
- **Map** — WebView2-based map with robot position, home point, route planning and fullscreen mode
- **Camera** — Live video panel with snapshot, recording and fullscreen support
- **Telemetry** — Recording, replay and expandable charts
- **Event log** — Searchable, filterable by severity, with export
- **Teleoperation** — Configurable keyboard and gamepad bindings with Hold-to-Drive, Drive-Arm and deadzone controls
- **Security** — Application lock, password management and user sessions
- **Settings** — Language, region, theme (Dark / Light / Glass / High Contrast), fonts, sounds, storage and backup/restore
- **Localization** — English and Persian (Farsi) with right-to-left layout support
- **Demo mode** — Fully functional simulator for exploring the application without a connected robot

---

## Download

**Latest release:** [v0.1.0 Beta](https://github.com/a-mohamadi/Guardian-GCS/releases/tag/v0.1.0-beta)

| File | Description | Size |
|------|-------------|------|
| [Guardian_GCS.Setup.v0.1.0.beta.exe](https://github.com/a-mohamadi/Guardian-GCS/releases/download/v0.1.0-beta/Guardian_GCS.Setup.v0.1.0.beta.exe) | Windows Installer | ~11.2 MB |

---

## System Requirements

- Windows 10 or Windows 11
- .NET Framework 4.7.2 (included with modern Windows)

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| UI Framework | WPF (.NET Framework 4.7.2) |
| Language | C# |
| Map / Charts | Embedded HTML via Microsoft.Web.WebView2 |
| Serialization | System.Text.Json |
| Fonts | Inter (Latin), Vazirmatn (Persian) |

---

## Getting Started (Source)

1. Clone the repository
2. Open `Guardian-GCS.sln` in Visual Studio 2022 (with the .NET desktop development workload)
3. Restore NuGet packages (`Microsoft.Web.WebView2`, `System.Text.Json`)
4. Optionally run `scripts\INSTALL_APP_FONTS.bat` to install the recommended fonts
5. Build and run

The application starts in Demo Mode by default. Connection settings can be adjusted in `appsettings.json` or through the in-app User page.

---

## Configuration

Runtime settings are stored in `appsettings.json` and cover:

- Robot host, port and connection mode
- Connection timeouts, heartbeat and auto-reconnect
- Keyboard / gamepad bindings and safety options
- Language, theme, fonts, notifications and storage paths

---

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

When reporting issues, please include:
- Steps to reproduce
- Expected vs actual behavior
- Windows version
- Whether you are using Demo Mode or a real connection

---

## License

This project is licensed under the [MIT License](LICENSE).
