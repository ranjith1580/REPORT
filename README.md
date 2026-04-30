# NIFTY CPR Extreme Levels 7–10 Dashboard

Interactive analytics dashboard for NIFTY 50 Central Pivot Range (CPR) extreme level breaches (S7–S10, R7–R10) from January 2000 to April 2026.

## Live Demo

**Deployed via GitHub Pages:** `https://<your-username>.github.io/nifty-cpr-dashboard`

## Features

- **40 ultra-rare breach events** across 26 years of data
- **6 interactive tabs:** Overview · Breach Log · Event Cards · Drill-down · VIX Analysis · Yearly
- **Multi-select filters** — Level, Direction, Breach Type, Day of Week
- **Breach type detection** — Gap Open vs Intraday vs Close Only
- **Market event context** — known events annotated on each breach date
- **Day-of-week analysis** — which day sees most extreme moves
- **Drill-down** — dates where multiple levels breached simultaneously
- **VIX correlation** — India VIX at each breach event
- **CSV export** for filtered breach data
- **Zero dependencies** — single HTML file, works offline

## Levels Covered

| Level | Type | Formula |
|-------|------|---------|
| S7 | Bearish Support | L − 7×(H − Pivot) |
| S8 | Bearish Support | L − 8×(H − Pivot) |
| S9 | Bearish Support | L − 9×(H − Pivot) |
| S10 | Bearish Support | L − 10×(H − Pivot) |
| R7 | Bullish Resistance | H + 7×(Pivot − L) |
| R8 | Bullish Resistance | H + 8×(Pivot − L) |
| R9 | Bullish Resistance | H + 9×(Pivot − L) |
| R10 | Bullish Resistance | H + 10×(Pivot − L) |

## CPR Formulas

```
Pivot = (Previous High + Previous Low + Previous Close) / 3
BC    = (Previous High + Previous Low) / 2
TC    = (Pivot − BC) + Pivot
```

## Data Sources

- NIFTY 50 daily OHLC: Jan 2000 – Apr 2026
- India VIX daily: Mar 2009 – Apr 2026

## Deploy to GitHub Pages

```bash
# 1. Fork or clone this repo
git clone https://github.com/<your-username>/nifty-cpr-dashboard.git
cd nifty-cpr-dashboard

# 2. Enable GitHub Pages in repo Settings
#    → Pages → Source → Deploy from branch → main → / (root)

# 3. Your site will be live at:
#    https://<your-username>.github.io/nifty-cpr-dashboard
```

## Local Usage

Just open `index.html` in any browser — no server needed.

## Tech Stack

- Vanilla HTML + CSS + JavaScript (no framework)
- Chart.js 4.4.1 (CDN)
- Apple-standard design system (SF Pro, system fonts)
