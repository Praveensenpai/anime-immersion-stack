# 🌸 Anime Immersion Stack — App Catalog

> A single place to see every anime / Japanese-immersion tool in the collection, what it does, and where it fits in the pipeline.

All tools are by [@Praveensenpai](https://github.com/Praveensenpai). Most are Rust, terminal-first, and designed to chain together.

---

## 🗺️ The Pipeline

```
DISCOVER          ACQUIRE            PREP / CLEAN           AUDIO              LISTEN / MINE
────────          ────────            ──────────           ─────              ─────────────
anirel            nagare              jpsan                otopod             ototune
             ──►   seedr-dl     ──►    dubstrip      ──►    immersionpod ──►   ototunetake
                  seedr-relay         kikoe                                  kotonoha
                                      subsink
```

1. **Discover** what to watch → **2. Acquire** the file → **3. Clean** it into pure Japanese media → **4. Condense** audio for passive listening → **5. Listen & mine** vocabulary back into Anki.

---

## 📱 The Apps

### 1. Discover — find something to watch

| App | What it does | Repo |
|---|---|---|
| **anirel** 🌸 | MyAnimeList relation-graph TUI. Finds related anime you haven't watched. Lazy-loads, no images. | [link](https://github.com/Praveensenpai/anirel) |

### 2. Acquire — get the file

| App | What it does | Repo |
|---|---|---|
| **nagare** 🌊 | RSS scheduler: new episodes → Seedr → high-speed download → rename → Jellyfin → Telegram notify → purge cloud. Headless CLI + TUI. | [link](https://github.com/Praveensenpai/nagare) |
| **seedr-dl** ⚡ | Seedr.cc automation engine + multi-threaded chunk downloader + Gemini AI Jellyfin renaming. CLI and Rust library. | [link](https://github.com/Praveensenpai/seedr-dl) |
| **seedr-relay** ⚡ | FIFO magnet queue daemon. Stages torrents to Seedr, notifies via Tayori, downloads, sanitizes filenames, writes `note.txt`. | [link](https://github.com/Praveensenpai/seedr-relay) |

### 3. Prep / Clean — strip everything that isn't Japanese

| App | What it does | Repo |
|---|---|---|
| **jpsan** ⛩️ | Lossless anime video cleaner (under 1.5s/ep). Keeps Japanese audio + JP subs, purges foreign dubs, English typesetting fonts, tags. | [link](https://github.com/Praveensenpai/jpsan) |
| **dubstrip** 🗡️ | Origin-aware audio-track stripper. 4-gate download safety, preserves the native theatrical master, strips redundant dubs. Lossless `-c copy`. | [link](https://github.com/Praveensenpai/dubstrip) |
| **kikoe** ⛩️ | Spoken-language ID from raw audio waveforms across 107 languages — ignores untrustworthy container tags. | [link](https://github.com/Praveensenpai/kikoe) |
| **subsink** ⛩️ | Subtitle fetcher + auto-syncer. Searches 7,200+ titles on Jimaku.cc / Kitsunekko, aligns timing with ALASS. Interactive TUI. | [link](https://github.com/Praveensenpai/subsink) |

### 4. Audio — passive listening

| App | What it does | Repo |
|---|---|---|
| **otopod** 🎧 | Single-pass anime audio condenser (replaces `impd`). Video → pure Japanese dialogue `.opus` in 2–3s, zero temp files. | [link](https://github.com/Praveensenpai/otopod) |
| **immersionpod** 🎧 | Setup utility: installs MPD/mpc/ffmpeg + `impd`, generates PipeWire-compatible config. | [link](https://github.com/Praveensenpai/immersionpod) |
| **ototune** 🎵 | Minimal Ratatui MPD client. AJATT shortcuts (`i` = immerse active folder), position persistence, dual-pane. | [link](https://github.com/Praveensenpai/ototune) |

### 5. Listen & Mine — active study

| App | What it does | Repo |
|---|---|---|
| **ototunetake** 🌸 | Shadowing player driven by your reviewed Anki collection. Shadow/repeat/gap controls, queue from mature cards. | [link](https://github.com/Praveensenpai/ototunetake) |
| **kotonoha** 🌸 | i+1 sentence miner. Sudachi.rs tokenizer, on-device naturalness scorer, generates Anki cards with audio + screenshots from anime + subs. | [link](https://github.com/Praveensenpai/kotonoha) |

---

## 🔗 Adjacent tools (general media, not immersion-specific)

- **PixelPlayer** — Material 3 offline music player (Compose). [link](https://github.com/Praveensenpai/PixelPlayer)
- **SmartTubeEx** — SmartTube with keyword/channel filtering for Android TV. [link](https://github.com/Praveensenpai/SmartTubeEx)
- **kukufm-dl** — Multi-threaded KukuFM audio downloader. [link](https://github.com/Praveensenpai/kukufm-dl)

---

## 🧩 Typical end-to-end flow

```
anirel                    → pick a title
nagare / seedr-*          → download + sort into Jellyfin
subsink                   → fetch & sync Japanese subs
jpsan / dubstrip / kikoe   → clean video + audio tracks
otopod                    → condense dialogue audio
ototune                   → passive listening
ototunetake               → shadowing from Anki reviews
kotonoha                  → mine new i+1 sentences back into Anki
```

---

*Made with 💖 by Praveen Senpai.*
