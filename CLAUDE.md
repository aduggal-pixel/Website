# CLAUDE.md

Project context for Claude Code. Read this first.

## What this is

A personal website for the domain **1729global.com**, hosted on **GitHub Pages**
(a static host — plain HTML/CSS/JS, no backend yet).

**1729 Global** is an investment and advisory firm. The website doubles as the
owner's test environment for AI-assisted projects: a `games/` section holds
browser games used to experiment with build tools, and an investing-focused set
of sections is planned (see below). It may later gain backend-powered features.

The owner has limited recent coding experience and is learning — prefer clear,
beginner-friendly code, plain explanations, and small reviewable steps.

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

Each game page has a fixed "← Home" link back to `index.html`.

Future sections (e.g. `investing/`) will be added as top-level folders with
their own `index.html`, linked from the homepage.

## Homepage (index.html)

A professional landing page with a navy (`#0c1f3f`) / gold (`#c9a256`) palette:

- **Header** — "1729 Global" / "An Investment & Advisory Firm".
- **Investing** section (badged "Coming Soon") — three cards:
  Weekly Market Commentary, Compensation Analysis, Investment Case Studies.
- **A Fun Intellectual Break** section — cards linking to the three games.
- Navy footer.

Self-contained HTML/CSS (no icons/emojis — intentionally text-only and clean).

## Planned / not-yet-done

- Refine homepage layout (more polished, professional spacing/styling).
- Improve the games pages' formatting to look cleaner and more professional
  (they are functional but visually basic).
- Add cross-links between game pages (each game links to the others), not just
  the existing "← Home" link.
- Build out the investing sections, starting with **Compensation Analysis**
  (board & executive compensation of public companies). Likely a new
  `investing/` folder. Best done in a fresh session.

## Conventions

- Each game is a single self-contained `.html` file: HTML structure, a `<style>`
  block, and a `<script>` block in one file. Keep this simple style.
- Plain vanilla JavaScript — no build step, no framework.
- External libraries are loaded via CDN `<script>` tags (e.g. chess.js).
- Prefer clear, beginner-friendly code and comments; the owner is learning.

## Running / testing / deploying

No build step. Open any `.html` file directly in a browser to run it.

The live site is published from the **`main`** branch via GitHub Pages and
serves at **www.1729global.com**. Workflow: develop on a feature branch →
commit → push → open a PR into `main` → merge. The live site updates a minute
or two after a merge to `main`. Do not edit or remove the `CNAME` file (it binds
the custom domain).
