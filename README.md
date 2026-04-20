# Arnie's Day Trading Setup Playbook

MES & M2K 2-minute scalping playbook with inline plain-English teaching explanations for every concept and SVG illustrations for every rule.

## What's in here

- `index.html` — the full single-file app (v3.0 — seven setups plus three workflow tools)
- `netlify.toml` — Netlify build/deploy config
- Pure HTML + CSS + vanilla JS. No build step. No dependencies beyond Google Fonts (loaded at runtime) and Firebase compat SDK (loaded at runtime).

## Seven setups

1. **Double Bottom** — reversal · quality scoring · red-flags · discipline gate
2. **Double Top** — reversal · same scoring + red-flags framework
3. **Bull Flag** — continuation · entry methods · stop methods · measured-move targets
4. **Bear Flag** — continuation · "faster and more violent" caveat · same framework
5. **Failed Breakout Reversal** — trap reversal · highest-edge setup · 60-65% win rate
6. **Opening Range Breakout with Retest (ORB-R)** — session breakout · max one per day
7. **VWAP Mean Reversion with RSI** — range play · midday only · 55-60% win rate

## Three workflow tools

- **Clock Matrix** — which setup to hunt based on time of day EST
- **Pre-Trade Decision Tree** — four yes/no questions, any NO = skip
- **Pre-Trade Checklist** — printable, interactive, tick-box with full market context / setup / volume / risk / mental state review

## Plus

- Unified Principles — 8-point cross-pattern reference
- Visual Masterclass — 20 illustrated lessons reinforcing pattern trading
- Trade journal with pattern tagging, localStorage persistence, and CSV export
- Four Principles discipline framework (Thunderstorm · Casino · Ambien · Calm State)
- Firebase Google Sign-In gate

## Local development

Just open `index.html` in a browser. No server required. For hot-reload during development, use the included `serve-dtb-teaching.js` static server on port 3478.

## Deployment

Connected to Netlify via GitHub auto-deploy. Any push to `master` triggers a rebuild.

Live site: https://arnie-double-top-bottom.netlify.app

## Author

A. Shapiro, MD — Arnie's Day Trading Setup Playbook · MES & M2K · v3.0
