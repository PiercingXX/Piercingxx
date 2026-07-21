# PiercingXX
> I bend Linux to my will so you don’t have to. Workstations, laptops, tablets, servers, phones — press the button, watch the chaos organize itself.

---

## About ⚙️

I enjoy a simple clean UI based on a reproducable dotfile ecosystem with customizations that make sense and eliminate friction. 

- I had to build a few things to make that happen though:
	- A series of reproducible Linux menu‑driven installers that turn “fresh ISO” into “daily driver”.
 	- A Wayland shell for Linux phones
  	- An Android launcher for GraphineOS/LineageOS
  	- A local‑first AI assistant that runs entirely locally and can compete with the cutting‑edge paid models.
  	- A keyboard layout for every platform I touch.
	
Where the open source ecosystem falls short, I fork it and grow it. 
The common thread: local‑first, frictionless, reproducible, and only self hosted cloud. 

Yes, it’s opinionated but that is why its good.

---

## What I build 🧰

### Installers & dotfiles (the classics)
- **Distro “mod” installers** — Arch, Debian, Fedora, Void, Artix, PopOS, FreeBSD, plus `mini` variants for tablets and note‑taking machines, and Pi‑Gnome for the Raspberry Pi 5
	- Menu‑driven setup (whiptail) with sensible defaults (mine)
	- Hyprland, Awesome, BSPWM, DWM, i3, Sway, Qtile and GNOME mods, Flatpak, UFW, developer tooling
	- Optional NVIDIA + Microsoft Surface kernel support assembled for easy script install.
 	- Different variants for Workstations/Servers/Tablets/Phones
- **Piercing‑Dots** — one repo to keep your machine updated and configured
	- Hyprland, Awesome, BSPWM, DWM, i3, Sway, and Qtile with unified UX across all of them. 
		- For touchscreen tablets and the like, customized Gnome and my own Piercing WM (see below).
	- Waybar, kitty, Neovim, Yazi, Tmux, GIMP customized into minimal yet fully functional powerhouses
	- Maintenance and software‑manager scripts so you stop copy‑pasting from blogs
	- `Super+/` opens your Cheat Sheet; `Super+S` opens a bash‑driven settings menu — don’t leave the keyboard

### Mobile Linux
Unfortionalely the mobile market is overrun by two equally non-valid options...then there are Linux phones, also not valid but for different reasons. They are way under developed with many issues and not enough finacial backing to make it a viable market...yet. 

While we wait on a viable Linux device my daily is a Pixel running GraphineOS. 
I built my own launcher as the first step to building the inteface for my linux touch screen devices. 

So far the best phone option I have found is the Fury Phone. There are still some minor issues keeping it from being a daily driver option though.

- **Piercing WM** — a minimalist Wayland shell for Linux phones and tablets. Text‑first, gesture‑driven, AMOLED black, Space Mono. No icon grids, anywhere. Calls, SMS, lock screen, notification shade — all first‑class surfaces. Working toward this being my Daily Driver.
- **PiercingXX Launcher** — the same text‑first philosophy, ported to Android (Kotlin). Folders, gestures, six theme presets, JSON backup, no icon grid.
- **furi‑phone‑colemak‑keyboard** — a Squeekboard/Phosh on‑screen Colemak layout tuned for Furi phone screens

### Local AI & self‑hosting
- **Skippy** — The local‑first AI assistant on one box and zero cloud.
	- Skippy is truley a universal AI.
 		- Terminal coding agent
   		- Personal assistant Home Assistant tie-in
     	- Per‑person/per-location reconization and memory
     	- Mobile app remote over Tailscale (text *and* voice).
      	- Optional Discord presence (text *and* voice).
	- The brain is served locally by whatever model your hardware can manage. 
   	- Designed to be subscription free. Only runs on local hardware.
- **skpp‑radio** — a private local radio station that will stream to multiple locations inside your tailscale network. Skippy writes and voices the ads (if you want them), controls the Home Assistant speakers, and airs spots on a schedule. Because he can.
- **wyoming‑sentence‑tts** — custom fork of the Wyoming‑protocol TTS bridge but this one streams audio per sentence, so your voice assistant starts talking after the first sentence instead of the last one.
- **XX‑Stack** — self‑hosted‑first AI orchestration: agent contracts, routing policy, an MCP server, and a local inference control plane over Tailscale. Cloud is strictly opt‑in.

### Input & hardware
- **Piercing keyboard layout** — my own layout that no one else will ever use. One layout, every platform: Linux (xkb), Windows, Android/GrapheneOS, and QMK/Vial ortho boards.
- **Device enablement** — drivers and scripts for hardware that isnt in the Linux kernals.
	- Microsoft Surface kernel support across the installers
	- NuVision 8" tablet Wi‑Fi/Bluetooth/Audio fixes - obsecure old tech that could be perfect.
	- KooTigers touchscreen/driver utilities - neat little toy that needed some help.

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
- Docker/Compose, NVIDIA + CUDA, SGLang, Ollama, Wyoming/Home Assistant, Tailscale, sglang

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

	Open an issue in the relevant repo. If it’s a rant, make it entertaining.
---
