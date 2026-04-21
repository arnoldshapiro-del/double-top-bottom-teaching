# Arnie's Day Trading Setup Playbook — UNIFIED

## Project Name
Arnie's Day Trading Setup Playbook — v4.0 Unified (MES · M2K · RTY · 2-min scalping)
The merged successor to three previous apps — Double Top/Bottom teaching playbook (this repo, the base), Arnie's Edge System, and Arnie's Trading Academy. Merged April 20, 2026.

## Purpose
A single unified 2-minute futures scalping program covering the full workflow in four sidebar sections:
- **LEARN** — 7 setup patterns + Aggressive Entry + Unified Principles + Visual Masterclass + Pattern Quiz + Calculators + Flashcards
- **TRADE** — Four Principles State Gate + Pre-Market Prep + Clock Matrix + Decision Tree + 24-item Checklist + 6-Box Live Checklist + Daily Gates
- **REVIEW** — Trade Journal + Edge Dashboard
- **THE PLAN** — 🧠 The Research Behind the Plan + 🏆 Final Trading Plan (added 2026-04-21)

## GitHub Repo
`arnoldshapiro-del/double-top-bottom-teaching` (master branch)
Branches 1-11 of the unified merge were all merged to master sequentially (Apr 20, 2026).

## Netlify Site URL
https://arnie-double-top-bottom.netlify.app

## Tech Stack
- Pure HTML + CSS + Vanilla JavaScript
- No build step. Single-file `index.html` (~9,000 lines after unified merge)
- Google Fonts + Firebase compat SDK v10.14.1 at runtime
- PWA: `manifest.json` in root
- Firebase Google Auth locked to `arnold.shapiro@gmail.com`

## Current Status
**v4.2 THE PLAN illustration pass (2026-04-21).** 16 inline SVG figures added across Research + Final Plan tabs. Matches existing visual language.
**v4.1 THE PLAN section added (2026-04-21).** Purely additive — no existing sections modified.
**v4.0 Unified LIVE (2026-04-20).** All 11 merge branches shipped in one session.

The three predecessor apps remain live as safety nets during the transition period:
- Edge System: https://arnies-edge-system.netlify.app (still live)
- Trading Academy: https://arnie-trading-academy.netlify.app (still live)

Per the master plan (`C:\Users\arnol\Desktop\MERGE-MASTER-PLAN.md`), Arnie decides
whether to archive / leave running / take down after verifying the unified app meets his needs.

**Uni's TA Bootcamp (unis-ta-bootcamp-day1.netlify.app) stays SEPARATE — do not touch it.**

## localStorage schema (playbook_ namespace — Branch 6)
All data keys now namespaced under `playbook_`. Legacy keys (`arnie_m2k_trades_v1`, `state`, `blockedAt`, `premarket_*`, `fc_stats`) preserved non-destructively as safety net.
- `playbook_trades` — trade objects array
- `playbook_state` — `{ name, at }` from State Gate (4-hour persistence)
- `playbook_blockedAt` — `{ state, at }` when non-Calm selected
- `playbook_premarket_YYYY-MM-DD` — per-date pre-market plan
- `playbook_fc_stats` — `{ correct, total }` flashcard accuracy
- `playbook_theme` — `dark` | `light`
- `playbook_migrated_v1` — migration sentinel

