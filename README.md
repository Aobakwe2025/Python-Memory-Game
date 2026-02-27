# 🐍 Python Memory Puzzle Game - SoftGrowTech

> A browser-based card-matching game that teaches Python fun facts while racing against the clock.

![Python Memory Game](https://img.shields.io/badge/Python-Memory%20Game-FFD43B?style=for-the-badge&logo=python&logoColor=306998)
![HTML5](https://img.shields.io/badge/HTML5-Single%20File-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-4CAF50?style=for-the-badge)

---

## 🎮 Overview

**Python Memory Puzzle** is a fully self-contained, single-file HTML game where players flip cards to find matching pairs — all themed around the Python programming language. Every matched pair rewards you with a real Python fun fact, making it a fun way to learn while you play.

Built with a cyberpunk aesthetic: dark background, neon accents, CSS 3D card flips, confetti bursts, and a live HUD — no frameworks, no dependencies, just pure HTML/CSS/JavaScript.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🃏 **16 Cards / 8 Pairs** | Python-themed: Guido van Rossum, Duck Typing, Lambda Functions, List Comprehensions, PIP, Zen of Python, Garbage Collector, Python Logo |
| 💡 **Fun Facts Panel** | Each matched pair reveals a real Python fact |
| ⏱️ **Timer & Scoring** | Live countdown with score bonuses for speed |
| ⭐ **Star Ratings** | 1–3 stars based on move efficiency |
| 🎚️ **3 Difficulty Levels** | Easy (60s), Medium (45s), Hard (30s) |
| 🎉 **Confetti Animations** | Burst on each match, shower on victory |
| 📊 **Live HUD** | Real-time time, score, moves, and progress bar |
| 🎨 **Cyberpunk Design** | Python blue/yellow + neon cyan/pink/purple palette |

---

## 🚀 Getting Started

### Play Instantly

No installation required. Just open the file in any modern browser:

```bash
# Download and open
open python-memory-game.html

# Or serve locally
python -m http.server 8000
# Then visit http://localhost:8000/python-memory-game.html
```

### Requirements

- Any modern browser (Chrome, Firefox, Safari, Edge)
- No internet connection required after initial load (Google Fonts are fetched once)
- No build tools, no npm, no dependencies

---

## 🕹️ How to Play

1. **Choose a difficulty** — Easy, Medium, or Hard
2. Click **▶ Start Game** to begin the countdown
3. Click any card to flip it and reveal the Python concept
4. Click a second card to try to find its match
5. Matched pairs stay face-up and reveal a **Python fun fact**
6. Unmatched pairs flip back — remember their positions!
7. Match all **8 pairs** before the timer hits zero to win

### Scoring

| Action | Points |
|---|---|
| Each matched pair | 100 + (time remaining × 2) |
| Victory time bonus | time remaining × 10 |

### Star Ratings

| Moves | Stars |
|---|---|
| ≤ 12 moves | ⭐⭐⭐ Perfect |
| ≤ 18 moves | ⭐⭐ Great |
| 19+ moves | ⭐ Good effort |

---

## 🐍 Python Concepts Covered

The game features 8 core Python concepts, each with a fun fact:

1. **Guido van Rossum** — Python's creator and the origin of its name
2. **Python Logo** — The two snakes and Python's global popularity
3. **The Zen of Python** — The `import this` Easter egg and Tim Peters' aphorisms
4. **Duck Typing** — Python's dynamic type system explained
5. **Lambda Functions** — Anonymous functions and functional programming
6. **PIP Package Manager** — PyPI's 500,000+ packages
7. **List Comprehensions** — Pythonic one-liner syntax
8. **Garbage Collector** — Python's automatic memory management

---

## 🗂️ File Structure

```
python-memory-game.html    ← Entire game in one file
README.md                  ← This file
```

The entire game is a single HTML file (~400 lines) containing:

- **HTML** — Game structure, modals, HUD
- **CSS** — Cyberpunk theming, 3D card flip animations, grid layout
- **JavaScript** — Game logic, state management, timer, scoring

---

## 🎨 Design Decisions

- **Dark cyberpunk theme** chosen to feel engaging and modern, inspired by Python's vibrant community
- **CSS `rotateY` 3D transforms** for smooth card flips without JavaScript libraries
- **`perspective` on the card container** for a realistic 3D effect
- **CSS Grid** for the responsive card layout
- **`backface-visibility: hidden`** to hide card backs when showing fronts
- **Confetti** built with dynamically generated `div` elements and CSS `@keyframes`

---

## 🛠️ Customisation

### Add New Card Pairs

Edit the `CARDS_DATA` array in the `<script>` section:

```javascript
{ 
  id: 'decorators',          // Unique ID (must match your pair)
  emoji: '@',                // Display emoji or character
  label: 'Decorators',       // Card label
  color: '#FF6B6B',          // Card accent colour
  borderColor: '#FF6B6B',    // Card border colour
  fact: 'Python decorators wrap functions to modify behaviour...'
}
```

### Change Difficulty Timers

```javascript
const DIFFICULTY = { easy: 60, medium: 45, hard: 30 };
// Change the values (in seconds) to your liking
```

### Adjust Grid Columns

```css
#grid {
  grid-template-columns: repeat(4, 1fr); /* Change 4 to your preferred column count */
}
```

---

## 📄 License

This project is open source and free to use, modify, and distribute. Perfect for classrooms, coding bootcamps, portfolio projects, or just learning Python facts the fun way.

---

## 🙌 Acknowledgements

- Python facts sourced from the official [Python documentation](https://docs.python.org) and community resources
- Fonts: [Fira Code](https://fonts.google.com/specimen/Fira+Code) & [Space Mono](https://fonts.google.com/specimen/Space+Mono) via Google Fonts
- Built with ❤️ and 🐍 — no snake was harmed in the making of this game
