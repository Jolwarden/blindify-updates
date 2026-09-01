# Blindify Updates

[![Build custom ffmpeg](https://github.com/jolwarden/blindify-updates/actions/workflows/build-ffmpeg.yml/badge.svg)](https://github.com/jolwarden/blindify-updates/actions/workflows/build-ffmpeg.yml)
[![Release Blindify](https://github.com/jolwarden/blindify-updates/actions/workflows/release.yml/badge.svg)](https://github.com/jolwarden/blindify-updates/actions/workflows/release.yml)

Ce dépôt **public** sert uniquement à héberger :

- Les **binaires ffmpeg/ffprobe** nécessaires à l’application Blindify (compilés via CI/CD).
- Les **mises à jour de Blindify** (installeurs signés + manifest `latest.json`).

Il est utilisé par le système d’auto-update de l’application [Blindify](https://github.com/jolwarden/blindify) (Tauri v2 + plugin updater).

---

## 📂 Structure

```txt
.
├── latest/                 # Dernière release publiée
│   ├── latest.json          # Manifest de mise à jour (lu par l'application)
│   ├── Blindify_x.y.z.msi   # Installeur Windows signé
│   ├── Blindify_x.y.z.dmg   # Installeur macOS signé
│   └── Blindify_x.y.z.AppImage  # Installeur Linux signé
│
├── archives/               # Historique complet des releases
│   ├── v0.1.0/
│   │   ├── latest.json
│   │   └── ...
│   ├── v0.2.0/
│   │   ├── latest.json
│   │   └── ...
│   └── ...
│
└── resources/              # Binaires ffmpeg/ffprobe compilés via GitHub Actions
    ├── linux/
    │   ├── ffmpeg
    │   └── ffprobe
    ├── macos/
    │   ├── ffmpeg
    │   └── ffprobe
    └── windows/
        ├── ffmpeg.exe
        └── ffprobe.exe
