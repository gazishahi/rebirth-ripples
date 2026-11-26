# Rebirth Ripples

**Living water for FINAL FANTASY VII REBIRTH (PC).** A simulated ocean, wakes, splashes and wet characters, with an in-game settings panel.

**[Download the latest release](../../releases/latest)**

## What it does

- **A simulated ocean.** Wind-driven waves of many sizes, with whitecaps that form on breaking crests, drift and fade. Swimming, floating objects and the Tiny Bronco ride the same waves you see.
- **Wakes.** Swimmers and Chocobos push bow waves, leave V-shaped wakes and foam trails, and make rings when they jump or fall in. A swimming Chocobo pushes white water around its chest.
- **Splashes.** Arm strokes and kicks make small splashes, and hands and feet make their own ripples. A sword swung into the water cuts a dent in the shape of the blade and throws up spray.
- **Rivers and lakes.** Wakes and ripples there too, drifting downstream with the current, which also carries you along.
- **Shorelines.** Characters stand up and wade in shallow water instead of swimming through the seabed.
- **Wet characters.** Clothes, skin and fur darken and shine where the water reached them, and dry over time (faster when moving).
- **An in-game settings panel** (Ctrl+Shift+F1) to tune all of it while you look at the water.

## Requirements

- **Game version:** Steam PC version, update 1.004. On any other game version the mod switches itself off and the game runs as normal (see [After a game update](#after-a-game-update)).
- **An ASI loader:** [Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader). You already have one if you use FF7RebirthFix, which installs it as `dsound.dll`.
- **Recommended: ShaderInjector** with its shader pack. With it, the ocean and rivers keep ShaderInjector's refraction and caustics, plus Rebirth Ripples' open-water whitecaps and fine wave detail. Without it, everything else still works; the water surface uses the game's own shading (no open-water whitecaps).
- **System:** Windows 10 or 11, DirectX 12.

## Install

1. Close the game.
2. Download `RebirthRipples-<version>.zip` from the [releases](../../releases).
3. Copy the `End` folder from the zip into your game folder (the folder that already has an `End` folder). Say yes if Windows asks to merge folders. That puts one file in place:
   `End\Binaries\Win64\RebirthRipples.asi`
4. Play. On the first launch the settings panel opens once by itself. After that, a small note at the top right reminds you of the key.

The game folder is usually `C:\Program Files (x86)\Steam\steamapps\common\FINAL FANTASY VII REBIRTH` (in Steam: right-click the game > Manage > Browse local files).

Each release lists the SHA-256 of its zip and of the `.asi`, so you can check your download.

## Settings

**Ctrl+Shift+F1** opens and closes the settings panel. Changes apply at once; press **Save** to keep them. Everything is stored in `End\Binaries\Win64\RebirthRipples.ini`, which is created on the first launch; you can also edit it in Notepad while the game is closed.

- **Quality:** Off (the game's own water), Low, Medium or High. Low and Medium draw fine wave detail and distant water more cheaply.
- **Ocean:** sea state (Calm, Breezy, Rough, Stormy), wind, wave height, choppiness, whitecaps.
- **Wakes and swimming**, **Weapons and impacts**, **Rivers and lakes**, **Characters** (wetness, drying).
- **Advanced:** a few switches that apply after a restart, and what to do after a game update.

While the panel is open, mouse and keyboard go to the panel, not to the game.

| Keys | |
|---|---|
| Ctrl+Shift+F1 | settings panel |
| Ctrl+Shift+F9 | cycle the water: the game's own / rebuilt / debug view / Rebirth Ripples (for comparing) |
| Ctrl+Shift+F2 | character wetness: on / debug view / off |

## Uninstall

Delete from `End\Binaries\Win64`:

- `RebirthRipples.asi`
- `RebirthRipples.ini`, `RebirthRipplesGUI.ini`, `RebirthRipples*.log`
- the `RebirthRipples` folder (cached shaders)

## After a game update

The mod checks the game version at start-up. On a version it doesn't know yet, it switches itself off and the game runs unmodded. Wait for a new version of the mod.

To try anyway, set one of these in `RebirthRipples.ini`:

- `UnknownBuild=1`: the water visuals only, with no changes to gameplay.
- `UnknownBuild=2`: everything, at your own risk.

## Compatibility

- **Tested with** ShaderInjector (recommended, see [Requirements](#requirements)), FF7RebirthFix, HDR and DLSS frame generation (dlssg_for_sm86).
- **Final Foliage Reenabled:** a different file and no overlapping hooks, so they should run together. Not yet tested side by side.
- **One copy only:** only one copy of Rebirth Ripples can run; a second copy switches itself off.

## Something wrong?

Open an [issue](../../issues) and attach `RebirthRipples.log` from `End\Binaries\Win64`. The previous two sessions are kept as `RebirthRipples.prev.log` and `RebirthRipples.prev2.log`.

No log at all means the mod isn't loaded. Check that `RebirthRipples.asi` is in `End\Binaries\Win64` and that an ASI loader is installed.

## Credits

- **ShaderInjector** and its shader pack, by their authors: the ocean and river surfaces build on them. Rebirth Ripples doesn't include any of their files; it reads your installed copy and builds its water shaders on your PC.
- **[Dear ImGui](https://github.com/ocornut/imgui)** by Omar Cornut and contributors (MIT licence, see [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)).

FINAL FANTASY VII REBIRTH is a trademark of Square Enix. Rebirth Ripples is an unofficial fan mod, not affiliated with or endorsed by Square Enix.
