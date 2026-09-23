<div align="center">

[Русский](README.md) · **English**

<img src="assets/logo.svg" alt="DeskRift" width="96">

# DeskRift

**Living wallpapers for Windows. YouTube and RuTube videos, your own files, GIFs — and a 3D universe rendered in real time that never repeats itself.**

[🌐 Website](https://deskrift.app) · [⬇️ Download](#download) · [🐛 Report a bug](../../issues/new/choose)

<!-- Bump the version badge by hand on every release. -->
![Windows 0.2.7](https://img.shields.io/badge/Windows_10%2F11-0.2.7-0078D6?logo=windows&logoColor=white)
![0% GPU in games](https://img.shields.io/badge/in%20games-0%25%20GPU-2ea44f)
![WebGL2](https://img.shields.io/badge/engine-WebGL2%20%2B%20Rust-blue)
![RU / EN / 中文](https://img.shields.io/badge/languages-RU%20%2F%20EN%20%2F%20中文-blueviolet)

<img src="assets/hero-poster.webp" alt="A black hole with real gravitational lensing — an actual engine frame" width="720">

<sub>Not a stock image — a frame the engine computed on the GPU.</sub>

</div>

---

Your desktop stops being a backdrop for icons. Put on a clip, a GIF, or switch to space — and the camera flies endlessly through a procedural universe: planets with atmospheres, stars with boiling plasma, black holes with real gravitational lensing. Every launch is a different route. Start a game and the wallpaper pauses instantly, handing the GPU back in full.

## Download

| Platform | File | Size | From the site | From GitHub |
|---|---|---|---|---|
| **Windows 10/11** · installer | `DeskRift-Setup.exe` | 108.4 MB | [download](https://deskrift.app/download/DeskRift-Setup.exe) | [v0.2.7](../../releases/tag/v0.2.7) |

The site and [Releases](../../releases) host **the same file, byte for byte** — take whichever is convenient. The site link always points at the latest build; Releases keeps past versions and checksums.

On first run Windows may show SmartScreen: the installer is not code-signed yet, so the publisher is "unknown" to the system. Click **"More info" → "Run anyway"**. Only download DeskRift from the official site or from here.

**The app is free.** No subscriptions, no Pro tier, no ads.

> **Updates are manual.** There is a "Check for updates" item in the user menu — the app never polls or downloads anything on its own. To move to a newer version, click that item or download the installer again.

## What it does

- 🪐 **A real-time 3D universe.** Not a recording — a WebGL2 simulation. Planets, nebulae, black holes, pulsars, comets, tidal disruption events. The universe is generated from a seed: a new launch is a new world.
- ▶️ **YouTube and RuTube video.** Paste a link or use the built-in search — DeskRift streams it to the desktop without waiting for a download. Like it? Save it to the library and watch offline, up to 4K.
- 📁 **Your own files and GIFs.** Local videos, seamless loops. You can cut a GIF straight out of any clip, no external tools.
- 🗂️ **Wallpaper catalogs.** Built-in collections: browse previews, apply in one click.
- 🖥️ **Multi-monitor done properly.** `span` — one continuous scene across every screen, honouring their real layout and DPI; `clone` — the same picture on each, frame-synced; `unique` — a separate universe per monitor.
- ⏸️ **0% GPU in games.** A fullscreen game or film pauses the render and frees the GPU. It comes back when you do.
- 🎚️ **Three graphics tiers.** One engine from an office laptop to a gaming rig: Light, Balanced, Maximum, plus an automatic mode.
- 🖱️ **Cursor parallax.** Space responds to mouse movement, even underneath your icons.
- 🌗 **Dark and light themes**, Russian, English and Chinese.
- 🔌 **Runs on its own.** The wallpaper lives in a separate process: set it up, close the window, the picture keeps going.

## Control center

Wallpapers, library, downloads and settings in one window.

<div align="center">
<img src="assets/app-ui.webp" alt="DeskRift control center" width="760">
</div>

## One setup, one scene

<div align="center">
<img src="assets/multimonitor.webp" alt="Space stretched across three monitors" width="760">
</div>

## Catalogs

<div align="center">
<img src="assets/catalog.webp" alt="Catalog of ready-made living wallpapers" width="760">
</div>

## Requirements

- Windows 10 or 11, 64-bit
- A WebGL2-capable GPU for the space engine. Video wallpapers run on almost anything
- YouTube and RuTube need an internet connection; local files and the space engine do not

## Found a bug, or want something?

[Open an issue](../../issues/new/choose) — I read all of them. It helps to include:

- your DeskRift version (user menu → "About");
- what happened and what you expected;
- a screenshot, if the defect is visible;
- a diagnostics bundle: **Settings → Logs → Export**.

## About this repository

There is **no source code here** — only the download page, releases and the issue tracker. The source is closed.

Privacy and security questions: [SECURITY.md](SECURITY.md).

---

<div align="center">
<sub>DeskRift · <a href="https://deskrift.app">deskrift.app</a></sub>
</div>
