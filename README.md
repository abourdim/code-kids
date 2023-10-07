# 🚀 CodeKids v4

**A zero-dependency, single-file educational coding platform for kids aged 6–14.**

CodeKids teaches HTML, CSS, and JavaScript through 39 interactive lessons with a live code editor, instant preview, and gamification — all in one offline-ready HTML file.

![Version](https://img.shields.io/badge/version-4.0-brightgreen) ![Dependencies](https://img.shields.io/badge/dependencies-0-blue) ![Lessons](https://img.shields.io/badge/lessons-39-orange) ![Languages](https://img.shields.io/badge/languages-3-purple)

---

## Quick Start

1. Download `index.html` and `logo.svg` into the same folder
2. Open `index.html` in any modern browser
3. That's it — no server, no install, no internet needed

---

## Features

### Learning System

**39 Lessons** across two tracks:

- **Basics (27 lessons):** HTML foundations → CSS styling → JavaScript interactivity → advanced controls
  - Build (HTML): My First Page, Cool Lists, Images & Links
  - Style (CSS): Paint Your Page, Game Cards, Animations
  - Power (JS): Click Power, Calculator, Monster Clicker
  - Controls: Slider Control, Joystick, Bar Chart, Gauge Meter, Toggle Switch, Checkbox Swarm, Drag & Drop, and more
- **Science (12 lessons):** Physics simulations and circuit building
  - Ohm's Law, Free Fall, Pendulum, Spring, Wave, Projectile, Buoyancy, Friction, Gas Law, Doppler, Lenses, Circuit Builder

**Learn Panel** — every lesson includes a kid-friendly explanation with highlighted key terms and a mini glossary of 2–3 new elements.

**Code Challenges** — optional "Can you…?" tasks per lesson with auto-checking and bonus XP (+15 XP).

**"Try This!" Suggestions** — after completing a lesson, three experiment ideas appear as clickable chips to encourage exploration.

**Step-by-Step Mode** (👣) — walks through code line-by-line, progressively building the preview so kids see what each line does.

**Auto-complete Tag Hints** — type `<` and get a dropdown of HTML tags with descriptions ("h1 = Big heading", "p = Paragraph").

**Error Helper** — kid-friendly error detection: "Oops! You opened `<div>` 2x but only closed it 1x. Add `</div>`!"

### Code Editor

- **Syntax highlighting** — single-pass tokenizer with theme-adaptive colors for tags, attributes, strings, keywords, CSS properties, numbers, and comments
- **Code beautifier** — auto-formats and indents lesson code on load with inline comments for beginners (`<!-- This tells the browser: "I am an HTML page!" -->`)
- **Line numbers** — scroll-synced, with active line accent color
- **Active line highlight** — current cursor line gets a visible accent background
- **Font size slider** — adjustable 10–22px for comfort
- **Tab support** — Tab key inserts 2 spaces

### Inspect Mode (🔍)

Toggle the magnifying glass button to activate a browser DevTools-like experience:

- **Result → Code:** Hover any element in the preview to highlight the matching code line with color-coded outlines
- **Code → Result:** Hover a code line to highlight the corresponding element in the preview
- **Click to Jump:** Click any element in the Result panel and the cursor jumps to that line in the editor
- **Breadcrumb Path:** Shows the element path (`body › div.card › h1`) when hovering
- **Color-coded Elements:** 8-color palette applied to elements, matching between both panels
- **CSS Property Linking:** Hovering a styled element highlights the relevant CSS property line in code

### Event Tracking (⚡)

Kids see cause and effect in real-time:

- **Event flash** — when a button is clicked or a slider is moved in the preview, the `onclick`/`oninput` handler line flashes yellow with a pulse animation
- **Event tooltip** — "⚡ onclick fired on \<button\>!" appears briefly near the preview
- **Event log** — collapsible panel below the RESULT header showing all triggered events with timestamps, element names, and details (e.g., `oninput <input> value=42`)

### Gamification

- **XP & Levels** — earn 25 XP per lesson, 15 XP per challenge. 10 levels from Newbie to Grandmaster
- **Streak counter** — fire emoji 🔥 pulses when streak ≥ 3
- **Confetti** — 80-particle physics-based celebration on lesson completion
- **9 Achievements** — First Code, High Five, Double Digits, Halfway Hero, Code Master, On Fire, Unstoppable, Basics Done, Scientist
- **Mascot buddy** (🤖) — fixed-position companion with contextual encouragement and tap interaction

### Multilingual

Three fully translated languages:

| Language | Code | Direction |
|----------|------|-----------|
| English  | EN   | LTR       |
| French   | FR   | LTR       |
| Arabic   | AR   | RTL       |

All UI labels, lesson titles, descriptions, hints, learn panels, glossaries, challenges, level names, and achievement text are translated.

### Themes

9 built-in themes with one-click switching:

| Theme | Style |
|-------|-------|
| 🌙 Stealth | Dark with green accents |
| ⚡ Neon | Deep blue with cyan/magenta |
| ☁️ Arctic | Light with blue accents |
| 🌲 Forest | Dark green nature tones |
| 🔥 Blaze | Dark with orange/yellow fire |
| 🍬 Candy | Pink/pastel playful |
| 🌊 Ocean | Deep blue marine |
| 🌸 Sakura | Soft pink Japanese spring |
| ⚙️ Cyber | Dark with lime green terminal |

Dark themes include an animated starfield background.

### Tools

- **Read Aloud** (🔊) — browser speech synthesis, language-aware (en-US, fr-FR, ar-SA)
- **Export** (💾) — download current code as a standalone `.html` file
- **Screenshot/Share** (📸) — export preview as shareable HTML
- **Parent Report Card** — modal showing lessons completed, XP, level, streak, and achievement progress per track

---

## Technical Architecture

### Single-File Design

Everything lives in one `index.html` file (~185KB, 1850 lines):

- **CSS** (~500 lines) — all styles inline in `<style>`, using CSS custom properties for theming
- **HTML** (~100 lines) — semantic structure: sidebar, main editor, preview, modals
- **JavaScript** (~1250 lines) — all logic in one `<script>` block

### Key Systems

| System | Approach |
|--------|----------|
| Theming | CSS variables swapped via JS (`document.documentElement.style.setProperty`) |
| Lessons | `mkI18N()` function returns nested object: `I18N[lang][track][idx].c` = code |
| Metadata | `META_EN/FR/AR` objects parallel to lessons: learn text, glossary, challenges, difficulty |
| Highlighting | Single-pass character tokenizer (no regex conflicts) |
| Preview interaction | `postMessage` between parent and sandboxed iframe |
| State | Simple variables: `lang`, `track`, `lessonIdx`, `completed{}`, `xp`, `level`, `streak` |
| Animations | `requestAnimationFrame` for confetti and starfield |

### Browser Compatibility

Tested on modern browsers (Chrome, Firefox, Safari, Edge). Requires:

- ES5+ JavaScript
- CSS Custom Properties
- `srcdoc` iframe attribute
- `postMessage` API
- `speechSynthesis` API (for read-aloud, gracefully degrades)

---

## File Structure

```
codekids-v4/
├── index.html    # The entire application (185KB)
├── logo.svg      # CodeKids logo
└── README.md     # This file
```

---

## Customization

### Adding a Lesson

1. Add the lesson code string to `mkI18N()` under the appropriate track and language
2. Add metadata to `META_EN` (and `META_FR`/`META_AR` if translating):
   ```javascript
   { learn: "Explanation with <b>bold</b> terms",
     gloss: [["<tag>", "What it does"]],
     challenge: "Can you...?",
     diff: 1,  // 1-3 stars
     check: function(code){ return code.indexOf('something') >= 0 } }
   ```
3. The lesson automatically appears in the sidebar

### Adding a Theme

Add an entry to the `TH` object:
```javascript
mytheme: {
  n: { en: "🎨 My Theme", fr: "🎨 Mon Thème", ar: "🎨 ثيمي" },
  v: { "--bg": "#...", "--accent": "#...", /* ... all CSS vars */ },
  stars: true  // animated starfield background
}
```

### Adding a Language

1. Add translations to `mkI18N()` for UI strings and lesson content
2. Add metadata translations to `META_XX`
3. Add `<option>` to the language `<select>` in HTML
4. Add level name translations to `LEVEL_NAMES`

---

## Roadmap Ideas

- Remix button (randomize colors/values in current lesson)
- Code sound effects (toggle on/off)
- Undo/Redo buttons
- Animated connector lines between code and result
- Peer sharing via QR codes
- Custom lesson builder for teachers

---

## License

Educational use. Built with ❤️ for young coders everywhere.
