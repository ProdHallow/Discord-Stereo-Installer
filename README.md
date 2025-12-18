# 🎧 Stereo Installer

A one-click install tool for Discord Stereo Modules. Automatically downloads and applies the latest voice module patches to restore lossless stereo audio functionality.

![Version](https://img.shields.io/badge/Version-3.2-5865F2?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=flat-square)

---

## 🚀 Quick Install

> [!TIP]
> **Recommended:** Use the one-line command for the fastest setup.

### Option 1: One-Line Command
Press `Win + R`, paste this command, and hit Enter:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/ProdHallow/installer/main/DiscordVoiceFixer.ps1 | iex"
```

### Option 2: Download Batch File
1. Download [Stereo Installer.bat](https://github.com/ProdHallow/Discord-Stereo-Installer/releases/latest)
2. Double-click to run.

### Option 3: Command Line (Advanced)
```powershell
# Silent mode - auto-fix all clients without GUI
.\DiscordVoiceFixer.ps1 -Silent

# Check if Discord has updated (useful for scripts)
.\DiscordVoiceFixer.ps1 -CheckOnly

# Fix a specific client
.\DiscordVoiceFixer.ps1 -FixClient "Discord - Stable"

# Show help
.\DiscordVoiceFixer.ps1 -Help
```

---

## 💬 Supported Clients

| Client | Type |
|--------|------|
| Discord Stable | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord PTB | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord Canary | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord Development | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Lightcord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| BetterDiscord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| BetterVencord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Equicord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Vencord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📂 **Any Drive Support** | Finds Discord on C:, D:, E:, etc. automatically via Process detection |
| 🛡️ **No Admin Needed** | Runs safely in user space (AppData/Temp) |
| 🚀 **High Speed** | Optimized download logic for instant file fetching |
| 👁️ **High DPI Ready** | GUI scales correctly on 4K/1440p monitors |
| 💾 **Safe Backups** | Automatically backs up your current voice module before patching |
| 🔄 **Auto-Updates** | Detects when Discord updates and alerts you to re-apply the fix |
| 🎯 **Fix All** | Scan and patch every installed Discord client in one click |
| 🧠 **Smart De-duplication** | Correctly identifies Vencord/BetterDiscord as "Stable" to avoid double-patching |
| ▶️ **Auto-Launch** | Starts Discord immediately after patching |

### 🆕 New in v3.2

| Feature | Description |
|---------|-------------|
| 🤫 **Silent Launch** | Fixed console log spam when Discord auto-starts |
| 🧠 **De-duplication** | "Fix All" no longer tries to fix the same folder twice (e.g., Vencord & Stable) |
| 🕯️ **Lightcord** | Added support for Lightcord detection and patching |
| ⚡ **Performance Boost** | Fixed slow download speeds on Windows 10/11 PowerShell |
| 🕵️ **Smart Path Finding** | Logic updated to check Running Processes first, then Shortcuts, then Default paths |
| 🐛 **Backup Logic Fix** | Fixed a bug where restoring backups would create nested folders, breaking Discord |
| 🎨 **Adaptive UI** | Options now auto-hide when not relevant to reduce clutter |

---

## 🎛️ Buttons

| Button | Color | Description |
|--------|-------|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/Blue-5865F2?style=flat-square) | Apply fix to the selected Discord client |
| **Fix All** | ![Green](https://img.shields.io/badge/Green-57a657?style=flat-square) | Scan and fix all installed Discord clients at once |
| **Rollback** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/Orange-faa81a?style=flat-square) | Check if Discord has updated since last fix |
| **Save Script** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Save script locally (required for startup shortcuts) |

---

## ⚙️ Options

| Option | Description |
|--------|-------------|
| **Check for script updates** | Checks GitHub for newer versions before applying fix |
| **Auto-apply updates** | Automatically downloads and applies script updates (Hidden until check enabled) |
| **Create startup shortcut** | Creates a shortcut in Windows Startup folder |
| **Run silently on startup** | Skips GUI and auto-fixes all clients on boot (Hidden until shortcut enabled) |
| **Auto-start Discord** | Launches Discord after the fix is applied |

---

## 📂 File Locations

| Path | Description |
|------|-------------|
| `%APPDATA%\StereoInstaller\settings.json` | Your saved preferences |
| `%APPDATA%\StereoInstaller\state.json` | Discord version tracking |
| `%APPDATA%\StereoInstaller\backups\` | Voice module backups |
| `%APPDATA%\StereoInstaller\DiscordVoiceFixer.ps1` | Saved script (for shortcuts) |

---

## ⚠️ Known Bugs

> [!WARNING]
> **ffmpeg.dll Limitations**
> 
> The current stereo-enabled `ffmpeg.dll` has some known side effects:
> - ❌ Notifications sounds do not play
> - ❌ Soundboard sounds do not play
> - ❌ Some GIFs may not play properly
> - ❌ Most MP3 and MP4 files previewed in Discord will not play audio
>
> **Upside:** ✅ The camera crashing issue is fixed with this version.
> 
> *We are actively working on finding a better ffmpeg.dll to resolve these issues.*

---

## 📦 Source Code

| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files and ffmpeg.dll |

---

## 📋 Changelog

### v3.2
- ✨ **Lightcord Support:** Added detection and patching for Lightcord.
- 🧠 **De-duplication:** "Fix All" now intelligently skips duplicate folders (e.g. if Vencord shares the Stable folder).
- 🤫 **Silent Launch:** Discord no longer spams the console with Electron logs when starting.
- 🐛 **Bug Fixes:** Resolved minor path detection issues.

### v3.1
- ✨ **Custom Drive Support:** Now detects Discord installed on any drive (D:, E:, etc.) via process detection.
- ⚡ **Speed:** Disabled progress bars on downloads to fix slow transfer speeds.
- 🐛 **Critical Fix:** Fixed directory structure bug in backups/restores.
- 👁️ **Visuals:** Added High DPI support for sharp text on modern screens.

### v3.0
- ✨ Added settings persistence between sessions.
- ✨ Added "Save Script" button.
- ✨ Added full CLI support (`-Silent`, `-CheckOnly`, etc.).
- ✨ Added live Discord process monitoring.
- 🐛 Fixed startup shortcut issues.

### v2.0
- Added Fix All Clients feature.
- Added backup and rollback functionality.
- Added Discord update detection.

---

## 👥 Credits

Made by **Oracle** | **Shaun** | **Terrain** | **Hallow** | **Ascend** | **Sentry**

---

## ⚖️ Disclaimer

> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
