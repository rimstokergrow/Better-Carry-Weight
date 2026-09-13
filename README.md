# dawnwalker-ngplus-save-transfer
New Game Plus save transfer mod for The Blood of Dawnwalker — carry level, perks, money and gear into NG+

# The Blood of Dawnwalker — New Game Plus Save Transfer Mod

<!--
GitHub "About" description (put this in the repo settings, not here):
New Game Plus save transfer mod for The Blood of Dawnwalker — carry level, perks, money and gear into NG+
Suggested topics: blood-of-dawnwalker, ue4ss, new-game-plus, save-tool, modding, lua
-->

Carry your progress into New Game Plus for **The Blood of Dawnwalker**.
This UE4SS mod exports your level, learned perks, unspent skill points,
money, and equipped weapons/armor at the end of a campaign, then imports
them into a fresh New Game Plus save. Your original save files are never
modified.

![Exporting a save in one campaign and importing it into a fresh New Game Plus run in The Blood of Dawnwalker](dawnwalker-new-game-plus-export-import.gif)
<!-- TODO: record the GIF above (export -> start NG+ -> import) and save it
     as dawnwalker-new-game-plus-export-import.gif in the repo root -->

## Features

- One keypress to export, one to import
- Original saves untouched — everything lives in a separate snapshot file
- Config toggles for exactly what gets carried over
- Ships with a one-click installer, no manual folder copying required

## What gets carried over

| Data | Toggle in `config.lua` |
|---|---|
| Character level + unspent skill points | `TransferLevel` |
| Learned perks / traits | `TransferTraits` |
| Money | `TransferMoney` |
| Equipped weapon + armor | `TransferItems` |
| Equipped unique items | `TransferUnique` |

Turn `TransferUnique` off if a carried-over unique item ends up conflicting
with a quest in your new campaign.

## Requirements

- The Blood of Dawnwalker (Steam or GOG)
- [UE4SS](https://www.nexusmods.com/thebloodofdawnwalker/mods/18) installed
  for this game

## Installation

1. Install UE4SS for The Blood of Dawnwalker first, if you haven't already.
2. Download the latest release below.
3. Run `DawnwalkerNGPlus_Installer.exe` and paste in your game's install
   folder (the one containing `Dawnwalker.exe`) when asked.

   **Manual install (no installer):** copy the `Scripts` folder and
   `enabled.txt` into
   `<game>\Binaries\Win64\ue4ss\Mods\DawnwalkerNGPlus\`.

## Usage

| Action | Hotkey |
|---|---|
| Export progress | `Ctrl+F7` |
| Import progress | `Ctrl+F8` |

Export at the end of your campaign, start New Game Plus, then import.
Visit a Road Shrine afterward to review restored perk ranks and spend any
remaining skill points.

`Ctrl+F6` is intentionally avoided — it's used by another common mod.

## Compatibility

Built and tested against the current UE4SS release for this game. Works
alongside the Dawnwalker Mod Menu. If a game update breaks it, check the
Issues tab before reporting — a fix may already be in progress.

## Downloads

Grab the latest packaged release (installer + mod files) from the
[Releases](../../releases) page — no need to clone the repo.

## Contributing

Issues and pull requests welcome, especially compatibility reports against
new game patches.

## License

[MIT](LICENSE)
