# 🎧 Stereo Installer

A one-click install tool for Discord Stereo Modules. Automatically downloads and applies the latest voice module patches to restore lossless stereo audio functionality.

![Version](https://img.shields.io/badge/Version-3.3-5865F2?style=flat-square)
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
1. Download `Stereo Installer.bat`
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

## 📊 Audio Analysis: 99.9% Filterless
The latest update patches the audio engine to remove virtually all artificial filtering.

### 🔴 Before (Standard Discord)
Heavy roll-off on low frequencies, aggressive filtering, and noise artifacts.

![Before - Standard Discord](images/before.png)

### 🟢 After (Stereo Installer)
99.9% Filterless. A completely flat, linear response preserving the original audio source perfectly.

![After - Stereo Installer](images/after.png)

## 💬 Supported Clients
| Client | Type |
|--------|------|
| Discord Stable | Official |
| Discord PTB | Official |
| Discord Canary | Official |
| Discord Development | Official |
| Lightcord | Mod |
| BetterDiscord | Mod |
| BetterVencord | Mod |
| Equicord | Mod |
| Vencord | Mod |

## ✨ Features
| Feature | Description |
|---------|-------------|
| 💎 Filterless Audio | Removes internal filters for true lossless quality |
| 📂 Any Drive Support | Finds Discord on C:, D:, E:, etc. automatically via Process detection |
| 🛡️ No Admin Needed | Runs safely in user space (AppData/Temp) |
| 🚀 High Speed | Optimized download logic for instant file fetching |
| 👁️ High DPI Ready | GUI scales correctly on 4K/1440p monitors |
| 💾 Safe Backups | Automatically backs up your current voice module before patching |
| 🔄 Auto-Updates | Detects when Discord updates and alerts you to re-apply the fix |
| 🎯 Fix All | Scan and patch every installed Discord client in one click |
| 🧠 Smart De-duplication | Correctly identifies Vencord/BetterDiscord as "Stable" to avoid double-patching |
| ▶️ Auto-Launch | Starts Discord immediately after patching |

## 🆕 New in v3.3
| Feature | Description |
|---------|-------------|
| 🛠️ No More FFmpeg | **Major Update:** The fix no longer requires replacing `ffmpeg.dll`. |
| ✅ Bugs Patched | Notification sounds, soundboards, and MP3/MP4 previews now work perfectly. |

## 🎛️ Buttons
| Button | Color | Description |
|--------|-------|-------------|
| Start Fix | Blue | Apply fix to the selected Discord client |
| Fix All | Green | Scan and fix all installed Discord clients at once |
| Rollback | Gray | Restore voice module from a previous backup |
| Backups | Gray | Open the backup folder in Explorer |
| Check | Orange | Check if Discord has updated since last fix |
| Save Script | Gray | Save script locally (required for startup shortcuts) |

## ⚙️ Options
| Option | Description |
|--------|-------------|
| Check for script updates | Checks GitHub for newer versions before applying fix |
| Auto-apply updates | Automatically downloads and applies script updates *(Hidden until check enabled)* |
| Create startup shortcut | Creates a shortcut in Windows Startup folder |
| Run silently on startup | Skips GUI and auto-fixes all clients on boot *(Hidden until shortcut enabled)* |
| Auto-start Discord | Launches Discord after the fix is applied |

## 📂 File Locations
| Path | Description |
|------|-------------|
| `%APPDATA%\StereoInstaller\settings.json` | Your saved preferences |
| `%APPDATA%\StereoInstaller\state.json` | Discord version tracking |
| `%APPDATA%\StereoInstaller\backups\` | Voice module backups |
| `%APPDATA%\StereoInstaller\DiscordVoiceFixer.ps1` | Saved script (for shortcuts) |

## 📦 Source Code
| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files |

## 📋 Changelog

### v3.3 (Current)
- 🗑️ **FFmpeg Removal:** The script no longer downloads or replaces `ffmpeg.dll`.
- ✅ **Bug Fixes:** Notification sounds, soundboard audio, and video previews now work correctly.
- 🔧 **Clean Up:** Removed legacy code related to ffmpeg handling.

### v3.2
- 🐛 **Critical Fix:** Fixed a syntax error in the Backup Manager that prevented rollbacks.
- ✨ **Lightcord Support:** Added detection and patching for Lightcord.
- 🧠 **De-duplication:** "Fix All" now intelligently skips duplicate folders (e.g. if Vencord shares the Stable folder).
- 🤫 **Silent Launch:** Discord no longer spams the console with Electron logs when starting.

### v3.1
- ✨ **Custom Drive Support:** Now detects Discord installed on any drive (D:, E:, etc.) via process detection.
- ⚡ **Speed:** Disabled progress bars on downloads to fix slow transfer speeds.
- 🐛 **Critical Fix:** Fixed directory structure bug in backups/restores.
- 👁️ **Visuals:** Added High DPI support for sharp text on modern screens.

## 👥 Credits
Made by **Oracle | Shaun | Terrain | Hallow | Ascend | Sentry**

## ⚖️ Disclaimer
> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
