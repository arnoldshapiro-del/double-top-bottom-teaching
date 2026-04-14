# Double Top / Bottom Teaching Edition

## Project Name
Double Top / Bottom Teaching Edition (M2K Scalping Reference)

## Purpose
A single-file HTML trading reference app for M2K 2-minute scalping. Covers double top and double bottom chart patterns with inline plain-English teaching explanations for every concept. Includes quality scoring (0–5), red-flags panel, Four Principles discipline gate, trade journal with localStorage persistence, and CSV export.

## GitHub Repo
`arnoldshapiro-del/double-top-bottom-teaching`

## Netlify Site URL
TBD — set during initial deployment session (2026-04-14)

## Tech Stack
- Pure HTML + CSS + Vanilla JavaScript
- No build step, no dependencies beyond Google Fonts (runtime CDN)
- Single file: `index.html`

## Current Status
Active — newly deployed 2026-04-14

## Features Completed
- Double Top + Double Bottom checklists with quality scoring (0–5)
- Red-flags panel
- Final "Four Principles" discipline gate
- Trade journal with localStorage persistence
- CSV export
- Print-friendly layout (landscape, Letter)
- Plain-English teaching explanations under every concept

## Features In Progress
None

## Features Planned / Next
None noted

## Known Issues / Bugs
None

## Important Decisions
- index.html is the canonical production file — identical to double-top-bottom-teaching-edition.html
- No build step needed — plain HTML deployed directly from root
- Repo name: double-top-bottom-teaching

## File Structure
```
/
├── index.html       — Full single-file app (~92 KB)
├── netlify.toml     — Netlify config (publish from root, no build)
├── README.md        — Repo readme
├── CLAUDE.md        — This file
└── SESSION_NOTES.md — Session history
```

## Project-Specific Rules
- Do NOT modify index.html without Arnie's explicit approval — it is a finished artifact
- Always deploy via GitHub push → Netlify auto-builds
