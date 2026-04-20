# Arnie's Day Trading Setup Playbook — Unified v4.0

The complete 2-minute scalping workflow for **MES · M2K · RTY** futures in a single app.
**LEARN · TRADE · REVIEW** — organized as a three-part sidebar.

Merged from three predecessor apps (April 2026):
- *Double Top / Double Bottom teaching playbook* (this repo, became the base)
- *Arnie's Edge System* (discipline workflow — state gate, pre-market, daily gates, dashboard)
- *Arnie's Trading Academy* (pattern quiz, calculators)

## Live
https://arnie-double-top-bottom.netlify.app

## What's in here
- `index.html` — the full single-file app (~9000 lines, all HTML + CSS + vanilla JS inline)
- `manifest.json` — PWA manifest
- `netlify.toml` — Netlify publish config (no build step)
- Pure HTML + CSS + vanilla JS. Google Fonts + Firebase compat SDK loaded at runtime.

## LEARN — Before the market opens
1. **Double Bottom** — reversal · quality scoring · red-flags
2. **Double Top** — reversal · same framework
3. **Bull Flag** — continuation · entry + stop methods · measured-move
4. **Bear Flag** — continuation · "faster and more violent" caveat
5. **Failed Breakout Reversal** — trap reversal · 60-65% WR
6. **ORB Retest** — session breakout · max one per day
7. **VWAP Mean Reversion with RSI** — midday range play
8. **Aggressive Entry** — 5-gate framework for entering before candle close
9. **Unified Principles** — 8 cross-pattern rules
10. **Visual Masterclass** — 20 lessons
11. **Pattern Quiz** — Canvas-rendered TRUE/FALSE recognition drill
12. **Calculators** — tick converter · position sizer · R:R · P&L scenarios
13. **Flashcard Trainer** — 6 deliberate-practice cards

## TRADE — Live execution
1. **🧘 Four Principles State Gate** — Calm/Thunderstorm/Casino/Ambien with 60-sec breath timer
2. **📋 Pre-Market Prep** — date-stamped plan (PDH/PDL/ONH/ONL/bias/setups/econ/mood/intent)
3. **🕐 Clock Matrix** — session-by-session time-of-day guide
4. **🌳 Decision Tree** — 4 yes/no gates with live GO/SKIP verdict
5. **✅ 24-Item Pre-Trade Checklist** — interactive tick-boxes across 5 sections
6. **🎚️ 6-Box Live Checklist** — Level · MACD · Stoch · Trigger · Volume · Time with live GO/MARGINAL/PASS
7. **🔒 Daily Gates** — Max 3 trades · 2-loss lock · 11:30–13:30 ET lunch lock

## REVIEW — After market closes
1. **📝 Trade Journal** — full-field log with pattern dropdown, 10-chip mistake tagging, emotion, plan adherence, notes
2. **📈 Edge Dashboard** — win-rate by pattern / emotion / session / adherence / direction + mistake tag frequency

## Firebase auth gate
Locked to `arnold.shapiro@gmail.com` only. Non-Arnie Google accounts are denied at the front-door overlay.

## localStorage schema (playbook_ namespace)
- `playbook_trades` — trade objects array
- `playbook_state` — `{ name, at }` from State Gate (4-hour persistence)
- `playbook_blockedAt` — `{ state, at }` when non-Calm selected
- `playbook_premarket_YYYY-MM-DD` — per-date pre-market plan
- `playbook_fc_stats` — `{ correct, total }` flashcard accuracy
- `playbook_theme` — `dark` | `light`
- `playbook_migrated_v1` — migration sentinel (set once)

Legacy keys (`arnie_m2k_trades_v1`, `state`, `blockedAt`, `premarket_*`, `fc_stats`)
are preserved as a non-destructive safety net.

## Tech stack
- Single-file HTML · CSS · vanilla JS
- No build step
- Firebase compat SDK v10.14.1 (auth + Firestore) injected at runtime
- PWA: manifest.json + apple-mobile-web-app tags
- Google Fonts: JetBrains Mono + Fraunces

## Design
- Dark mode default with light-mode toggle (sidebar, persisted)
- Left sidebar navigation with three labeled sections (LEARN / TRADE / REVIEW)
- Color accents: teal (Calm state), orange (Aggressive Entry · Pre-Market Prep),
  violet (workflow tools · Review), blue (calculators), gold (quiz)
- JetBrains Mono for body, Fraunces for display type
- Responsive: sidebar stacks above main content below 900px

## Deploy
Push to GitHub — Netlify auto-builds.
