# Blade & Sorcery Mod Manager

A lightweight, fully themeable mod manager for **Blade & Sorcery**, built with Python and Tkinter. No third-party dependencies.

## Features

### Mod management
- **Bulk ZIP install**: select multiple mod ZIPs at once and install them in one go
- **Live progress bar** with per-file status, tracked across every file in the batch
- **Safe extraction**: archives are unpacked into a private temp folder first, with protection against malicious paths (zip-slip)
- **Error-tolerant installs**: a bad archive is reported at the end instead of aborting the whole batch
- **Enable / disable mods** without deleting them (disabled mods are moved to a `_DISABLED` folder)
- **Multi-select actions**: enable, disable, or uninstall several mods at once
- **Uninstall confirmation** so nothing is deleted by accident
- **Auto-detects** your Blade & Sorcery `Mods` folder from common Steam locations, or browse to any folder
- **Remembers** your mods folder between launches

### Mod list
- Sortable columns: **Name**, **Status**, and **Size**
- **Instant search** and an All / Enabled / Disabled filter
- Folder sizes calculated in the background, so the list never freezes
- Live counts of total, enabled, and disabled mods
- **Double-click** a mod to toggle it, **Delete** key to uninstall
- **Right-click menu**: Enable, Disable, Open folder, Uninstall

### Profiles
- Save your current enabled/disabled setup as a named **profile**
- **Load** a profile to switch your whole mod loadout in one click
- Rename and delete profiles
- Profile names are validated so they can't create invalid files

### Appearance and customization
- **Rounded UI**: panels, search box, and buttons are drawn with rounded corners
- **Corner roundness slider** from fully square to very round
- **Native title bar theming**: the Windows title bar matches your theme colors (Windows 11 for exact colors, light/dark on Windows 10)
- **Live preview**: every change applies instantly, with Save or Cancel to keep or revert
- **Full color control**: window background, panels, text, muted text, accent, progress bar, and danger buttons, with hex entry or a color picker
- **Typography**: choose any installed font family, font size, and row padding for compact or roomy lists
- **Layout options**: sidebar on the left or right, adjustable sidebar width, and toggles for the size column and status bar
- **Automatic contrast**: button and selection text colors adjust so light themes stay readable

### Themes
- **6 built-in presets**: Crimson Dark, Midnight Blue, Forest, Amoled, Parchment Light, Steel Light
- **Save your own themes**: colors, fonts, roundness, and layout are stored together as a `.json` file
- Saved themes live in `%LOCALAPPDATA%\BladeSorceryModManager\themes\`
- **Quick theme switcher** right in the sidebar
- **Import and export** themes to share them with others
- One-click **Open themes folder** button
- **Reset to default** at any time

### Reliability
- UI stays responsive during installs (work runs on a background thread, UI updates stay on the main thread)
- Moves safely replace existing files instead of failing
- Window size and settings are saved automatically on exit

## Requirements

- Python 3.8 or newer
- Tkinter (included with the standard Python installer on Windows)
- Windows is the primary target. The app also runs on macOS and Linux, but title bar theming is Windows-only

## Getting started

1. The app looks for your Blade & Sorcery `Mods` folder automatically. Use **Browse…** if it can't find it.
2. Click **Install ZIP Mods** and pick one or more mod archives.
3. Use the sidebar or right-click menu to enable, disable, or uninstall mods.
4. Open **Customize** to make the app look the way you like.

## Data locations

| What | Where |
| --- | --- |
| Settings | `%LOCALAPPDATA%\BladeSorceryModManager\config.json` |
| Saved themes | `%LOCALAPPDATA%\BladeSorceryModManager\themes\` |
| Profiles | `<Mods folder>\_PROFILES\` |
| Disabled mods | `<Mods folder>\_DISABLED\` |

## Roadmap

- Mod conflict and dependency detection
- Drag-and-drop ZIP install

## License

MIT
