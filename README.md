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

## Features

- Automatic updates — always runs the latest version
- Downloads fresh voice module files each run
- Creates optional startup shortcut to auto-fix on boot
- Auto-launches Discord after patching

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
