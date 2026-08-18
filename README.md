# PiercingXX
> I bend Linux to my will so you don’t have to. Workstations, laptops, tablets, servers, phones — press the button, watch the chaos organize itself.

---

## About ⚙️

I prefer a simple clean UI based on a reproducible dotfile ecosystem, with customizations that make sense and eliminate friction.

- I had to build a few things to make that happen:
	- A phone suite for GrapheneOS — launcher, keyboard, app blocker, fitness tracker. My daily driver, built by me.
	- A Wayland shell for Linux phones, so the whole suite has somewhere to go next.
	- A series of reproducible Linux menu‑driven installers that turn “fresh ISO” into “daily driver”.
	- A local‑first AI assistant that runs entirely on my own hardware.
	- A keyboard layout for every platform I touch.

Where the open source ecosystem falls short, I fork it and grow it.

Yes, it’s opinionated, but that is why it’s good.

---

## Phone 📱

The mobile market is overrun by two equally non‑valid options... then there are Linux phones, also not valid but for different reasons: way underdeveloped, many issues, and not enough financial backing to make it a viable market — *yet*.

So while we wait, my daily is a Pixel 9 Pro running GrapheneOS, and I'm replacing the stock experience one app at a time:

- **[XX-Launcher](https://github.com/Piercingxx/XX-Launcher)** — text‑first Android launcher (Kotlin). No icons, no wallpaper clutter. Search‑first drawer, 8 home slots, inline folders, gestures, widgets, theme presets, JSON backup. The design ancestor of everything below.
- **[Nope-Mode](https://github.com/Piercingxx/Nope-Mode)** — selected apps go silent and un‑openable, on a schedule or on demand. Focus Mode for GrapheneOS, where Digital Wellbeing doesn't exist. Runs as device owner; no accounts, no network, no analytics.
- **[HeliBoard fork](https://github.com/Piercingxx/HeliBoard)** — glide typing without the proprietary Google blob. I'm building an open‑source gesture decoder with an offline replay harness to tune it against real swipe recordings.
- **XX-Vitals** (private) — a cleanroom Google Fit replacement: Health Connect on the phone, Postgres on my own NAS, no cloud anywhere. In progress; private until it can walk.
- **TxxT** (private) — too early to talk about.
- **[piercing-keyboard-layout](https://github.com/Piercingxx/piercing-keyboard-layout)** — my own layout that no one else will ever use. One layout, every platform: Linux (xkb), Windows, Android/GrapheneOS, and QMK/Vial ortho boards.

And where it's all headed:

- **[XX-WM](https://github.com/Piercingxx/XX-WM)** — a minimalist Wayland shell for Linux phones and tablets. Text‑first, gesture‑driven, AMOLED black, Space Mono. No icon grids, anywhere. Calls, SMS, lock screen, notification shade — all first‑class surfaces. The Android suite above is the rehearsal; this is the venue. Working toward this being my daily driver.

Which brings us to...

---

## Linux 🐧

### Installers & dotfiles (the classics)
- **Distro “mod” installers** — [Arch](https://github.com/Piercingxx/arch-mod), [Debian](https://github.com/Piercingxx/debian-mod), [Fedora](https://github.com/Piercingxx/fedora-mod), [Void](https://github.com/Piercingxx/void-mod), [Artix](https://github.com/Piercingxx/artix-mod), [FreeBSD](https://github.com/Piercingxx/freebsd-mod), plus `mini` variants for tablets and note‑taking machines ([arch-mini-mod](https://github.com/Piercingxx/arch-mini-mod), [debian-mini-mod](https://github.com/Piercingxx/debian-mini-mod)), [Pi-Gnome](https://github.com/Piercingxx/Pi-Gnome) for the Raspberry Pi 5, and [debian-server](https://github.com/Piercingxx/debian-server) for the media & AI box
	- Menu‑driven setup (whiptail) with sensible defaults (mine)
	- Hyprland, Awesome, BSPWM, DWM, i3, Sway, Qtile and GNOME mods, Flatpak, UFW, developer tooling
	- Optional NVIDIA + Microsoft Surface kernel support assembled for easy script install
	- Different variants for workstations, servers, tablets, and phones
- **[Piercing-Dots](https://github.com/Piercingxx/piercing-dots)** — one repo to keep your machine updated and configured
	- Hyprland, Awesome, BSPWM, DWM, i3, Sway, and Qtile with unified UX across all of them
		- For touchscreen tablets and the like: customized GNOME and my own XX-WM (see above)
	- Waybar, kitty, Neovim, Yazi, Tmux, GIMP customized into minimal yet fully functional powerhouses
	- Maintenance and software‑manager scripts so you stop copy‑pasting from blogs
	- `Super+/` opens your Cheat Sheet; `Super+S` opens a bash‑driven settings menu — don’t leave the keyboard

### Device enabling
Drivers and scripts for hardware that isn’t in the Linux kernel:
- Surface kernel support across the installers
- NuVision 8" tablet Wi‑Fi/Bluetooth/Audio fixes — obscure old tech that could be perfect
- KooTigers touchscreen/driver utilities — neat little toy that needed some help

---

## Local AI & self‑hosting 🤖

- **Skippy** (private) — the local‑first AI assistant on my own hardware and private cloud.
	- Skippy is truly a universal AI:
		- Terminal coding agent
		- Personal assistant with Home Assistant tie‑in
		- Per‑person / per‑location recognition and memory
		- Mobile app remote over Tailscale (text *and* voice)
		- Optional Discord presence (text *and* voice)
	- The brain is served locally by whatever model your hardware can manage
	- Designed to be subscription‑free. Only runs on local hardware.
- **Nagatha** (private) — Skippy add‑on: Skippy's independent auditor and cleanroom counterpart in a two‑agent estate: Skippy builds, Nagatha audits. A terminal agent framework for self‑hosted LLMs behind any OpenAI‑compatible API.
- **Roscoe** (private) — Skippy add‑on: face‑recognition presence and greetings for home and business sites, served over the tailnet.
- **skpp‑radio** (private) — Skippy add‑on: a local radio station that streams to multiple locations inside your Tailscale network. Skippy writes and voices the ads (if you want them), controls the Home Assistant speakers, and airs spots on a schedule. Because he can.
- **skippy-tel** (private) — Skippy add‑on: Skippy's communications layer: event streams with a hard business/personal wall, offline‑first, and agents post through the same door people do.
- **elder-ai** (private) — Skippy add‑on: drop cleaned business email's in, dash in some FAQs and website links, get a local model that talks like an employee plus a RAG index over the real correspondence. Runs on this box. No cloud.
- **jal** (private) — Skippy add‑on: offline inventory sourcing engine. House catalog, USD quotes, a staff chatbot for skippy-tel; everything stays on the machine.
- **[wyoming-sentence-tts](https://github.com/Piercingxx/wyoming-sentence-tts)** — fork of the Wyoming‑protocol TTS bridge that streams audio per sentence, so your voice assistant starts talking after the first sentence instead of the last one.
- **XX‑Stack** (private) — self‑hosted AI orchestration with optional cloud tie-in for Opencode and Hermes Agent: agent contracts, routing policy, an MCP server, and a local inference control plane over Tailscale. This is what Skippy started as. This has grown alongside Skippy as a benchmark tool.

---

## Battlezone 98 Redux 🎮

The 1998 tank‑RTS/FPS hybrid that refuses to die...and I intend to keep it that way:

- **[battlezone-netcode-patch](https://github.com/Piercingxx/battlezone-netcode-patch)** — netcode patch for BZ98 Redux multiplayer.
- **[battlezone98-map-generator](https://github.com/Piercingxx/battlezone98-map-generator)** — AI map‑generation toolchain (`bzmap`) for multiplayer maps: generation pipeline, format writers, validators, and Workshop packaging.
- **[BattleZone98-Godot-Map-Editor](https://github.com/Piercingxx/BattleZone98-Godot-Map-Editor)** — a feature rich Godot‑based map editor for the same.
- **[BZ1-GameWatcher](https://github.com/Piercingxx/BZ1-GameWatcher)** — fork of the multiplayer game watcher.
- **skippy-battlezone-map-generator** (private) — this one is explicitly for Skippy with lots of testing and future plans in the works. The public toolchain above was extracted from this.
- **skippy-plays-battlezone** (private) — Skippy plays BZ98 Redux as a real multiplayer opponent: own client, own player slot, own scoreboard line, acting only through the same input path a human uses. **Currently Shelved ** - Skippy needs more data.

---

## Odds & ends 🗃️

- **piercingxx-branding** (private) — the brand system behind all of the above: color, type, logomark, and voice.
- **hha-platform** (private) — a full business web platform: booking, chat, docs, and forms. Next.js + Prisma.
- **book-list** (private) — my ongoing attempt to separate the worthwhile from the well‑marketed nonsense.

---

## How I work 🧪

- POSIX‑first Bash where Bash belongs; Python + GTK4, Kotlin, or TypeScript where it doesn’t
- Local‑first, always: my AI, my inference, my data, my hardware. Cloud is opt‑in or absent.
- Reproducibility over hand‑tweaking; scripts > screenshots (always)
- Text‑first, gesture‑driven, low‑friction UX — on a desktop, a phone, or a lock screen
- Minimal dependencies, sane defaults, readable code, zero drama

---

## Tech I reach for 🛠️

- Bash, systemd (when needed), whiptail
- Hyprland (also Sway and Herbst; GNOME on tablets; phoc on phones)
- Kitty, Yazi, Neovim, tmux
- Python + GTK4/libadwaita + layer‑shell for mobile surfaces; Kotlin for Android
- Pacman/Paru, apt, xbps, Flatpak… build from source when needed (Neovim Nightly & Yazi)
- Docker/Compose, NVIDIA + CUDA, SGLang, Wyoming/Home Assistant, Tailscale

---

## Philosophy (short version) 🌀

- Applied entropy: build systems that stay useful as the world changes
- Elegant complexity: hide the sharp edges, keep the power
- Repeatable results: a fresh install should feel like home in minutes
- Local first: if it can run on my hardware, it will...if it cant, buy more hardware
- Defaults with a spine: opinions included at no extra charge

---

## Contact 📮

- Email: Don’t

	Open an issue in the relevant repo. If it’s a rant, make it entertaining.
---
