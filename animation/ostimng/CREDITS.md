# OStimNG extras for Cyberpunk 2077 — credits

Ported from **OStimNG**, the OStim Standalone mono repo (Skyrim Special Edition):
<https://github.com/VersuchDrei/OStimNG>

Licensed under [GPLv3](LICENSE), as the original is.

**Only the clips OpenSex does not have.** An OStimNG clip whose animation is also in
[OpenSex](https://github.com/acepleiades/OpenSex) is ported from OpenSex instead, in the [`opensex/`](../opensex/)
pack.

## Original authors

| Who | What |
|---|---|
| **Ace and Moon** | the animations, as OStimNG's README credits them |
| **a community member** | animations added in OStimNG's commit "added new animations provided by a community member" (2026-08-03); the repo does not name them |
| **VersuchDrei** | OStimNG, its scene data, and changes to some of the animations |

## What was changed

- Converted from Skyrim SE's 64-bit Havok (`.hkx`), decoded against the skeleton each clip was authored on, and
  retargeted from the Skyrim skeleton onto Cyberpunk 2077's `man_base` / `woman_base` rigs, and from those onto V's
  player skeletons.
- Cooked as Cyberpunk `.anims`: one set per OStimNG folder and body, under `ostimng\anims\npc\` (`_ma` / `_wa`) and
  `ostimng\anims\player\` (`_pma` / `_pwa`). A clip keeps its original file name, lower case.
- Scene JSON converted to `scenes.json`. A scene half whose clip comes from OpenSex names it as `opensex:<clip>`.
- From OStimNG's scene files, NightCityNet's scene files (`bin/.../data/scenes/ostimng/`), with OStimNG's menu labels
  on the moves. A scene that is an OpenSex scene is filed with OpenSex's, its moves and labels joined to it.

The editable source of every `.anims`, the retargeted `.glb`, is in `glb/` at the same path. Each cooked clip names
its original file in `source-map.json`.

These changes were made by blackpotoftea. The original authors did not make this port and do not endorse it.
