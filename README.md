# Screen Stocks Mod Manager
A BepInEx plugin that adds a **mod manager** to Screen Stocks. See your installed mods and edit their settings without leaving the game.

-# Unofficial fan-made mod, not affiliated with the Screen Stocks devs. It only edits BepInEx config files. It does not touch your save, trades, money or online data.

## What you can do
- Click the **MODS** button (it replaces the **Tips** `?` button) or press **F10** to open it
- See every installed mod: name, version, GUID and file
- Edit any mod's settings: on/off toggles, pick-lists, and text boxes
- Reset a setting, reset a whole mod, or reload its config from disk
- Disable or enable a mod (takes effect on the next game start)
- Open it inside the game, or as its own separate window (the window closes with the game)
- Changes save to the mod's `.cfg` right away

## Install
1. Install **BepInEx 5.4.x** (Windows x64) in the game folder and run the game once
2. Put `ScreenStocksModManager.dll` in `BepInEx/plugins`
3. Optional, for the separate window: put the `ModManagerWindow` folder in `BepInEx/`, then set `OpenInSeparateWindow = true` in `BepInEx/config/local.screenstocks.modmanager.cfg`
4. Start the game

**Needs:** Windows 64-bit, BepInEx 5.4.x
