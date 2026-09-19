# PiercingXX
> I bend Linux to my will so you don’t have to. Workstations, laptops, tablets, servers, phones — press the button, watch the chaos organize itself.

---

## About ⚙️

I prefer a simple clean UI based on a reproducible dotfile ecosystem, with customizations that make sense and eliminate friction.

- I had to build a few things to make that happen:
	- A GrapheneOS phone suite — launcher, store, files, camera, photos, notes, calendar, mail, radio, audiobooks, the rest — plus a keyboard. My daily driver, built by me.
	- A Wayland shell for Linux phones, so the whole suite has somewhere to go next.
	- A series of reproducible Linux menu‑driven installers that turn “fresh ISO” into “daily driver”.
	- A local‑first AI assistant that runs entirely on my own hardware.
	- A keyboard layout for every platform I touch.

Where the open source ecosystem falls short, I fork it and grow it.

Yes, it’s opinionated, but that is why it’s good.

---

## Phone 📱

The mobile market is overrun by two equally non‑valid options... then there are Linux phones, also not valid but for different reasons: way underdeveloped, many issues, and not enough financial backing to make it a viable market — *yet*.

So while we wait, my daily is a Pixel 9 Pro running GrapheneOS, and I've replaced the stock experience one app at a time:

- **XX-Apps** (private) — the suite store. One login (Skippy username/password), one catalog, updates from the house forge. Not Play. Not F-Droid. Not Obtainium.
- **[XX-Launcher](https://github.com/Piercingxx/XX-Launcher)** — text‑first Android launcher (Kotlin). No icons, no wallpaper clutter. Search‑first drawer, 8 home slots, inline folders, gestures, widgets, theme presets, JSON backup. The design ancestor of everything below.
- **[TxxT](https://github.com/Piercingxx/TxxT)** — SMS in the same style as the launcher, with a few extras to cut out the noise.
- **[XX-Dialer](https://github.com/Piercingxx/xx-dialer)** — pretty much the same as TxxT but for calls, with a ring policy attached: spam never rings, starred contacts always ring, everyone else rings only inside their allowed time-window.
- **[XX-Contacts](https://github.com/Piercingxx/xx-contacts)** — a UI over the system address book. Not a second contact store, not CardDAV, not a dialer. Ring policy stays in XX-Dialer. No INTERNET.
- **[Nope-Mode](https://github.com/Piercingxx/Nope-Mode)** — selected apps go silent and un‑openable, on a schedule or on demand. Focus Mode for GrapheneOS, where Digital Wellbeing doesn't exist. Runs as device owner; no accounts, no network, no analytics.
- **[XX-Calculator](https://github.com/Piercingxx/xx-calculator)** — Its a Calculator, that matches my theme. BigDecimal engine, no Android dependencies in the math.
- **XX-Calendar** (private) — syncs with Google through DAVx⁵, because sometimes we still need to use Google, but not on my phone, refuses to do the other ninety things Google Calendar does at you. No INTERNET on the app. The CalDAV backend lives in the same repo.
- **[XX-Email](https://github.com/Piercingxx/xx-email)** — Gmail without the proprietary Google blob. Tabs, snooze, undo-send, operator search. No Play Services, no analytics.
- **[XX-Note](https://github.com/Piercingxx/xx-note)** — Keep's front end over a folder of Markdown files on my own NAS. Every note is one plain file with frontmatter. Delete the app and lose nothing.
- **[XX-Clock](https://github.com/Piercingxx/xx-clock)** — clock, alarms, timers, offline. Per‑alarm ringtones.
- **[XX-Weather](https://github.com/Piercingxx/xx-weather)** — ZIP in, forecast out. NWS first, Open-Meteo if NOAA is down. No location permission, no Play Services.
- **[XX-Files](https://github.com/Piercingxx/xx-files)** — a real directory tree (`File.listFiles()`), not MediaStore “Recent / Images / Downloads”. Per‑volume trash, 30‑day restore. No INTERNET.
- **[XX-Keyboard](https://github.com/Piercingxx/xx-keyboard)** — swipe-first English keyboard with Colemak and Piercing layouts. Glide typing, no INTERNET permission, no proprietary Google blob.
- **[XX-Auth](https://github.com/Piercingxx/xx-auth)** — offline TOTP/HOTP. Secrets stay in the Android Keystore. Scan a QR or paste a URI. No network, no cloud account, no telemetry.
- **[XX-Camera](https://github.com/Piercingxx/xx-camera)** — Pixel-class camera: AUTO, MANUAL, panorama/360. Writes JPEG/DNG/video on the phone. No INTERNET. The library is XX-Photos, not this APK.
- **[XX-Photos](https://github.com/Piercingxx/xx-photos)** — private photo library on hardware I own. Phone client plus FastAPI server in the same repo. Timeline, backup, albums; tagging stays on the server.
- **[XX-Audiobook](https://github.com/Piercingxx/xx-audiobook)** — FastAPI server + Kotlin/Compose client in one repo. Audiobooks, ebooks, podcasts, RSS from my NAS. Not a storefront account.
- **[XX-Vitals](https://github.com/Piercingxx/xx-vitals)** — a cleanroom Google Fit replacement: entered on the phone, Postgres on my own NAS, no cloud anywhere.

The app that works with Android and Linux right now:
- **[XX-Drive](https://github.com/Piercingxx/xx-drive)** — self‑hosted file sync: one static Go binary on the server, plus a web UI, a Linux CLI client, and an Android app. Files stay as plain files on disk, metadata in SQLite.

They work individually or with the xx-launcher sharing a single active color theme. These apps will probably work on other versions of android, but its not tested.
Any app that reaches out to a server, make sure you have Tailscale installed (or Headscale) and point the app at your server. Done.

And where it's all headed:

- **[XX-WM](https://github.com/Piercingxx/XX-WM)** — a minimalist Wayland shell for Linux phones and tablets. Text‑first, gesture‑driven, AMOLED black, Space Mono. No icon grids, anywhere. Calls, SMS, lock screen, notification shade — all first‑class surfaces. The Android suite above is the rehearsal; this is the venue. Working toward this being my daily driver.

## **All the Android apps ARE my daily drivers. XX-WM is under construction.**

Which brings us to...

---

## Linux 🐧

### Installers & dotfiles (the classics)
- **[linux-mod](https://github.com/Piercingxx/linux-mod)** — one workstation installer for Arch, Artix, Debian/Ubuntu, Fedora, Void, openSUSE, and Alpine. The per‑distro trees I still keep are [Arch](https://github.com/Piercingxx/arch-mod), [Debian](https://github.com/Piercingxx/debian-mod), [FreeBSD](https://github.com/Piercingxx/freebsd-mod), plus `mini` variants for tablets ([arch-mini-mod](https://github.com/Piercingxx/arch-mini-mod), [debian-mini-mod](https://github.com/Piercingxx/debian-mini-mod))
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
- Surface kernel support across the installers.
- NuVision 8" tablet Wi‑Fi/Bluetooth/Audio fixes — obscure old tech that could be perfect if it was made with modern hardware.
- KooTigers touchscreen/driver utilities — neat little toy that needed some help.

---

## Local AI & self‑hosting 🤖

- **Skippy** (private) — the local‑first AI assistant on my own hardware and private cloud.
	- Skippy is a universal AI:
		- Terminal coding agent
		- Personal assistant with Home Assistant tie‑in
		- Per‑person / per‑location recognition and memory
		- Mobile app remote over the Skippy-Tel-Network (text *and* voice)
		- Optional Discord presence (text *and* voice)
	- Home Assistant TTS is a per‑sentence Wyoming bridge that lives inside Skippy. There is no separate TTS repo.
	- Skippy orchestrates. Bilby builds. Nagatha audits and cleanrooms. They do not share a session.
	- The brain is served locally by whatever model your hardware can manage.
	- Designed to be subscription‑free, secure, private, and only runs on local hardware.
- **Bilby** (private) — Skippy add‑on: Skippy queues the work, Bilby builds.
- **Nagatha** (private) — Skippy add‑on: Skippy's independent auditor and cleanroom counterpart.
- **skippy-tel-network** (private) — Headscale mesh, cross-node sync daemon, Cloudflare LB ingress, split-horizon DNS, location gateway. The federated network Skippy breaths on. Everything else rides on this.
- **Skippy-Speaker** (private) — drop‑in replacement electronics for Google Home Max–class speakers. Home Assistant voice satellite on hardware I own.
- **xx-chat** (private) — Mattermost-wire compatible staff/group chat with AI agent tie in, event-log spine, membership walls, agents-as-staff. Offline-first; agents post through the same door people do.
- **Roscoe** (private) — Skippy add‑on: face‑recognition presence and greetings for home and business sites, served over the Skippy-Tel-Network.
- **skpp‑radio** (private) — Skippy add‑on: a local radio station that streams to multiple locations inside the Skippy-Tel-Network. FastAPI server + Kotlin phone client in the same repo — listen on the phone, drive house speakers by zone, air spots on a schedule. Skippy writes and voices the ads if you want them.
- **elder-ai** (private) — Skippy add‑on: This is a local AI model trainer. Runs on this box. No cloud.
- **Margaret** (private) — Skippy add‑on: front‑desk business agent. Answers from a trained facts store, drafts email (never sends), interactive client chat on the website. Local brain only.
- **Jal** (private) — Skippy add‑on: offline inventory sourcing engine. House catalog, USD quotes, a staff chatbot via xx-chat; everything stays on the machine.
- **[XX-Stack](https://github.com/Piercingxx/xx-stack)** — let your local AI use every computer you own. Agent contracts, routing policy, an MCP server, and a local inference control plane over Tailscale. Cloud APIs are off unless you switch them on. This is what Skippy started as; it grew alongside as a benchmark tool.
- **[free-opencode-hermes](https://github.com/Piercingxx/free-opencode-hermes)** — a local proxy so OpenCode (and Hermes-Agent) can run from the terminal against providers you already have keys for, or models on machines you own. Keys stay in the proxy, not in the agent.

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
- **xx-platform** (private) — a self‑hosted ops platform for the businesses under XX: scheduling, bookkeeping, documents, reminders. Next.js + Prisma + PostgreSQL. One login, one database.
- **[piercing-keyboard-layout](https://github.com/Piercingxx/piercing-keyboard-layout)** — my own layout that no one else will ever use. One layout, every platform: Linux (xkb), Windows, Android/GrapheneOS, and QMK/Vial ortho boards.
- **[tailscale-protonvpn-exitnode](https://github.com/Piercingxx/tailscale-protonvpn-exitnode)** — docker‑compose: Tailscale plus ProtonVPN as an exit node.
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
