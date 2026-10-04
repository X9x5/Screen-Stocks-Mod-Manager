## Use

- Put the dll in BepInEx/Plugins in Screen Stocks
- Open the game menu and click **MODS**, or press **F10** anywhere.
- Left: installed mods. Right: that mod's settings, grouped by section.
  - bool = ON/OFF button, enums and "acceptable value" lists = `< value >` cycler,
    everything else = text box (same format as the .cfg file; Enter or click away to apply).
  - **Reset** per setting, **Reset all**, **Reload from disk**.
  - **Disable/Enable (needs restart)** renames the DLL to `.dll.disabled` and back.
  - "Show other DLLs" lists plugin-folder DLLs that aren't loaded plugins (libraries, disabled files).
- Edits save to the mod's .cfg immediately. Mods that listen for `SettingChanged` react at once; others read config at startup.

## Separate window

In `BepInEx\config\local.screenstocks.modmanager.cfg` set `OpenInSeparateWindow = true` (section `[Window]`).
The MODS button / F10 then opens the Mod Manager as its own Windows window (`ScreenStocksModManagerWindow.exe`,
installed into `BepInEx\ModManagerWindow` by build.bat). It edits the .cfg files directly and the game reloads them live
while the window is open. Default is `false` (in-game window).

## Which button is replaced

By default the **Tips** button becomes the MODS button (`ButtonToReplace = tips`). Quit is not touched.
Set `ReplaceExistingButton = false` to add a separate button instead.

## If the button lands in the wrong place (or nowhere)

The scene layout wasn't available, so the menu is auto-detected: the largest group of the game's
`CustomButton`s. Press **F9** and look in `BepInEx\LogOutput.log` for the `[dump]` list, then put the
right path into `BepInEx\config\local.screenstocks.modmanager.cfg` -> `TargetParentPath`.
If nothing is found after 20 s a small floating MODS button appears top-right (configurable).
