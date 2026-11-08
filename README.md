# Kortex Apps Repository (Kortex App Hub Catalog) 🏪
### Official Software Catalog & Package Manifests for KortexOS

[![Catalog Version](https://img.shields.io/badge/catalog-v1.0.0-00f0ff.svg?style=for-the-badge)](apps.json)
[![License](https://img.shields.io/badge/license-MIT-00ff41.svg?style=for-the-badge)](LICENSE)
[![KortexOS Compatibility](https://img.shields.io/badge/KortexOS-v1.0.0%2B-ff003c.svg?style=for-the-badge)](https://github.com/ArtiomITPROGRAMING/KortexOS)

[ 🇬🇧 Read in English ](README.md) | [ 🇷🇺 Читать на русском ](README.ru.md) | [ 🌌 KortexOS Main Repo ](https://github.com/ArtiomITPROGRAMING/KortexOS)

Welcome to the official **Kortex Apps Repository**! This repository serves as the decentralized cloud back-end for **Kortex App Hub (`kortex-store`)** in KortexOS.

Every app listed here is automatically synchronized to KortexOS installations across the globe.

---

## 🚀 How It Works

1. **Client Synchronization**:
   When a user opens Kortex App Hub (`kortex-store` or `Super + P`), the client fetches the latest application catalog from:
   ```
   https://raw.githubusercontent.com/ArtiomITPROGRAMING/kortex-apps/main/apps.json
   ```
2. **Offline Fallback**:
   If internet is disconnected, KortexOS falls back to `/usr/share/kortex/apps.json` cached during the last online run.
3. **One-Click Installation**:
   Users can install software with 1 click using either:
   - **`native`**: Arch Linux / Pacman repositories.
   - **`flatpak`**: Sandboxed Flathub packages.
   - **`bundle`**: Custom shell installers or AppImages.

---

## 🤝 How to Submit Your Application

We welcome contributions from developers! To add your app or game to the Kortex App Hub:

### Step 1: Fork this Repository
Fork `https://github.com/ArtiomITPROGRAMING/kortex-apps` and clone your fork.

### Step 2: Edit `apps.json`
Add an entry to the `"apps"` array in [`apps.json`](apps.json):

```json
{
  "id": "my-awesome-app",
  "name": "My Awesome App",
  "category": "Development & IDE",
  "description": "Short description of what the app does.",
  "version": "1.0.0",
  "icon": "🚀",
  "type": "native",
  "package": "my-awesome-app",
  "install_cmd": "sudo pacman -S --noconfirm my-awesome-app",
  "launch_cmd": "my-awesome-app",
  "homepage": "https://example.com",
  "size": "25 MB"
}
```

### Supported Categories:
- `Audio & Music`
- `Browsers & Web`
- `Development & IDE`
- `Communication`
- `Media & Graphics`
- `Gaming & Emulation`
- `Cybersecurity & Net`
- `System Utilities`

### Step 3: Open a Pull Request
Submit a Pull Request with a title like `feat(app): add my-awesome-app`. Once approved and merged, your app will instantly appear in all KortexOS devices worldwide!

---

## 📄 License
This repository and its manifests are licensed under the [MIT License](LICENSE).
