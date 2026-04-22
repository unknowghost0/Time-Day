# TimeAndDay Mod

A Castle Miner Z mod that displays the current in-game day number and time on the HUD.

## Features

- **Day Counter**: Shows the current day number
- **Time Display**: Shows the current in-game time in HH:MM format (24-hour)
- **HUD Integration**: Displays on the left side of the screen, vertically centered
- **Performance Optimized**: Minimal FPS impact with cached font access
- **Green Text**: Lime green text with dark shadow for visibility

## Display Format

```
Day X | HH:MM
```

Example: `Day 1 | 04:25`

## Installation

1. Build the mod from the TimeAndDay.csproj
2. Place `TimeAndDay.dll` in your game's `!Mods` folder
3. Ensure `ModLoader` is installed and loaded before this mod

## Configuration

- **Position**: Left side of screen, vertically centered (X=16, Y=330)
- **Color**: Lime Green (#00FF00) with black shadow
- **Font**: Medium font from CastleMinerZGame
- **Refresh Rate**: Updates every frame

## Technical Details

- **Patching Method**: Harmony attribute-based patching
- **Target Method**: `InGameHUD.OnDraw()`
- **Font Access**: Instance field reflection with 60-frame cache refresh
- **Framework**: .NET Framework 4.8.1

## Dependencies

- ModLoaderExtensions
- HarmonyLib (0Harmony)
- CastleMinerZ

## Building

```bash
msbuild TimeAndDay.csproj /p:Configuration=Release /p:BuildOutputRoot="...\Build\" /p:ReferenceAssembliesRoot="...\ReferenceAssemblies\"
```

Output: `Build\Release\!Mods\TimeAndDay.dll`

## Mod Details

- **Version**: 1.0.0
- **Author**: TimeAndDay Contributors
- **License**: Copyright © 2026
