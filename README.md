# Cyberpunk Animations

Animations ported to Cyberpunk 2077 from other games' open-licensed mods. They are retargeted onto the game's
own NPC rigs (`man_base` / `woman_base`) and onto V's skeleton, and cooked as `.anims`. Release zips also carry the
big and fat rigs (`man_big`, `man_fat`, `woman_big`, `woman_fat`).

**Each pack has its own licence**, stated in its folder: `opensex/` is [CC BY-SA 4.0](LICENSE), `ostimng/` is
[GPLv3](ostimng/LICENSE). You may use, change and redistribute them, commercially too, if you credit the original
authors (each pack's `CREDITS.md`) and release your changes under that pack's licence.

## Packs

| Folder | From | Original authors | Credits |
|---|---|---|---|
| [`opensex/`](opensex/) | [OpenSex](https://github.com/acepleiades/OpenSex) (Skyrim SE, OStim NG) | acepleiades, Frolique | [`opensex/CREDITS.md`](opensex/CREDITS.md) |
| [`ostimng/`](ostimng/) | [OStimNG](https://github.com/VersuchDrei/OStimNG) (Skyrim SE), only the clips OpenSex lacks | as credited by OStimNG: Ace and Moon | [`ostimng/CREDITS.md`](ostimng/CREDITS.md) |

## Layout of a pack

```
<pack>/
  CREDITS.md        who made the originals, the source, what was changed
  depot/            the cooked game files at their depot paths (.anims), packable with WolvenKit
  archive/pc/mod/   <pack>.archive, the animations, and <pack>_amm.archive, what AMM plays them through
  bin/x64/plugins/cyber_engine_tweaks/mods/nightcitynet/data/scenes/<pack>/
                    NightCityNet's scene files: one per scene, its moves and transitions, plus clips.json
  bin/x64/plugins/cyber_engine_tweaks/mods/AppearanceMenuMod/Collabs/Custom Poses/nightcitynet/<pack>.lua
                    the pack's poses in AMM's list
  glb/              GPL packs only: the retargeted .glb, the editable source of each .anims
  scenes.json       the source's scene data as converted, which the scene files were generated from
  source-map.json   each cooked clip -> the original file it came from
```

This repository holds the sources: `glb/`, `bin/`, `scenes.json`, `source-map.json` and the credits. The cooked
`depot/` and the packed `archive/` are in the release zip.

## Install

A release is one zip holding every pack, ready for your mod manager. Its `archive/` and `bin/` folders mirror the game
folder, so you can also copy them into `<Cyberpunk 2077>/`. Each pack's licence and credits are in `licenses/<pack>/`.
The scene files are read by NightCityNet; the animations alone need only the packs' archives.

## Use with Appearance Menu Mod

With [AMM](https://www.nexusmods.com/cyberpunk2077/mods/790) installed, each pack is a category of its own in AMM's
poses, for NPCs and for V. No other animation mod is needed. Each body plays its own half of a two-person pose, so
pick the same pose for both, with the `_0` and `_1` clips. AMM has no list for `woman_big` or `woman_fat`, so those
bodies don't show the packs there.

## What is not here

- **No CD Projekt files.** The `.anims` name the game's rigs by path; no rig, mesh or vanilla clip is copied.
- **No original-game files.** No `.hkx`, no Skyrim skeletons, and no converter built on the Havok SDK.

Large files are stored with [Git LFS](https://git-lfs.com/). Run `git lfs install` once before cloning.
