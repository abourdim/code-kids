# 🚀 CodeKids — Learn to Code Like a Superhero!

A fun, kid-friendly interactive coding platform inspired by [W3Schools](https://www.w3schools.com/), designed for children aged 7–14. Kids learn HTML, CSS, and JavaScript through hands-on missions with a live code editor and instant preview.

![CodeKids](https://img.shields.io/badge/CodeKids-v1.0-blue?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![Languages](https://img.shields.io/badge/languages-EN%20|%20FR%20|%20AR-orange?style=for-the-badge)

---

## ✨ Features

### 🌍 3 Languages
- **English** — Full interface + lessons
- **Français** — Full interface + lessons
- **العربية** — Full RTL support + lessons

### 🎨 8 Themes
| Theme | Vibe |
|---|---|
| 🚀 Space Commander | Deep space with animated starfield |
| 🥷 Ninja Dojo | Dark & red combat aesthetic |
| 🌊 Ocean Explorer | Deep sea blues |
| 🐉 Dragon Quest | Purple & fire gradients with stars |
| 🤖 Cyber Hacker | Green-on-black Matrix style |
| 🏔️ Arctic Mission | Crisp light theme |
| 🌋 Volcano Base | Molten reds & oranges |
| 🌴 Jungle Safari | Deep green wilderness |

### 📚 9 Missions per Language (27 total)
Organized into 3 categories:

**🏗️ Build It (HTML)**
1. My First Page — basic HTML tags
2. Cool Lists — ordered & unordered lists
3. Images & Links — media and navigation

**🎨 Style It (CSS)**
4. Paint Your Page — colors & text-shadow
5. Game Cards — gradients, shadows, hover effects
6. Animations — keyframes, spin, bounce, rainbow

**⚡ Power It (JS)**
7. Click Power — buttons, alerts, events
8. Calculator — inputs, functions, DOM
9. Monster Clicker — a full mini-game

### 🛠️ Editor Features
- **Live code editor** with syntax-colored text
- **Instant preview** via sandboxed iframe
- **Tab key support** (inserts 2 spaces)
- **Hint system** — every lesson has a hint
- **Reset button** — encourages experimentation
- **Star progress** — tracks completed lessons
- **Responsive** — works on desktop, tablet, and mobile

---

## 🚀 Getting Started

### Option 1: Just Open It
```
Double-click index.html
```
That's it. No build tools, no npm, no server required. It's a single HTML file.

### Option 2: Local Server (optional)
```bash
# Python
python -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```
Then open `http://localhost:8000` in your browser.

---

## 📁 Project Structure

```
codekids/
├── index.html    ← The entire app (HTML + CSS + JS)
└── README.md     ← This file
```

Everything lives in a single `index.html` file — no dependencies, no build step, no external frameworks. Just open and go.

---

## 🎯 How It Works

1. **Pick a language** from the sidebar dropdown
2. **Pick a theme** to customize the look
3. **Select a mission** from the sidebar
4. **Read the code** in the editor (left panel)
5. **Click Launch** to see it run (right panel)
6. **Edit the code** — experiment and break things!
7. **Use Hint** if you get stuck
8. **Use Reset** to start over — no fear!
9. **Earn stars** for each mission you complete

---

## 🧰 Tech Stack

| What | How |
|---|---|
| HTML5 | Semantic structure |
| CSS3 | Custom properties, gradients, animations, backdrop-filter |
| Vanilla JS | No frameworks — just plain JavaScript |
| Google Fonts | Fredoka (display), Fira Code (mono), Noto Sans Arabic (RTL) |
| Canvas API | Animated starfield background |

---

## 🌐 Browser Support

- Chrome 90+
- Firefox 90+
- Safari 15+
- Edge 90+

---

## 🤝 Contributing

Want to add more lessons, themes, or languages? Here's how:

### Add a New Theme
In the `THEMES` object, add a new entry with `name`, `vars` (CSS custom properties), `icon`, and `stars` (boolean).

### Add a New Language
In the `I18N` object, add a new language key with `dir`, all UI strings, `cats` (category labels), and a `lessons` array matching the structure of existing languages.

### Add a New Lesson
Add an object to the `lessons` array in each language with:
- `cat` — category (`html`, `css`, or `js`)
- `t` — title
- `d` — description
- `h` — hint text
- `c` — starter code (full HTML document)

---

## 📄 License

MIT — free to use, modify, and share.

---

Built with ❤️ for the next generation of coders.
