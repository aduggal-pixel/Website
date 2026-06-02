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
    ├── quoridor.html — local two-player Quoridor (move pawn / place walls)
    ├── tictactoe.html
    └── presets.js    — puzzle data for Sudoku
```

Each game page has a "← Home" link back to `index.html` (a styled link in the
page header).

Future sections (e.g. `investing/`) will be added as top-level folders with
their own `index.html`, linked from the homepage.

## Homepage (index.html)

A professional landing page with a navy (`#0c1f3f`) / gold (`#c9a256`) palette:

- **Header** — "1729 Global" / "An Investment & Advisory Firm".
- **Investing** section (badged "Coming Soon") — three cards:
  Weekly Market Commentary, Compensation Analysis, Investment Case Studies.
- **A Fun Intellectual Break** section — cards linking to the four games.
- Navy footer.

Self-contained HTML/CSS (no icons/emojis — intentionally text-only and clean).

## Game pages (design)

All four game pages share a polished brand template (applied across the games):

- Scaled-down "1729 Global / An Investment & Advisory Firm" navy header with a
  gold bottom-border and a styled `← Home` link (`.home-link`, top-right).
- Brand CSS variables in `:root` — `--navy #0c1f3f`, `--navy2 #172d56`,
  `--gold #c9a256`, `--white`, `--text #2d3748`, `--muted #718096`,
  `--border #e2e8f0`, `--shadow 0 2px 14px rgba(0,0,0,.07)`.
- A white `.panel` card (1px border, 14px radius, soft shadow) wrapping the game.
- Buttons: navy background, gold-on-hover (text navy), ~8px radius.
- System font stack; `clamp()` for responsive sizing.

`quoridor.html` and `chess.html` are the most polished references for this look.

## Planned / not-yet-done

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
serves at **www.1729global.com**. Workflow: cut a fresh feature branch from the
latest `main` → commit in small steps → push → open a PR into `main` →
squash-merge. Delete the feature branch once merged. The live site updates a
minute or two after a merge to `main`. Do not edit or remove the `CNAME` file
(it binds the custom domain).
