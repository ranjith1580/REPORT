# NIFTY CPR Extreme Levels 7–10 Dashboard

Interactive analytics dashboard for NIFTY 50 Central Pivot Range (CPR) extreme level breaches — S7 through S10 and R7 through R10 — covering January 2000 to April 2026.

## Live Demo

**GitHub Pages:** `https://<your-username>.github.io/<repo-name>/`

## What's Inside

### 9 Interactive Tabs

| Tab | Description |
|-----|-------------|
| Overview | KPIs, level cards, frequency charts, insights |
| Unique Breaches | One card per date — multi-level days grouped, expandable |
| All Records | Full 40 breach records with multi-select filters + CSV export |
| Drill-down | Dates ranked by number of levels breached simultaneously |
| VIX Analysis | NIFTY close chart with breach markers, VIX trends |
| Yearly | Annual stacked bar chart + table |
| Probability | Live checkbox filter — success rate updates in real time |
| Scenarios | 9 pre-defined exclusion scenarios compared side by side |
| DOW Analysis | Level × Day-of-Week heatmap, VIX bucket analysis |

### Key Stats (Jan 2000 – Apr 2026)

- **6,552 CPR trading days** analysed
- **40 level-breach records** across **20 unique dates**
- **10 multi-level days** (2+ levels breached same day)
- **Baseline success rate: 99.69%** (probability of no extreme breach)
- Excluding Mondays → **99.81%** success rate

### Levels Covered

| Level | Type | Formula |
|-------|------|---------|
| S7 | Bearish Support | L − 7 × (H − Pivot) |
| S8 | Bearish Support | L − 8 × (H − Pivot) |
| S9 | Bearish Support | L − 9 × (H − Pivot) |
| S10 | Bearish Support | L − 10 × (H − Pivot) |
| R7 | Bullish Resistance | H + 7 × (Pivot − L) |
| R8 | Bullish Resistance | H + 8 × (Pivot − L) |
| R9 | Bullish Resistance | H + 9 × (Pivot − L) |
| R10 | Bullish Resistance | H + 10 × (Pivot − L) |

### CPR Formulas

```
Pivot  = (Previous High + Previous Low + Previous Close) / 3
BC     = (Previous High + Previous Low) / 2
TC     = (Pivot − BC) + Pivot
```

All calculations use **previous day's OHLC** shifted forward.

### Exclusion Scenarios (Probability Tab)

| Scenario | Days | Success Rate |
|----------|------|-------------|
| All Days (Baseline) | 6,552 | 99.69% |
| Exclude Mondays | 5,239 | 99.81% |
| Exclude Election Result Days | 6,546 | 99.73% |
| Exclude Mon + Election Results | 5,234 | 99.83% |
| Exclude Mon + Election + Budget | 5,221 | 99.83% |

## Deploy to GitHub Pages

```bash
# 1. Create a new PUBLIC repo on github.com

# 2. Push this folder
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main

# 3. Settings → Pages → Branch: main → Folder: / (root) → Save

# 4. Live in ~60 seconds at:
#    https://YOUR_USERNAME.github.io/YOUR_REPO/
```

## Local Usage

Just open `index.html` in any browser — no server, no dependencies, works offline.

## Tech Stack

- Vanilla HTML + CSS + JavaScript (no framework, no build step)
- Chart.js 4.4.1 (CDN)
- Apple-standard design system
- Single self-contained file
