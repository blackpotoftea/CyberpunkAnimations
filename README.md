# Cyberpunk Animations

Various animations for Cyberpunk 2077, ported from other games' open-licensed mods: one, two and more people,
standing, sitting, lying and on furniture. They are retargeted onto the game's NPC rigs (`man_base` / `woman_base`)
and V's skeletons, and the release also carries the big and fat rigs (`man_big`, `man_fat`, `woman_big`, `woman_fat`).

**Download:** the [latest release](https://github.com/blackpotoftea/CyberpunkAnimations/releases/latest) is one zip
with every pack, ready for your mod manager.

## Packs

| Folder | Ported from | Original authors | Licence | Credits |
|---|---|---|---|---|
| [`animation/opensex/`](animation/opensex/) | [OpenSex](https://github.com/acepleiades/OpenSex) | acepleiades, Frolique | [CC BY-SA 4.0](LICENSE) | [`CREDITS.md`](animation/opensex/CREDITS.md) |
| [`animation/ostimng/`](animation/ostimng/) | [OStimNG](https://github.com/VersuchDrei/OStimNG), the clips OpenSex lacks | Ace and Moon, as OStimNG credits them | [GPLv3](animation/ostimng/LICENSE) | [`CREDITS.md`](animation/ostimng/CREDITS.md) |

You may use, change and redistribute them, commercially too, if you credit the original authors (each pack's
`CREDITS.md`) and release your changes under that pack's licence. The original authors did not make this port and do
not endorse it.

## What is in this repository

The sources; the cooked animations are in the release zip.

```
animation/<pack>/
  CREDITS.md        who made the originals, where they come from, what was changed
  bin/x64/plugins/cyber_engine_tweaks/mods/nightcitynet/data/scenes/<pack>/
                    NightCityNet's scene files: one per scene, its moves and transitions, plus clips.json
  bin/x64/plugins/cyber_engine_tweaks/mods/AppearanceMenuMod/Collabs/Custom Poses/nightcitynet/<pack>.lua
                    the pack's poses in AMM's list
  glb/              GPL packs only: the retargeted .glb, the editable source of each cooked animation
  scenes.json       the original scene data as converted, which the scene files were generated from
  source-map.json   each cooked clip -> the original file it came from
```

## Install

Install the release zip with your mod manager, or copy its `archive/` and `bin/` folders into `<Cyberpunk 2077>/`.
Each pack's licence and credits are in the zip under `licenses/<pack>/`. The scene files are read by NightCityNet; the
animations alone need only the archives.

## Use with Appearance Menu Mod

With [AMM](https://www.nexusmods.com/cyberpunk2077/mods/790) installed, each pack is a category of its own in AMM's
poses, for NPCs and for V. Each body plays its own half of a two-person pose, so pick the same pose for both, with the
`_0` and `_1` clips. AMM has no list for `woman_big` or `woman_fat`, so those bodies don't show the packs there.

## What is not here

- **No CD Projekt files.** The animations name the game's rigs by path; no rig, mesh or vanilla clip is copied.
- **No original-game files.** No `.hkx`, no Skyrim skeletons, and no converter built on the Havok SDK.

Large files are stored with [Git LFS](https://git-lfs.com/). Run `git lfs install` once before cloning.
