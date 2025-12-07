# Stereo Installer

A one-click install tool for Discord Stereo Modules. Automatically downloads and applies the latest voice module patches to restore lossless stereo audio functionality.

## Quick Install

### Option 1: One-Line Command
Press `Win + R`, paste this command, and hit Enter:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/ProdHallow/installer/main/DiscordVoiceFixer.ps1 | iex"
```

### Option 2: Download Batch File
1. Download [Stereo Installer.bat](https://github.com/ProdHallow/Discord-Stereo-Installer/releases/latest)
2. Double-click to run

## Supported Clients

| Client | Type |
|--------|------|
| Discord Stable | Official |
| Discord PTB | Official |
| Discord Canary | Official |
| Discord Development | Official |
| BetterDiscord | Mod |
| Vencord | Mod |
| Equicord | Mod |

## Features !!!Update!!! v2.0

- **Automatic updates** — always runs the latest version
- **Fix All Clients** — scan and patch all installed Discord clients at once
- **Backup & Rollback** — automatically backs up voice modules before patching; restore anytime
- **Discord update detection** — alerts you when Discord updates and the fix needs to be reapplied
- **Quick backup access** — open your backup folder directly from the app
- **Discord running warning** — warns you if Discord is running and will be closed
- **Completion sound** — audio notification when fix completes
- **Startup shortcut** — optional auto-fix on Windows boot
- **Auto-launches Discord** after patching

## Buttons

| Button | Description |
|--------|-------------|
| Start Fix | Apply fix to the selected Discord client |
| Fix All | Scan and fix all installed Discord clients at once |
| Rollback | Restore voice module from a previous backup |
| Backups | Open the backup folder in Explorer |
| Check | Check if Discord has updated since last fix |

## Known Bugs

> **ffmpeg.dll Limitations**
> 
> The current ffmpeg.dll has some known issues:
> - Notifications do not play
> - Soundboards do not work
> - GIFs may not play properly
> - Most MP3 and MP4 files will not play
> 
> **Upside:** The camera crashing issue is fixed with this version.
> 
> We are actively working on finding a better ffmpeg.dll to resolve these issues.

## Source Code

| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files and ffmpeg.dll |

## Credits

Made by **Oracle** | **Shaun** | **Terrain** | **Hallow** | **Ascend**

## Disclaimer

This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
