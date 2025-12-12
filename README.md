Here is the updated README. I bumped the version to **v3.1** to reflect the major logic improvements regarding non-C: drive support and the UI polish.

# 🎧 Stereo Installer

A one-click install tool for Discord Stereo Modules. Automatically downloads and applies the latest voice module patches to restore lossless stereo audio functionality.

![Version](https://img.shields.io/badge/Version-3.1-5865F2?style=flat-square)
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
2. Double-click to run

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
| BetterDiscord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| BetterVencord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Equicord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Vencord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📂 **Any Drive Support** | Finds Discord on C:, D:, E:, etc. automatically |
| 🔄 **Automatic Updates** | Always runs the latest version |
| 🎯 **Fix All Clients** | Scan and patch all installed Discord clients at once |
| 💾 **Backup & Rollback** | Automatically backs up voice modules before patching; restore anytime |
| 🔔 **Update Detection** | Alerts you when Discord updates and the fix needs to be reapplied |
| 📁 **Quick Backup Access** | Open your backup folder directly from the app |
| ⚠️ **Running Warning** | Warns you if Discord is running and will be closed |
| 🛡️ **Safe Detection** | Uses Start Menu shortcuts instead of Registry (No AV flags) |
| ▶️ **Auto-Launch** | Starts Discord after patching |

### 🆕 New in v3.1

| Feature | Description |
|---------|-------------|
| 🕵️ **Smart Path Finding** | Logic updated to check Running Processes first, then Start Menu shortcuts |
| 💾 **Settings Persistence** | Your preferences are saved and restored between sessions |
| 🎨 **Adaptive UI** | Options now auto-hide when not relevant to reduce clutter |
| 📝 **Save Script** | Save the script locally for startup shortcuts to work properly |
| 🤫 **Silent Mode** | Run without GUI using `-Silent` flag - perfect for automation |
| 🔄 **Live Discord Check** | Automatically updates Discord running status every 5 seconds |

---

## 🎛️ Buttons

| Button | Color | Description |
|--------|-------|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/Blue-5865F2?style=flat-square) | Apply fix to the selected Discord client |
| **Fix All** | ![Green](https://img.shields.io/badge/Green-57a657?style=flat-square) | Scan and fix all installed Discord clients at once |
| **Rollback** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/Orange-faa81a?style=flat-square) | Check if Discord has updated since last fix |
| **Save Script** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Save script to AppData (required for startup shortcut) |

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
> The current ffmpeg.dll has some known issues:
> - ❌ Notifications do not play
> - ❌ Soundboards do not work
> - ❌ GIFs may not play properly
> - ❌ Most MP3 and MP4 files will not play

> [!NOTE]
> **Upside:** ✅ The camera crashing issue is fixed with this version.
> 
> We are actively working on finding a better ffmpeg.dll to resolve these issues.

---

## 📦 Source Code

| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files and ffmpeg.dll |

---

## 📋 Changelog

### v3.1
- ✨ **Custom Drive Support:** Now detects Discord installed on any drive (D:, E:, etc.)
- 🧠 **Smart Logic:** Improved install path detection (checks Process -> Shortcut -> Default)
- 🎨 **UI Polish:** Sub-options now auto-hide when not relevant
- 🐛 **Bug Fix:** Fixed logic timing where killing Discord first prevented path detection

### v3.0
- ✨ Added settings persistence between sessions
- ✨ Added "Save Script" button
- ✨ Added full CLI support (`-Silent`, `-CheckOnly`, etc.)
- ✨ Added live Discord process monitoring
- 🐛 Fixed startup shortcut issues

### v2.0
- Added Fix All Clients feature
- Added backup and rollback functionality
- Added Discord update detection

### v1.0
- Initial release

---

## 👥 Credits

Made by **Oracle** | **Shaun** | **Terrain** | **Hallow** | **Ascend** | **Sentry**

---

## ⚖️ Disclaimer

> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
