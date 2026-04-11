# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A static landing page for HearthPlay Games, hosted on GitHub Pages at `hearthplaygames.com`. The entire site is a single self-contained file: `index.html`.

## Architecture

No build step, no framework, no dependencies. Everything — HTML, CSS, and any future JS — lives in `index.html`. Fonts are loaded from Google Fonts (Playfair Display + Source Serif 4).

**Design tokens** are defined as CSS custom properties at `:root` (`:12–27`): amber, brick, charcoal, cream, and warm-white. Use these variables for any new color usage rather than hardcoding hex values.

**Layout sections** (in order):
- Fixed nav
- `.hero` — full-viewport hero with floating dice background element
- `.app-section` (dark) — HearthRoll feature section with dice showcase grid
- `.values-section` — 3-column values grid
- `footer`

## Deploying

Push to `main`. GitHub Pages serves `index.html` from the repo root automatically.

## Key constraints

- Accessibility is a core value of the brand. Maintain ARIA labels, `aria-hidden` on decorative elements, `:focus-visible` styles, and `prefers-reduced-motion` support when making changes.
- Keep the single-file architecture — do not introduce a build system or split into multiple files unless explicitly asked.
