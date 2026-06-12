# Technický kontext: Dashboard 400K SJL

---

## Architektura

- **Typ:** statická HTML stránka (vše v jednom souboru)
- **GitHub:** https://github.com/jiranekvaclav/400K-SJL-MREG1
- **Soubory:**
  - `index.html` — celý dashboard (HTML + JS + CSS v jednom)
  - `data.json` — datový soubor
  - `transcripts/` — přepisy schůzek
  - `hynek.png` — obrázek

## Co dashboard zobrazuje

- 4 KPI ukazatele s trendem (týdenní sparkline grafy):
  - Kvalita dodávek
  - Kvalita expedice
  - Produktivita CZLC4 (SJL/hod)
  - Produktivita LCU (SJL/hod)
- Přehled projektů — filtrovatelná mřížka, statusy on-track / at-risk / off-track / on-hold
- Projektové karty — milníky, historie, přiřazený PM
- Program brief — shrnutí aktuálních výzev

## Integrace

- **Cloudflare:** chat webhook v dashboardu
- **n8n:** automatizace (workflow)
- **Data:** aktuálně hardcoded v HTML, plánovaná změna na dynamická data přes n8n

## Historie změn

| Datum | Změna |
|---|---|
| 2026-06-12 | Vytvoření paměťové struktury |

## Plánované změny

- (doplnit)
