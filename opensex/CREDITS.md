# OpenSex for Cyberpunk 2077 — credits

Ported from **OpenSex**, an adult animation set for OStim NG (Skyrim Special Edition):
<https://github.com/acepleiades/OpenSex> · <https://www.nexusmods.com/skyrimspecialedition/mods/61167/>

Licensed under [CC BY-SA 4.0](../LICENSE), as the original is.

## Original authors

| Who | What |
|---|---|
| **acepleiades** | the animations: 313 of the 317 scenes ([Patreon](https://www.patreon.com/skyrimaceanimations)) |
| **Frolique** | the animations of 4 scenes: GentleEmbrace, HoldingChin, HoldingChinHug, HoldingChinKiss |
| **acepleiades, VersuchDrei, DragoFall** | the scene data (positions, transitions, speeds, tags) |

## What was changed

- Decoded from Havok (`.hkx`) and retargeted from the Skyrim (XPMSE) skeleton onto Cyberpunk 2077's
  `man_base` / `woman_base` rigs, and from those onto V's player skeletons.
- Cooked as Cyberpunk `.anims`: one set per OpenSex position folder and body, under
  `opensex\anims\npc\` (`_ma` / `_wa`) and `opensex\anims\player\` (`_pma` / `_pwa`). A clip keeps its
  original file name, lower case, without the leading `_` (`_Cr-MountedGrind_S2_1` is `cr-mountedgrind_s2_1`).
- Scene XML converted to `scenes.json`, and from it NightCityNet's scene files (`bin/.../data/scenes/opensex/`):
  each scene's moves, with OStimNG's menu labels where OStimNG has the same scene; a speed with no file for one
  actor plays that actor's slowest clip.
- Three scenes OpenSex removed in commit `140a6680` while keeping their animations -- LesbianAnimationHub,
  LesbianKneLyBCunnilingus and AceLesbian69Fingering -- are taken from the commit before it, cast as two women (those
  files name no actors), and replace the OPrivacy redirect that later reused the cunnilingus file. Two are renamed:
  "Standing Together" and "Kneeling Cunnilingus" (the original file was titled "Breast Groping").

Each cooked clip names its original file in `source-map.json`.

These changes were made by blackpotoftea. The original authors did not make this port and do not endorse it.
