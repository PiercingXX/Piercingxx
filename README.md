# PiercingXX
> I bend Linux to my will so you don’t have to. Desktops, tablets, servers, phones — press the button, watch the chaos organize itself.

---

## About ⚙️

I started out building reproducible Linux environments and dotfile ecosystems: menu‑driven installers that turn “fresh ISO” into “daily driver”. That’s still here, and still opinionated. But the scope grew.

I wanted my phone to be just as user friendly as my desktop...so I build a Wayland shell for Linux phones, an Android launcher to match, a local‑first AI assistant that runs entirely on my own hardware, and my own keyboard layout for every platform I touch. Where the open ecosystem falls short, I fork it and grow it until locally hosted AI competes with the cutting‑edge paid models — on hardware I own, with data that never leaves my local network unless I want it to.

The common thread: local‑first, text‑first, reproducible, and no cloud unless I explicitly invite it. Yes, it’s opinionated. No, I won’t apologize.

---

## What I build 🧰

### Installers & dotfiles (the classics)
- **Distro “mod” installers** — Arch, Debian, Fedora, Void, Artix, PopOS, FreeBSD, plus `mini` variants for tablets and note‑taking machines, and Pi‑Gnome for the Raspberry Pi 5
	- Menu‑driven setup (whiptail) with sensible defaults (mine)
	- Hyprland + GNOME mods, Flatpak, UFW, developer tooling
	- Optional NVIDIA + Microsoft Surface kernel support (for the brave)
- **Piercing‑Dots** — one repo to keep your machine updated and configured
	- Hyprland, Awesome, BSPWM, DWM, i3, Sway, and Qtile with unified UX across all of them. 
		- For touchscreen tablets and the like, customized Gnome and my own Piercing WM (see below).
	- Waybar, kitty, Neovim, Yazi, Tmux, GIMP customized into minimal yet fully functional powerhouses
	- Maintenance and software‑manager scripts so you stop copy‑pasting from blogs
	- `Super+/` opens your Cheat Sheet; `Super+S` opens a bash‑driven settings menu — don’t leave the keyboard

### Mobile Linux (the new frontier)
- **Piercing WM** — a minimalist Wayland shell for Linux phones. Text‑first, gesture‑driven, AMOLED black, Space Mono. No icon grids, anywhere. Calls, SMS, lock screen, notification shade — all first‑class surfaces, because a daily driver isn’t a demo.
- **linux‑phone‑mod** — Droidian/Mobian/Ubuntu Touch/PureOS setup in one go, with the full Piercing‑Dots treatment on a phone
- **furi‑phone‑colemak‑keyboard** — a Squeekboard/Phosh on‑screen Colemak layout tuned for Furi phone screens
- **PiercingXX Launcher** — the same text‑first philosophy, ported to Android (Kotlin). Folders, gestures, six theme presets, JSON backup, work‑profile support — and still no icon grid.

### Local AI & self‑hosting
- **Skippy** — a local‑first AI assistant on one box with eight RTX 5090s and zero cloud. Terminal coding agent, tiered per‑person memory, mobile PWA remote over Tailscale, Discord presence (text *and* voice). The brain is served locally; everything else is Skippy — forked, modified, and grown until it goes toe‑to‑toe with the cutting‑edge paid models. Fully solar powered and subscription price: zero.
- **skpp‑radio** — a private local radio station where Skippy writes and voices the ads, controls the Home Assistant speakers, and airs spots on a schedule. Because he can.
- **wyoming‑sentence‑tts** — a Wyoming‑protocol TTS bridge that streams audio per sentence, so your voice assistant starts talking after the first sentence instead of the last one
- **XX‑Stack** — self‑hosted‑first AI orchestration: agent contracts, routing policy, an MCP server, and a local inference control plane over Tailscale. Cloud is strictly opt‑in, and it stays that way.
- **debian‑server** — a single‑file bootstrap that turns a fresh Debian box into a media & AI workstation: CUDA/NVIDIA, Docker/Compose, Nextcloud, local LLMs

### Input & hardware
- **Piercing keyboard layout** — my own layout that no one else will ever use. One layout, every platform: Linux (xkb), Windows, Android/GrapheneOS, and QMK/Vial ortho boards.
- **Device enablement** — drivers and scripts for hardware Linux forgot
	- Microsoft Surface kernel support across the installers
	- NuVision 8" tablet Wi‑Fi/Bluetooth/Audio fixes (you’re welcome)
	- KooTigers touchscreen/driver utilities

---

## How I work 🧪

- POSIX‑first Bash where Bash belongs; Python + GTK4, Kotlin, or TypeScript where it doesn’t
- Local‑first, always: my AI, my inference, my data, my hardware. Cloud is opt‑in or absent.
- Reproducibility over hand‑tweaking; scripts > screenshots (always)
- Text‑first, gesture‑driven, low‑friction UX — on a desktop, a phone, or a lock screen
- Minimal dependencies, sane defaults, readable code, zero drama

---

## Tech I reach for 🛠️

- Bash, systemd, whiptail
- Hyprland (also Sway and Herbst; GNOME on tablets; phoc on phones), Kitty, Yazi, Neovim, tmux
- Python + GTK4/libadwaita + layer‑shell for mobile surfaces; Kotlin for Android
- Pacman/Paru, apt, xbps, Flatpak… build from source when needed (Neovim Nightly & Yazi)
- Docker/Compose, NVIDIA + CUDA, SGLang, Ollama, Wyoming/Home Assistant, Tailscale

---

## Philosophy (short version) 🌀

- Applied entropy: build systems that stay useful as the world changes
- Elegant complexity: hide the sharp edges, keep the power
- Repeatable results: a fresh install should feel like home in minutes
- Local first: if it can run on my hardware, it will
- Defaults with a spine: opinions included at no extra charge

---

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Piercingxx&layout=compact&theme=aura&hide_border=true" height="150"/>
</div>

---

## Contact 📮

- Email: Don’t

	Open an issue in the relevant repo instead. If it’s a rant, make it entertaining.
---
