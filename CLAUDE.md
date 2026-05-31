# CLAUDE.md

Project context for Claude Code. Read this first.

## What this is

A personal website for the domain **1729global.com**, hosted on **GitHub Pages**
(a static host — plain HTML/CSS/JS, no backend yet). It currently holds a small
collection of browser games. Over time it will grow into a multi-section site
(e.g. a games section and an investing section) with a proper home page, and may
later gain backend-powered features.

## Structure (current)

The repo is currently flat (all files in the root):

- `index.html` — Tic-Tac-Toe game (also the site's landing page for now)
- `tictactoe.html` — duplicate of `index.html` (cleanup candidate)
- `sudoku.html` — Sudoku game
- `sudoku-test.html` — mobile-optimised Sudoku variant (work in progress)
- `presets.js` — puzzle data used by the Sudoku pages
- `chess.html` — local two-player chess (uses the chess.js library)

A future task is to reorganise into folders (e.g. `games/`, `investing/`) with a
real home page at `index.html` linking to each section.

## Conventions

- Each game is a single self-contained `.html` file: HTML structure, a `<style>`
  block, and a `<script>` block in one file. Keep this simple style.
- Plain vanilla JavaScript — no build step, no framework.
- External libraries are loaded via CDN `<script>` tags (e.g. chess.js).
- Prefer clear, beginner-friendly code and comments; the owner is learning.

## Running / testing

No build step. Open any `.html` file directly in a browser to run it. The live
site updates when changes are merged to the publishing branch and pushed.
