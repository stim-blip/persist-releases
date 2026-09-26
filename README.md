<div align="center">

# 🚀 Persist — Official Releases

**Binary distribution & OTA update channel for [Persist](https://github.com/stim-blip/Persist)**

[![Latest Release](https://img.shields.io/github/v/release/stim-blip/persist-releases?style=for-the-badge&color=6C63FF&label=Latest)](https://github.com/stim-blip/persist-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/stim-blip/persist-releases/total?style=for-the-badge&color=00C9A7&label=Downloads)](https://github.com/stim-blip/persist-releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Linux-FF6B6B?style=for-the-badge)](https://github.com/stim-blip/persist-releases/releases/latest)

---

*Repositori ini adalah saluran distribusi resmi untuk binary Persist.*
*Semua APK dan DEB dipublikasikan di sini untuk pembaruan OTA (Over-The-Air).*

</div>

---

## 📦 Apa Itu Repositori Ini?

Repositori ini **bukan** berisi source code — melainkan tempat distribusi resmi binary **Persist**, sebuah aplikasi habit tracker & task management cross-platform bergaya glassmorphism.

| Artifact | Platform | Format |
|----------|----------|--------|
| `app-release.apk` | Android 8.0+ | APK |
| `persist_x.x.x-1_amd64.deb` | Linux (Debian/Ubuntu) | DEB |

> Source code tersedia di repo utama: **[stim-blip/Persist](https://github.com/stim-blip/Persist)** (private)

---

## 🔄 Sistem OTA Update

Persist memiliki sistem pembaruan otomatis bawaan yang bekerja di kedua platform:

```
┌─────────────┐     fetch manifest     ┌──────────────────┐
│  Persist App │ ──────────────────────► │  Version Manifest │
│  (Android /  │                        │  (GitHub Gist)    │
│   Desktop)   │ ◄────────────────────── │                   │
└──────┬───────┘    compare version     └──────────────────┘
       │
       │ version_code > local?
       │
       ▼
┌──────────────┐     download binary    ┌──────────────────┐
│ Update Dialog │ ──────────────────────► │  GitHub Releases  │
│  (Auto-shown) │                        │  (this repo)      │
└──────────────┘                        └──────────────────┘
```

### Bagaimana Cara Kerjanya

1. **Manifest Check** — Aplikasi secara berkala mengambil JSON manifest yang berisi `version_code`, `version_name`, dan `download_url`
2. **Version Compare** — Membandingkan `version_code` (integer) dengan versi yang terinstall
3. **Auto-Prompt** — Jika versi baru tersedia, dialog update muncul otomatis
4. **Direct Download** — Binary diunduh langsung dari GitHub Releases di repositori ini

---

## 📥 Instalasi Manual

### Android
```bash
# Download APK terbaru
curl -LO https://github.com/stim-blip/persist-releases/releases/latest/download/app-release.apk

# Install via ADB
adb install app-release.apk
```

### Linux (Debian/Ubuntu)
```bash
# Download DEB terbaru (ganti versi sesuai kebutuhan)
curl -LO https://github.com/stim-blip/persist-releases/releases/latest/download/persist_1.3.1-1_amd64.deb

# Install
sudo dpkg -i persist_*.deb
```

---

## 📋 Riwayat Rilis

| Versi | Tag | Highlights |
|-------|-----|------------|
| **v1.3.1** | `v1.3.1` | 🔧 Hotfix logika Kegagalan Persisten — hanya evaluasi 2 hari penuh yang lampau |
| **v1.3** | `v1.3` | ✨ Animasi multi-stack, heatmap pulse, volume bar animation, swipe gestures |
| **v1.2** | `v1.2` | 📊 Analisis lengkap, heatmap, volume chart, streak tracking |
| **v1.1** | `v1.1` | 🎯 Rilis awal dengan fitur inti task management |

> Lihat semua rilis: [**Releases →**](https://github.com/stim-blip/persist-releases/releases)

---

## 🏗️ Struktur Proyek

```
persist-releases/
├── README.md              ← Anda di sini
└── releases/              ← Binary didistribusikan via GitHub Releases
    ├── v1.3.1/
    │   ├── app-release.apk
    │   └── persist_1.3.1-1_amd64.deb
    ├── v1.3/
    │   ├── app-release.apk
    │   └── persist_1.3-1_amd64.deb
    └── ...
```

---

## 🔗 Links

| Resource | Link |
|----------|------|
| 📱 Source Code | [stim-blip/Persist](https://github.com/stim-blip/Persist) |
| 📦 Latest Release | [Download](https://github.com/stim-blip/persist-releases/releases/latest) |
| 👤 Developer | [@stim-blip](https://github.com/stim-blip) |

---

<div align="center">

**Built with ❤️ by [Xahara](https://github.com/stim-blip)**

*PT. Delusional · Indonesia*

</div>
