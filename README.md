<div align="center">

<img src="https://i.pinimg.com/originals/a0/6d/46/a06d460e5ff30e20ec42ea4ba127b140.gif" alt="Aesthetic Anime Banner" width="560"/>

# 🌸 イマージョン・スタック — Immersion Stack ✨

### *Every anime immersion tool in one place. Pick a stage, pick a tool, start listening.* 🎧

<br>

[![Apps](https://img.shields.io/badge/Apps-14-cba6f7?style=for-the-badge)](https://github.com/Praveensenpai/anime-immersion-stack)
[![Built with](https://img.shields.io/badge/Built%20with-Rust-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Platform](https://img.shields.io/badge/Platform-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://archlinux.org/)
[![License](https://img.shields.io/badge/License-MIT-89b4fa?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Curated-a6e3a1?style=for-the-badge)](https://github.com/Praveensenpai/anime-immersion-stack)
[![Made with](https://img.shields.io/badge/Made%20with-%E2%9D%A4%20-f38ba8?style=for-the-badge)](https://github.com/Praveensenpai)

<br>

[🗺️ Pipeline](#-the-pipeline) • [📑 Catalog](#-app-catalog) • [🏷️ Tags](#-tag-legend) • [🧩 Flow](#-end-to-end-flow) • [🔗 Adjacent](#-adjacent-tools)

</div>

---

> [!TIP]
> **Zero Bloat · Pure Curation · 14 Tools · One Overview**
> This repo is a living index of the anime / Japanese-immersion ecosystem. No installs, no config — just a fast map of what exists, what each tool does, and where it plugs into the pipeline.

---

## 🗺️ The Pipeline

```
   ┌──────────────┐    ┌──────────────┐    ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
   │  🔎 DISCOVER  │    │  📥 ACQUIRE   │    │  🧹 PREP      │    │  🎧 AUDIO     │    │  🌱 LISTEN &  │
   │              │    │              │    │              │    │              │    │     MINE      │
   ├──────────────┤    ├──────────────┤    ├──────────────┤    ├──────────────┤    ├──────────────┤
   │  anirel      │    │  nagare      │    │  jpsan       │    │  otopod      │    │  ototune     │
   │              │───►│  seedr-dl    │───►│  dubstrip    │───►│  immersionpod│───►│  ototunetake │
   │              │    │  seedr-relay │    │  kikoe       │    │              │    │  kotonoha    │
   │              │    │              │    │  subsink     │    │              │    │              │
   └──────────────┘    └──────────────┘    └──────────────┘    └──────────────┘    └──────────────┘
        pick               download            clean files          condense            study
```

**1. Discover** what to watch → **2. Acquire** the file → **3. Prep** it into pure Japanese media → **4. Condense** dialogue for passive listening → **5. Listen & mine** vocabulary back into Anki. 🔄

---

## 📑 App Catalog

All tools by [@Praveensenpai](https://github.com/Praveensenpai). Most are Rust, terminal-first, and built to chain together.

<br>

### 🔎 1. Discover — find something to watch

| App | What it does | Tags | Repo |
|:--|:--|:--|:--:|
| **anirel** 🌸 | MyAnimeList relation-graph TUI. Finds related anime you haven't watched — lazy-loaded, text-first. | `rust` `tui` `offline` | [link](https://github.com/Praveensenpai/anirel) |

<br>

### 📥 2. Acquire — get the file

| App | What it does | Tags | Repo |
|:--|:--|:--|:--:|
| **nagare** 🌊 | RSS scheduler: new episodes → Seedr → fast download → rename → Jellyfin → Telegram notify → cloud purge. | `rust` `tui` `automation` | [link](https://github.com/Praveensenpai/nagare) |
| **seedr-dl** ⚡ | Seedr.cc automation engine + multi-threaded chunk downloader + Gemini AI Jellyfin renaming. | `rust` `cli` `library` | [link](https://github.com/Praveensenpai/seedr-dl) |
| **seedr-relay** ⚡ | FIFO magnet queue daemon. Stages to Seedr, notifies via Tayori, downloads, sanitizes names, writes `note.txt`. | `rust` `cli` `daemon` | [link](https://github.com/Praveensenpai/seedr-relay) |

<br>

### 🧹 3. Prep — strip everything that isn't Japanese

| App | What it does | Tags | Repo |
|:--|:--|:--|:--:|
| **jpsan** ⛩️ | Lossless cleaner (< 1.5s/ep). Keeps JP audio + JP subs, purges foreign dubs, typesetting fonts, tag spam. | `rust` `cli` `lossless` | [link](https://github.com/Praveensenpai/jpsan) |
| **dubstrip** 🗡️ | Origin-aware audio-stripper with 4-gate download safety. Keeps the native master track, drops redundant dubs. | `rust` `cli` `lossless` | [link](https://github.com/Praveensenpai/dubstrip) |
| **kikoe** ⛩️ | Spoken-language ID from raw audio waveforms across 107 languages — ignores untrustworthy container tags. | `rust` `cli` `ai` | [link](https://github.com/Praveensenpai/kikoe) |
| **subsink** ⛩️ | Subtitle fetcher + auto-syncer. Searches 7,200+ titles on Jimaku.cc / Kitsunekko, aligns via ALASS. | `rust` `tui` `subtitles` | [link](https://github.com/Praveensenpai/subsink) |

<br>

### 🎧 4. Audio — passive listening

| App | What it does | Tags | Repo |
|:--|:--|:--|:--:|
| **otopod** 🎧 | Single-pass audio condenser (replaces `impd`). Video → pure Japanese dialogue `.opus` in 2–3s, zero temp files. | `rust` `cli` `audio` | [link](https://github.com/Praveensenpai/otopod) |
| **immersionpod** 🎧 | Setup utility: installs MPD/mpc/ffmpeg + `impd`, generates PipeWire-compatible config. | `bash` `cli` `setup` | [link](https://github.com/Praveensenpai/immersionpod) |
| **ototune** 🎵 | Minimal Ratatui MPD client. AJATT shortcut `i` immerses the active folder; saves playback position. | `rust` `tui` `audio` | [link](https://github.com/Praveensenpai/ototune) |

<br>

### 🌱 5. Listen & Mine — active study

| App | What it does | Tags | Repo |
|:--|:--|:--|:--:|
| **ototunetake** 🌸 | Shadowing player driven by your reviewed Anki collection. Shadow / repeat / gap controls, mature-card queue. | `rust` `tui` `anki` | [link](https://github.com/Praveensenpai/ototunetake) |
| **kotonoha** 🌸 | i+1 sentence miner. Sudachi.rs tokenizer + on-device naturalness scorer → Anki cards with audio & screenshots. | `rust` `cli` `anki` `offline` | [link](https://github.com/Praveensenpai/kotonoha) |

---

## 🏷️ Tag Legend

| Tag | Meaning |
|:--|:--|
| `rust` | Written in Rust 🦀 |
| `bash` | Shell script |
| `cli` | Command-line only |
| `tui` | Interactive terminal UI |
| `daemon` | Runs in the background |
| `library` | Usable as a Rust crate |
| `automation` | Scheduled / hands-off |
| `ai` | Uses an LLM or model |
| `subtitles` | Subtitle fetching / syncing |
| `audio` | Audio processing / playback |
| `anki` | Integrates with Anki |
| `japanese` | Japanese-language focus |
| `offline` | Works without network |
| `lossless` | No re-encoding / zero quality loss |
| `setup` | Installer / environment setup |

---

## 🧩 End-to-End Flow

```text
anirel                    → pick a title
nagare / seedr-*          → download + sort into Jellyfin
subsink                   → fetch & sync Japanese subs
jpsan / dubstrip / kikoe   → clean video + audio tracks
otopod                    → condense dialogue audio
ototune                   → passive listening
ototunetake               → shadowing from Anki reviews
kotonoha                  → mine new i+1 sentences back into Anki
```

> [!NOTE]
> The loop closes at **kotonoha** — mined sentences become new Anki cards, which feed **ototunetake**, which drives more listening. Passive and active immersion reinforce each other.

---

## 🔗 Adjacent Tools

General media utilities that aren't anime-specific, but live in the same ecosystem:

- 🎵 **PixelPlayer** — Material 3 offline music player (Jetpack Compose). [link](https://github.com/Praveensenpai/PixelPlayer)
- 📺 **SmartTubeEx** — SmartTube build with keyword/channel filtering for Android TV. [link](https://github.com/Praveensenpai/SmartTubeEx)
- ⬇️ **kukufm-dl** — Multi-threaded KukuFM audio downloader. [link](https://github.com/Praveensenpai/kukufm-dl)

---

<div align="center">

Made with 💖 by [Praveen Senpai](https://github.com/Praveensenpai)

*🌸 イマージョン・スタック — curated for the people who just want to listen.*

</div>
