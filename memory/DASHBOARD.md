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
- **GitHub CLI:** nainstalován, napojený na repozitář jiranekvaclav/400K-SJL-MREG1
- **Repozitář naklonován:** `~/Documents/400K-SJL-MREG1`

## n8n Webhooky

| Workflow | URL | Spuštění |
|---|---|---|
| WF1 - Master Dashboard | `https://n8n.dev.gcp.alza.cz/webhook/f5014ea1-ca4b-4562-b921-0c1a70de7f89` | POST |
| WF2 - Zpracování přepisů | `https://n8n.dev.gcp.alza.cz/webhook/90e0b07d-641d-4f12-b650-144d45c1a4f9` | POST |
| WF3 - Chat Hynek | Cloudflare webhook (vždy aktivní) | automaticky |

## Historie změn

| Datum | Změna |
|---|---|
| 2026-06-12 | Vytvoření paměťové struktury |

## Plánované změny

- (doplnit)
