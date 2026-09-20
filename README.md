# Threads

A small, minimal puzzle game for the browser. Connect each pair of matching colored dots with a single line — every cell on the board has to be covered to solve it.

No build step, no dependencies. It's one self-contained HTML file.

## Play

Open `index.html` in any browser, or visit the live version on GitHub Pages once it's deployed (see below).

**How to play**
- Drag from a colored dot to its matching dot.
- The line can only move up, down, left, or right — no diagonals, no crossing another color.
- A puzzle is solved once every color is connected *and* every cell on the board is filled.

**Controls**
- **Undo** — removes your last move.
- **Hint** — reveals the solution for one pair you haven't connected yet.
- **Reset** — clears the current puzzle and starts it over.
- 🔈 / 🔊 (top right) — toggles sound effects.

There are 6 puzzles, from a 5×5 board up to an 8×8 board. Solving one unlocks the next, and your progress, best move count, and best time per puzzle are all saved in your browser.

## Running locally

Just open the HTML file — no server or install required:

```bash
open index.html      # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

## Deploying to GitHub Pages

1. Push this repo to GitHub (make sure the game file is named `index.html`).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, pick the `main` branch and `/ (root)` folder, then Save.
4. After a minute or two, your game will be live at `https://<your-username>.github.io/<repo-name>/`.

## Tech

Plain HTML, CSS, and JavaScript — no frameworks or build tools. Puzzle paths render as SVG, game state is a small in-memory grid, and progress persists via `localStorage`.
