# Europe — Interactive Economic Map Dashboard (2000–2025)

**Professional-grade map-centric dashboard** covering 45 European economies with 9 switchable map overlays, a 26-year animated timeline, interactive country popups with sparkline charts, and a comprehensive data sidebar — all in a single self-contained HTML file.

## Features

- **🗺️ Interactive Leaflet Map** — Full-viewport dark-themed map with CARTO dark tiles, circle markers sized by GDP and colored by the selected metric
- **⏱️ 26-Year Animated Timeline** — Play/pause animation through 2000–2025 with keyboard controls and a year slider
- **9 Switchable Map Overlays** — Toggle between GDP, GDP Growth, GDP/Capita, Population, Inflation, Unemployment, FDI Inflow, Government Debt, and Trade Balance
- **Rich Country Popups** — Click any country for a detailed popup with all 9 economic indicators, EU/eurozone badges, and a GDP trajectory sparkline chart (2000–2025)
- **Collapsible Sidebar** — 350px overlay panel with:
  - 4 KPI cards (Combined GDP, Avg Growth, FDI, Inflation)
  - 9 metric pill selectors
  - Year timeline slider with play/pause
  - 8 region filter chips
  - Interactive horizontal bar chart (Chart.js) comparing top 12 countries
  - Searchable, sortable country list with EU/eurozone badges
- **Animated Fly-To** — Click any country in the sidebar to fly the map to it and auto-open its popup
- **Legend** — Dynamic gradient legend that updates with the selected metric and year
- **Fullscreen Mode** — Built-in fullscreen control for presentations
- **Keyboard Shortcuts** — `←` `→` for year navigation, `Space` for play/pause, `B` to toggle sidebar
- **Region Filtering** — Filter by Western Europe, Southern Europe, Northern Europe, Eastern Europe, Western Balkans, Eastern Partnership, Caucasus, or Russia & Turkey
- **Bottom Info Bar** — EU membership stats, current region, and data sources
- **Responsive** — Adapts to mobile, tablet, and desktop

## Data Coverage

| Indicator | Countries | Range |
|-----------|-----------|-------|
| GDP (USD bn) | 45 | 2000–2025 |
| GDP Growth (%) | 45 | 2000–2025 |
| GDP per Capita (USD) | 45 | 2000–2025 |
| Population (M) | 45 | 2000–2025 |
| Inflation (%) | 45 | 2000–2025 |
| Unemployment (%) | 45 | 2000–2025 |
| FDI Inflow (USD bn) | 45 | 2000–2025 |
| Government Debt (% GDP) | 45 | 2000–2025 |
| Trade Balance (USD bn) | 45 | 2000–2025 |

## Regions Covered

| Region | Countries |
|--------|-----------|
| Western Europe | 🇩🇪 Germany · 🇫🇷 France · 🇬🇧 UK · 🇳🇱 Netherlands · 🇧🇪 Belgium · 🇨🇭 Switzerland · 🇦🇹 Austria · 🇮🇪 Ireland · 🇱🇺 Luxembourg |
| Southern Europe | 🇮🇹 Italy · 🇪🇸 Spain · 🇵🇹 Portugal · 🇬🇷 Greece · 🇲🇹 Malta · 🇨🇾 Cyprus |
| Northern Europe | 🇸🇪 Sweden · 🇩🇰 Denmark · 🇫🇮 Finland · 🇳🇴 Norway · 🇮🇸 Iceland |
| Eastern Europe | 🇵🇱 Poland · 🇨🇿 Czech Republic · 🇭🇺 Hungary · 🇷🇴 Romania · 🇧🇬 Bulgaria · 🇸🇰 Slovakia · 🇱🇹 Lithuania · 🇱🇻 Latvia · 🇪🇪 Estonia · 🇸🇮 Slovenia · 🇭🇷 Croatia |
| Western Balkans | 🇷🇸 Serbia · 🇧🇦 Bosnia & Herz. · 🇲🇪 Montenegro · 🇲🇰 North Macedonia · 🇦🇱 Albania · 🇽🇰 Kosovo |
| Eastern Partnership | 🇺🇦 Ukraine · 🇲🇩 Moldova · 🇧🇾 Belarus |
| Caucasus | 🇬🇪 Georgia · 🇦🇲 Armenia · 🇦🇿 Azerbaijan |
| Russia & Turkey | 🇷🇺 Russia · 🇹🇷 Turkey |

## Tech Stack

- **Leaflet.js 1.9.4** — Interactive map with Canvas rendering
- **Chart.js 4.4.7** — Sidebar comparison bar chart
- **Vanilla HTML/CSS/JS** — Zero build step, zero dependencies beyond CDN scripts
- **Dark professional theme** — H Heuristics design system
- **Self-contained** — All economic data (65KB, 45 countries × 26 years × 9 indicators) embedded directly in the HTML

## Deployment

This is a **fully static single-file site** — deploy anywhere:

```bash
# GitHub Pages — push to main branch, enable Pages in repo settings
# Cloudflare Pages
wrangler pages deploy .

# Or any static host: Netlify, Vercel, S3
# Local: python3 -m http.server 8080
```

## GitHub Pages Setup

1. Push this repo to GitHub
2. GitHub Actions will auto-deploy via the included `.github/workflows/pages.yml`
3. Your dashboard will be live at `https://hunterhghs.github.io/Europe-Economic-Map/`

## Project Structure

```
Europe-Economic-Map/
├── index.html              # Main dashboard (self-contained, ~112KB)
├── data/
│   └── europe_economy.json # Full economic dataset (170KB pretty-printed)
├── build_data.py           # Python script to regenerate/update data
├── .github/
│   └── workflows/
│       └── pages.yml       # GitHub Pages auto-deployment
└── README.md
```

## License

MIT — Built for [H Heuristics](https://hheuristics.substack.com)

---

*Data compiled from IMF World Economic Outlook (April 2025), World Bank, and Eurostat patterns. Last updated July 2025.*
