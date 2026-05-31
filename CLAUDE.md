# CLAUDE.md

Project context for Claude Code. Read this first.

## What this is

A personal website for the domain **1729global.com**, hosted on **GitHub Pages**
(a static host — plain HTML/CSS/JS, no backend yet). It currently holds a small
collection of browser games. Over time it will grow into a multi-section site
(e.g. a games section and an investing section) with a proper home page, and may
later gain backend-powered features.

## Structure (current)

```
Website/
├── index.html        — professional homepage (1729 Global brand + section links)
├── CNAME             — custom domain: www.1729global.com
├── CLAUDE.md
├── README.md
└── games/
    ├── chess.html    — local two-player chess (chess.js library)
    ├── sudoku.html   — Sudoku game (uses presets.js)
    ├── tictactoe.html
    └── presets.js    — puzzle data for Sudoku
```

Future sections (e.g. `investing/`) will be added as top-level folders with
their own `index.html`, linked from the homepage.

## Conventions

- Each game is a single self-contained `.html` file: HTML structure, a `<style>`
  block, and a `<script>` block in one file. Keep this simple style.
- Plain vanilla JavaScript — no build step, no framework.
- External libraries are loaded via CDN `<script>` tags (e.g. chess.js).
- Prefer clear, beginner-friendly code and comments; the owner is learning.

## Running / testing

No build step. Open any `.html` file directly in a browser to run it. The live
site updates when changes are merged to the publishing branch and pushed.
