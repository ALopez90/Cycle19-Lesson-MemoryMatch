# Memory Match

Lightweight, beginner-friendly **Memory Match** built with **HTML, CSS, and JavaScript**.

Goal: teach DOM manipulation, basic state handling, and event-driven logic.

---

## What You’ll Build

- A 4×3 grid of cards
- Click to flip → compare → match or unflip  
- Turn counter, reset button, and a simple “You win!” message  
- Clean, modern look with light animations

---

## Tools & Setup

**You’ll Need:**
- **VS Code** (recommended editor)
  - Extension: `Live Server` (for instant browser preview)
  - Optional: `Prettier` (auto-formatting)
- **Modern Browser:** Chrome, Edge, or Firefox
- *(Optional)* **Git** for version tracking or sharing work

**Project Folder Structure**
```
memory-match/
├── index.html
├── style.css
├── app.js
└── assets/   # optional (if you use images instead of emoji)
```

---

## 🚀 Quick Start

1. **Download or Clone**
   ```bash
   git clone https://github.com/your-org/memory-match-mini.git
   cd memory-match-mini
   ```

2. **Open in VS Code** → Right-click `index.html` → “Open with Live Server”

3. **If Live Server is missing**
   Go to **VS Code → Extensions → Search “Live Server” → Install** → Try again.

4. The app should open automatically in your browser at something like:
   ```
   http://127.0.0.1:5500/
   ```

---

## How It Works

- **Data:** an array of 6 emojis duplicated into 12 cards.
- **Shuffle:** Fisher–Yates algorithm randomizes card order each game.
- **Render:** JS dynamically creates `<button>` cards and attaches click events.
- **State:** tracks `firstCard`, `secondCard`, `lockBoard`, `turns`, and `matches`.
- **Logic Flow:**
  1. First flip → store reference.
  2. Second flip → compare icons.
  3. Match → lock as “matched”.
  4. No match → briefly lock board, then unflip both.

---

## 🧠 Mini Checkpoints

| # | Checkpoint | Expected Outcome |
|---|-------------|------------------|
| 1 | Grid renders | 12 cards visible in a grid |
| 2 | Card flips | Clicking rotates a card |
| 3 | Match logic | Pairs stay flipped |
| 4 | Counter works | Turns increase after each comparison |
| 5 | Win condition | Message shows when all matches found |

---

## Quiz!

**Q1:** Why do we duplicate the emoji array before shuffling?
**Q2:** What does `lockBoard` prevent during the flip delay?
**Q3:** What’s the difference between `textContent` and `innerHTML`?
**Q4:** How could you add difficulty levels without breaking existing logic?

---

## Troubleshooting

| Problem | Likely Fix |
|----------|-------------|
| Cards won’t flip | Check `.card` gets `.flipped` and `.card-inner` rotates via CSS |
| Matches never trigger | Compare `firstCard.dataset.icon === secondCard.dataset.icon` |
| Win never shows | Increment `matches` properly and check `matches === icons.length` |
| All cards identical | Confirm shuffle runs before rendering (`deck = shuffle([...icons,...icons])`) |

---

## Challenges

- Add **difficulty levels** (more cards or time limits)
- Include a **timer** or “best score” using `localStorage`
- Add **theme switching** (emoji → image mode)
- Display a small **confetti effect** on win
- Add **sound effects** for flips or matches

---

## 🧾 Credits & License

This project is free for **educational and internal training** use.
Attribution appreciated if you remix or share externally.
