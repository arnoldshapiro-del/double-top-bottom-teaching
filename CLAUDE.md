# Trading Double Bottoms and Double Tops, and Bull Flags and Bear Flags

## Project Name
Trading Double Bottoms and Double Tops, and Bull Flags and Bear Flags — Teaching Edition v2.0
(Formerly "Double Top / Double Bottom — M2K 2-Min Scalping Reference")

## Purpose
A single-file HTML trading reference app for M2K and MES 2-minute scalping. Covers four chart patterns — Double Top, Double Bottom, Bull Flag, Bear Flag — with inline plain-English teaching explanations for every concept. Also includes a Unified Principles reference tab that ties all four patterns together with 8 cross-pattern rules. Has quality scoring (0–5), red-flags panel, Four Principles discipline gate, trade journal with localStorage persistence, and CSV export.

## GitHub Repo
`arnoldshapiro-del/double-top-bottom-teaching` (branch: `feature/add-flags-and-tops` for Phase 1, merges to `master`)

## Netlify Site URL
https://arnie-double-top-bottom.netlify.app

## Tech Stack
- Pure HTML + CSS + Vanilla JavaScript
- No build step, no dependencies beyond Google Fonts (runtime CDN)
- Single file: `index.html` (~2700 lines after v2.0 expansion)
- Local dev server: `C:\Users\arnol\Desktop\serve-dtb-teaching.js` (port 3478, launched via `.claude/launch.json` config "dtb-teaching")

## Current Status
Phase 1 v2.0 complete on branch `feature/add-flags-and-tops` — awaiting Arnie's merge approval

## Features Completed (v1.x)
- Double Top + Double Bottom checklists with quality scoring (0–5)
- Red-flags panel
- Final "Four Principles" discipline gate
- Trade journal with localStorage persistence
- CSV export
- Print-friendly layout (landscape, Letter)
- Plain-English teaching explanations under every concept

## Features Completed (v2.0 — Phase 1, 2026-04-15)
- **App renamed** to "Trading Double Bottoms and Double Tops, and Bull Flags and Bear Flags" (title, H1, subtitle, footer, README, SEO meta tags)
- **Tab navigation system** — 5 tabs (Double Bottom default, Double Top, Bull Flag, Bear Flag, Unified Principles). CSS `order` property keeps Double Bottom first visually even though HTML source has Short/Double-Top column first
- **Bull Flag tab built from scratch** — 7 sections: precision definition, anatomy, four entry methods (candle-close above breakout, break entry, pullback to 20-EMA, stochastic cross reversal), three stop-loss methods (below flag low, below 20-EMA, Fibonacci-based), M2K vs MES comparison, professional workflow, Arnie's 6-point personal approach
- **Bear Flag tab built from scratch** — 9 sections including the critical "Bear Flags Are Faster and More Violent" callout, long-term upward market bias considerations, four entry methods, three stop-loss methods, M2K vs MES comparison, pro workflow, Arnie's 7-point approach
- **Unified Principles tab** — 8 numbered cross-pattern rules (confirmation trumps prediction, risk before reward, 61.8% Fib invalidation, trend alignment, measured-move targets, volume confirmation, higher-timeframe filter, emotional discipline) plus a cross-reference map that shows where each principle applies across the four patterns
- **Print-friendly** — print media query shows all tab panels sequentially with `page-break-after: always` so physical printouts cover all four patterns
- **SEO meta tags** — title, description, keywords added to `<head>`
- **No regressions** — all existing scoring, journal, CSV export, and Four Principles gate preserved

## Features Planned / Next (v2.1 — Phase 2)
- Enrich existing Double Bottom and Double Top sections with additional entry methods from the reference doc (currently they only have their original short checklists)
- Add "Pattern" dropdown to trade journal so entries can be tagged by pattern (DB / DT / BullFlag / BearFlag)

## Known Issues / Bugs
None

## Important Decisions
- Kept single-file HTML stack (did NOT migrate to Vite+React+TS+Tailwind even though the task prompt assumed that stack)
- Kept repo name `double-top-bottom-teaching` (did not rename)
- Branch off `master` (repo has no `main`)
- Tab navigation (not sidebar) to preserve existing card-based layout
- Cover both M2K AND MES (not M2K-only)
- Reference doc content added as NEW sections — did not replace existing checklists
- Bull/Bear Flag called out the voice-dictation fidelity note ("Bow Flags and Bare Flags") and used correct "Bull/Bear" wording

## File Structure
```
/
├── index.html       — Full single-file app (~2700 lines, v2.0)
├── netlify.toml     — Netlify config (publish from root, no build)
├── README.md        — Repo readme (updated v2.0)
├── CLAUDE.md        — This file
└── SESSION_NOTES.md — Session history
```

## Project-Specific Rules
- Always deploy via GitHub push → Netlify auto-builds
- When reference document says "incorporate ALL content in full" — do not summarize or trim
