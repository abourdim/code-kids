# 🚀 CodeKids v3 — Learn to Code!

**By XSCO** | Interactive coding platform for kids & beginners

![Version](https://img.shields.io/badge/version-3.0-22c55e)
![Lessons](https://img.shields.io/badge/lessons-39-3b82f6)
![Languages](https://img.shields.io/badge/languages-3-f97316)
![Themes](https://img.shields.io/badge/themes-9-8b5cf6)
![Dependencies](https://img.shields.io/badge/dependencies-0-ef4444)

---

## ✨ What is CodeKids?

CodeKids is a **zero-dependency, single-file** interactive coding playground that teaches HTML, CSS, JavaScript, UI controls, and science/tech concepts through **39 hands-on lessons** in **3 languages**.

Just open `index.html` in any browser. No install. No server. Works offline.

---

## 📖 Lesson Tracks

### Track 1: Basics (27 lessons)

#### Tier 1 — 🧱 Build It (HTML)
| # | Lesson | What You Learn |
|---|--------|---------------|
| 1 | My First Page | HTML tags, headings, paragraphs |
| 2 | Cool Lists | Ordered & unordered lists |
| 3 | Images & Links | `<img>` and `<a>` tags |

#### Tier 2 — 🎨 Style It (CSS)
| # | Lesson | What You Learn |
|---|--------|---------------|
| 4 | Paint Your Page | Inline styles, colors |
| 5 | Game Cards | CSS classes, gradients, hover effects |
| 6 | Animations | @keyframes, spin, bounce, rainbow |

#### Tier 3 — ⚡ Power It (JavaScript)
| # | Lesson | What You Learn |
|---|--------|---------------|
| 7 | Click Power | onclick events, alerts |
| 8 | Calculator | DOM manipulation, math operations |
| 9 | Monster Clicker | Game loop, variables, upgrades |

#### Tier 4 — 🎛️ Controls & Gadgets (18 lessons)
| # | Lesson | What You Learn |
|---|--------|---------------|
| 10 | Slider Control | Range inputs, RGB color mixer |
| 11 | Joystick | Drag controls, position tracking |
| 12 | Bar Chart | Data visualization with DOM |
| 13 | Gauge Meter | Canvas arc drawing, animated needle |
| 14 | Toggle Switch | Boolean state, on/off UI |
| 15 | Checkbox Group | Multi-select, pizza builder |
| 16 | Radio Buttons | Single-select, theme picker |
| 17 | Tooltip Slider | Floating tooltip follows thumb |
| 18 | Stepper Counter | Plus/minus with min/max limits |
| 19 | Star Rating | Click-to-rate, hover preview |
| 20 | Color Picker | RGB sliders, hex output |
| 21 | Stopwatch | Start/stop/lap, millisecond precision |
| 22 | Thermometer | Temperature gauge, °C/°F conversion |
| 23 | Progress Ring | SVG circle, animated progress |
| 24 | Piano Keys | Web Audio API, keyboard shortcuts |
| 25 | Radar Sweep | Canvas animation, polar coordinates |
| 26 | Flashlight | Toggle, brightness, color temperature |
| 27 | Drag & Drop | Reorderable list, drag events |

### Track 2: Science & Tech (12 lessons)

#### 🟢 Beginner
| # | Lesson | What You Learn |
|---|--------|---------------|
| 1 | Ohm's Law Lab | V=I×R calculator, electron animation |
| 2 | Morse Code | Text to dots/dashes, audio beeps |
| 3 | Logic Gates | AND/OR/NOT/XOR toggle simulation |
| 4 | Wave Playground | Sine/square/sawtooth waveforms |

#### 🔵 Explorer
| # | Lesson | What You Learn |
|---|--------|---------------|
| 5 | Robot Commander | Grid robot, command programming |
| 6 | Star Map | 100+ real stars, constellation view |
| 7 | Signal Lab | Wave mixing, AM/FM modulation |
| 8 | Periodic Table | 118 elements, interactive grid |

#### 🔴 Advanced
| # | Lesson | What You Learn |
|---|--------|---------------|
| 9 | Spectrum Analyzer | Microphone FFT, live frequency display |
| 10 | Fourier Visualizer | Harmonic decomposition, 8 sliders |
| 11 | Satellite Tracker | ISS orbit, world map projection |
| 12 | Circuit Builder | Drag/drop components, simulation |

---

## 🌍 Languages

| Language | Direction | Font |
|----------|-----------|------|
| 🇬🇧 English | LTR | Fredoka |
| 🇫🇷 Français | LTR | Fredoka |
| 🇸🇦 العربية | RTL | Noto Sans Arabic |

All 39 lessons are fully translated. Code examples remain universal (HTML/CSS/JS are language-independent).

---

## 🎨 Themes

| Theme | Style | Accent |
|-------|-------|--------|
| 🌙 Stealth | Dark slate + starfield | Green `#22c55e` |
| ⚡ Neon | Cyberpunk + starfield | Cyan `#00d4ff` |
| ☁️ Arctic | Light & clean | Blue `#2563eb` |
| 🔥 Blaze | Deep ember | Orange `#ff6600` |
| 🌊 Ocean | Deep sea | Cyan `#00e5ff` |
| 🐉 Dragon | Purple + starfield | Violet `#a855f7` |
| 🤖 Cyber | Matrix terminal | Green `#00ff41` |
| 🥷 Ninja | Dark stealth | Red `#ff4444` |
| 🕌 Islamic Heritage | Deep green + gold + starfield | Gold `#d4af37` |

---

## 🏗️ Architecture

```
codekids-v3/
├── index.html   (788 lines, 102KB — the entire app)
├── logo.svg     (XSCO brand logo)
└── README.md    (this file)
```

### Single-File Design
- **Zero dependencies** — no npm, no CDN, no build step
- **Zero server** — runs from `file://` protocol
- **Offline-first** — works without internet (after first font load)
- **102KB total** — smaller than most images

### Technical Details
- CSS custom properties for theming (20+ variables per theme)
- Responsive grid/flexbox layout with mobile sidebar toggle
- Sandboxed iframe for live code preview
- Canvas-based starfield animation (dark themes only)
- Web Audio API for Piano & Morse Code lessons
- Full RTL support for Arabic (direction, borders, alignment)
- `{{/SC}}` placeholder system to safely embed `<script>` in lessons

---

## 🚀 Usage

```bash
# Option 1: Just open it
open index.html
# (or double-click in file explorer)

# Option 2: Local server (optional)
python3 -m http.server 8000
# → http://localhost:8000
```

---

## 📊 Stats

| Metric | Value |
|--------|-------|
| Total lessons | 39 |
| Total translated | 117 (39 × 3) |
| Themes | 9 |
| Languages | 3 |
| File size | 102KB |
| Lines of code | 788 |
| Dependencies | 0 |
| Build step | None |

---

## 📜 Version History

| Version | Changes |
|---------|---------|
| v1.0 | React JSX prototype |
| v1.1 | Converted to standalone HTML/CSS/JS |
| v1.2 | Fixed `</script>` escaping bug |
| v2.0 | Complete rebuild: dual-track, 25 lessons, 9 themes, 3 languages, micro:bit-inspired UI |
| v3.0 | Expanded Controls to 18 gadgets (39 total lessons), `{{/SC}}` placeholder fix |

---

## 📄 License

© XSCO — All rights reserved.

---

*Built with ❤️ for the next generation of coders.*
