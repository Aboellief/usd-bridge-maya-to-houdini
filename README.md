# USD Bridge — Maya to Houdini

**Move a full Maya scene into Houdini (Karma or Arnold) — or into a clean new Maya — through properly structured USD. No rebuild.**

[![Watch the full walkthrough](https://img.youtube.com/vi/krMLf5W39uQ/maxresdefault.jpg)](https://youtu.be/krMLf5W39uQ)

▶ **[Watch the full walkthrough (3 min)](https://youtu.be/krMLf5W39uQ)** · 🛒 **[Get USD Bridge on Gumroad](https://aboellief.gumroad.com/l/jetmm)**

> 🚀 **Launch offer:** 50% off with code `LAUNCH50` until **November 20, 2026** ($79 → $39.50) — [apply the discount](https://aboellief.gumroad.com/l/jetmm/LAUNCH50)

---

## Why

Every time a scene jumps from Maya to Houdini, the same work starts again: re-linking textures, rebuilding shaders, re-creating lights, re-doing render settings. USD Bridge skips the rebuild.

## Tested on a real production scene

| | |
|---|---|
| Meshes | 2,629 |
| Polygons | 10.4M |
| Materials / Textures | 44 / 57 |
| Lights / Render cameras | 3 / 1 |
| Export click → Houdini open | **~2 minutes** |

## How it works

1. **Scan** — the Dashboard reads geometry, materials, textures, cameras and lights. Read-only.
2. **Validate & Auto Fix** — see every issue, preview every fix, apply them all as one Maya undo. *(On the test scene: 8 issues found, 114 fixes previewed.)*
3. **Export** — pick a target: Maya (Arnold), Houdini (Arnold) or Houdini (Karma). Use USD layers (a Static layer for the set, written once, plus Animated layers for anything that moves) or one flat layer.
4. **Build** — a new Maya or Houdini opens on its own with the scene ready to render.

## What comes across

- Geometry, hierarchy and animation
- **Materials:** Arnold → Arnold keeps the same shaders. **Karma gets MaterialX.**
- **Lights, render settings, AOVs and Cryptomatte** rebuilt as native Houdini nodes (or Maya's own render settings for a Maya build) — open and edit them like anything you built yourself
- Render cameras (default cameras never export) and the Maya frame range
- Displaced surfaces in Karma are baked with Arnold's subdivision, so displaced water doesn't tile

## Honest notes

- Maya Arnold and Houdini Arnold renders match.
- Karma renders come straight out of the build and need a touch of look-dev (water/sea materials differ from Arnold; area lights read about 15% brighter).
- Animated lights come across static in Karma. Hair and XGen are not supported yet.
- Native builds for Windows, macOS and Linux; tested so far on Windows.

The goal isn't a magic button. It's skipping the rebuild.

## Requirements

- Maya 2024.2+, 2025, 2026 or 2027 with Arnold (MtoA) and the Maya USD plug-in
- Houdini 20.5 or newer for Houdini targets (+ HtoA for Arnold renders)
- Windows 10/11 · macOS (Apple silicon or Intel) · Linux x86_64

## Licence

Commercial tool. One key per computer, lifetime, no subscription, works offline. This repository is the public showcase and support page — **no source code is published here.**

## Support

Found an issue or have a pipeline question? [Open an issue](../../issues) or email **ahmed.elsayed.abo.ellief@gmail.com**.

---

Made by **Ahmed Abo Ellief** — Senior Technical Artist, Lighting & LookDev · [YouTube](https://www.youtube.com/channel/UCCPOgFevCLEK8_F7IX8j4VA) · [ArtStation](https://ahmedaboellief.artstation.com) · [LinkedIn](https://www.linkedin.com/in/ahmed-aboellief) · [Gumroad](https://aboellief.gumroad.com)
