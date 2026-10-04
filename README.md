<div align="center">

# Persist — Releases

**Binary distribution and over-the-air update channel for Persist.**

[![Latest release](https://img.shields.io/github/v/release/stim-blip/persist-releases?style=flat-square&color=7C3AED&label=latest)](https://github.com/stim-blip/persist-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/stim-blip/persist-releases/total?style=flat-square&color=06B6D4&label=downloads)](https://github.com/stim-blip/persist-releases/releases)
![Platforms](https://img.shields.io/badge/platforms-Android%208.0%2B%20%7C%20Debian%2FUbuntu-4F46E5?style=flat-square)

</div>

This repository contains **release binaries only**. The application source is private.

Persist is a cross-platform habit and routine tracker with offline-first storage, cloud sync, and a built-in analytics
engine. Each release publishes two artifacts:

| Artifact | Platform | File name |
| :--- | :--- | :--- |
| Android app | Android 8.0 (API 26) and newer | `Persist-vX.Y.Z.apk` |
| Linux desktop app | Debian / Ubuntu, amd64 | `persist_X.Y.Z-1_amd64.deb` |

> Early releases (v1.1 – v1.3.1) shipped the Android file as `app-release.apk`; see each release's assets.

## Install

**Easiest:** open the [latest release](https://github.com/stim-blip/persist-releases/releases/latest) and download
the file for your platform.

**Android**

1. Download the `.apk` on your phone (or `adb install Persist-vX.Y.Z.apk` from a computer).
2. Allow installation from your browser or file manager when Android asks.
3. Open Persist.

**Linux (Debian / Ubuntu)**

```bash
sudo dpkg -i persist_X.Y.Z-1_amd64.deb
```

Replace `X.Y.Z` with the version you downloaded.

## Updates

Both apps check a small version manifest and offer an update when a newer version is published. The download comes
straight from this repository's releases.

```
Persist app ──► version manifest ──► newer than installed?
                                           │ yes
                                           ▼
                                  update dialog ──► GitHub Releases (this repo)
```

You can always update manually by installing a newer file over the existing app.

## Release history

| Version | Highlights |
| :--- | :--- |
| **v1.3.3.4** | **Insight engine** on the Analysis screen (Android and desktop): consistency score, plain-language findings, failure risk, day-of-week patterns, task dependencies, goal forecasts, and a backtested prediction model. New liquid-glass desktop UI. |
| v1.3.3.3 | One-tap task lock, slimmer task blocks, more transparent glass, refined dark mode. |
| v1.3.3.2 | Compact task cards and dark theme refinements. |
| v1.3.3.1 | Task lock, endless stack tasks with custom units, show-in-calendar option, category delete protection, vault-key QR pairing, Google Calendar / Keep / Tasks integration, home-screen widgets. |
| v1.3.3 | Dark-theme text fixes, v3 signing scheme, install compatibility for Android 13 Go. |
| v1.3.2 | Release-signed APK (fixes "App not installed"), license text correction. |
| v1.3.1 | Fix for persistent-failure detection (only evaluates fully elapsed days). |
| v1.3 | Multi-stack animations, heatmap pulse, volume bar animation, swipe gestures. |
| v1.2 | Analysis screen, heatmap, volume chart, streak tracking. |
| v1.1 | Initial release with core task management. |

Full notes for every version are on the [Releases page](https://github.com/stim-blip/persist-releases/releases).

## License

Persist is proprietary software. © 2026 Nizar / Xahara. All rights reserved. Reverse engineering and redistribution without permission are not allowed.

<div align="center"><sub>Built by <a href="https://github.com/stim-blip">Xahara</a> · Indonesia</sub></div>