## Features by branch
- **B1** — Unified nav: LEARN / TRADE / REVIEW sidebar + light-mode toggle
- **B2** — Four Principles State Gate + 60-sec breath timer (replaces old always-visible Four Principles)
- **B3** — Pre-Market Prep form (PDH/PDL/ONH/ONL/bias/setups/econ/mood/intent)
- **B4** — 6-Box Live Checklist with GO/MARGINAL/PASS banner
- **B5** — Daily Gates: max 3 trades · 2-loss lock · 11:30-13:30 lunch lock
- **B6** — Journal merge: 10-chip mistake tagging + localStorage namespace migration
- **B7** — Edge Dashboard: win-rate by pattern/emotion/session/adherence/direction + mistake tag frequencies
- **B8** — Pattern Quiz: 41 Canvas-rendered scenarios (true + false DBs and DTs)
- **B9** — Calculators: tick converter · position sizer · R:R · P&L scenarios (M2K/MES/RTY)
- **B10** — Flashcard Trainer: 6 deliberate-practice cards with inline SVG
- **B11** — Final polish: SEO, metadata, README, CLAUDE.md, SESSION_NOTES
- **B12** — Red Flags moved from always-visible top panel to its own first-position TRADE tab (🚩 Red Flags — No Trade). Every other tab now opens clean at the top
- **B13** — Layout: container max-width 1400→1800px; body font 13→14px; line-height 1.5→1.55; padding 24px→20px 28px
- **B14** — Sidebar: height fills full viewport (calc(100vh-32px)); flex-column; theme toggle pinned to bottom via margin-top:auto
- **B15** — TTS read-aloud engine: browser Web Speech API (same as Uni's TA Bootcamp); teal 🔊 "Read this lesson" button + reading-time estimate on 14 tabs; sentence-queue pattern; floating pause/stop/speed control bar; auto-stops on tab switch; persists rate in `playbook_tts_rate`
- **B16** — THE PLAN section (2026-04-21): new 4th sidebar section below REVIEW with gold 🏁 header. Two tabs:
  - `tab-research-plan` (🧠 The Research Behind the Plan) — 9-part scholarly document with sticky TOC navigation and "back to top" links; covers DB research, wick-vs-body neckline decision, "15 seconds left" dilemma, buy stops/entry mechanics, stop placement breakthrough, DT/Bull Flag/Bear Flag research, and unified research principles. TTS-enabled.
  - `tab-final-plan` (🏆 Final Trading Plan) — LIVE TRADING REFERENCE checklist styled distinctly from the rest of the app. 4 pattern cards (DB/DT/BF/BEF) with numbered step cards, color-coded by pattern (green/red/green/red). 10 Universal Rules in a prominent gold box. Quick Reference table. Two Mindset Trap callouts. Mobile-responsive for phone viewing next to trading computer.

## Design system
- Dark mode default · light mode toggle in sidebar (persisted in `playbook_theme`)
- Left sidebar nav with 3 labeled sections (LEARN / TRADE / REVIEW)
- Color accents:
  - Teal `#14b8a6` — Calm state · flashcards
  - Orange `#fb923c` — Aggressive Entry · Pre-Market Prep
  - Violet `#c4b5fd` — Clock Matrix / Decision Tree / Checklist · Review
  - Blue `#60a5fa` — Calculators
  - Gold `#e6b859` — Pattern Quiz · Neckline annotations
  - Red `#ef4444` — Daily Gates · Thunderstorm state · Failure zones
- Typography: JetBrains Mono (body) · Fraunces (headings)

## File Structure
```
/
├── index.html       — Full single-file app (~9000 lines after unified merge)
├── manifest.json    — PWA manifest
├── netlify.toml     — Netlify publish config
├── README.md        — Repo readme
├── CLAUDE.md        — This file
└── SESSION_NOTES.md — Session history
```

## Firebase Integration (unchanged since v3.1)
- Firebase Project ID: `double-top-bottom-teach`
- Auth: Google Sign-In, locked to `arnold.shapiro@gmail.com`
- Firestore: Enabled
- Netlify domain authorized: `arnie-double-top-bottom.netlify.app`

## Project-Specific Rules
- Deploy via GitHub push → Netlify auto-builds
- Never Vercel CLI
- Every branch merged to master sequentially (no parallel merges)
- localStorage keys MUST stay in `playbook_` namespace going forward
- Three predecessor apps (Edge System, Trading Academy) stay live until Arnie decides their fate
- Uni's TA Bootcamp is separate — NEVER merge it in

## Known Issues / Bugs
None at v4.0 ship. State Gate breath animation can cause preview screenshot timeouts during testing but does not affect users.
