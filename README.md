# Guardian GCS

**Modern Windows Ground Control Station for robotic systems**

[![Release](https://img.shields.io/github/v/release/a-mohamadi/Guardian-GCS?include_prereleases&style=flat-square)](https://github.com/a-mohamadi/Guardian-GCS/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D4?style=flat-square&logo=windows&logoColor=white)](https://github.com/a-mohamadi/Guardian-GCS/releases)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![UI](https://img.shields.io/badge/UI-English%20%7C%20Persian-blue?style=flat-square)](https://github.com/a-mohamadi/Guardian-GCS)

Guardian GCS is a WPF-based desktop application designed for operators who require a reliable, single-window interface to monitor and control remote robots. It integrates live telemetry, interactive mapping, video, teleoperation, event logging, and system management into a coherent workspace, with native support for both English and Persian (including full right-to-left layout).

The application currently ships with a built-in simulator so the complete interface can be evaluated without physical hardware. The underlying connection interfaces are prepared for real TCP, UDP, or serial transports.

---

## Screenshots

| Dashboard | Interactive Map |
|-----------|-----------------|
| ![Dashboard](docs/screenshots/01-dashboard.png) | ![Map](docs/screenshots/02-map.png) |

| Live Camera | Telemetry & Charts |
|-------------|--------------------|
| ![Camera](docs/screenshots/03-camera.png) | ![Telemetry](docs/screenshots/04-telemetry.png) |

| Event Log | Settings & Themes |
|-----------|-------------------|
| ![Event Log](docs/screenshots/05-event-log.png) | ![Settings](docs/screenshots/06-settings.png) |

> Add high-quality screenshots to the `docs/screenshots/` directory using the filenames shown above.

---

## Key Capabilities

- **Live Dashboard** — Real-time display of battery, speed, signal strength, operating mode, depth, voltage, current, motor status and GPS
- **Interactive Map** — WebView2-powered map panel with robot position, home point, route planning and fullscreen mode
- **Live Camera** — Video feed with snapshot capture, recording controls and fullscreen support
- **Telemetry** — Recording, replay and expandable charts for detailed analysis
- **Event Log** — Searchable, severity-filtered log with export functionality
- **Teleoperation** — Configurable keyboard and gamepad bindings with Hold-to-Drive, Drive-Arm and deadzone safety controls
- **Security** — Application lock, password management and user session handling
- **Localization** — Full English and Persian (Farsi) support with automatic right-to-left layout
- **Themes** — Dark, Light, Glass and High Contrast themes
- **Demo Mode** — Complete simulator for immediate exploration without connected hardware

---

## Download

**Current release:** [v0.1.0 Beta](https://github.com/a-mohamadi/Guardian-GCS/releases/tag/v0.1.0-beta)

| Asset | Platform | Size |
|-------|----------|------|
| [Guardian_GCS.Setup.v0.1.0.beta.exe](https://github.com/a-mohamadi/Guardian-GCS/releases/download/v0.1.0-beta/Guardian_GCS.Setup.v0.1.0.beta.exe) | Windows 10 / 11 | ~11.2 MB |

Install and launch. No additional runtime installation is required on modern Windows systems.

---

## System Requirements

- Windows 10 or Windows 11 (64-bit)
- Approximately 50 MB free disk space
- .NET Framework 4.7.2 (included with current Windows installations)

---

## Technical Overview

| Area | Implementation |
|------|----------------|
| UI Framework | WPF (.NET Framework 4.7.2) |
| Language | C# |
| Map & Charts | Embedded HTML via Microsoft.Web.WebView2 |
| Data Serialization | System.Text.Json |
| Fonts | Inter (Latin), Vazirmatn (Persian) |
| Architecture | MVVM (Views / ViewModels / Services) |

---

## Getting Started from Source

1. Clone the repository
2. Open `Guardian-GCS.sln` in Visual Studio 2022 with the **.NET desktop development** workload
3. Restore NuGet packages (`Microsoft.Web.WebView2`, `System.Text.Json`)
4. (Optional) Run `scripts\INSTALL_APP_FONTS.bat` to install the recommended font families
5. Build and run

The application starts in Demo Mode by default. Connection parameters can be adjusted in `appsettings.json` or through the in-application User page.

---

## Configuration

Runtime configuration is managed through `appsettings.json` and covers:

- Robot host, port and connection mode
- Connection timeouts, heartbeat interval and auto-reconnect behaviour
- Keyboard and gamepad bindings together with safety options
- Language, region, theme, fonts, notifications and storage paths

---

## Project Status

This is an early public beta release.

- Demo Mode is fully operational and uses simulated data
- Real robot transport (TCP / UDP / serial) and portions of the server connectivity layer remain under active development
- Stability and feature completeness will improve in subsequent releases

Feedback is encouraged and directly influences the development roadmap.

---

## Feedback & Issues

Bug reports, unexpected behaviour and feature requests are welcome.  
Please open an [Issue](https://github.com/a-mohamadi/Guardian-GCS/issues) and include:

- Clear steps to reproduce
- Expected versus actual behaviour
- Windows version
- Whether Demo Mode or a real connection was used

---

## License

Guardian GCS is distributed under the [MIT License](LICENSE).

---

**Abolfazl Mohamadi**  
Engineer · Builder · Designer  
Robotics · Electronics · Software · R&D
