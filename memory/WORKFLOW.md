# Pravidla sdílené práce pro Codex a Claude

Tento soubor popisuje, jak udržovat kontext při střídání mezi Codexem a Claudem.

## Start každé práce

Na začátku každého nového chatu nebo nové pracovní relace si asistent musí přečíst:

1. `CLAUDE.md` nebo `AGENTS.md`
2. `memory/CONTEXT.md`
3. `memory/DASHBOARD.md`
4. relevantní soubory v `memory/projects/`, pokud se řeší konkrétní projekt

Teprve potom má začít navrhovat nebo měnit aplikaci.

## Konec každé práce

Na konci každé relace musí asistent aktualizovat:

1. `memory/CONTEXT.md`
   - co se řešilo
   - co se změnilo
   - jaká rozhodnutí padla
   - jaké jsou další kroky

2. `memory/projects/<projekt>.md`, pokud se výrazně změnil stav konkrétního projektu.

3. `memory/DASHBOARD.md`, pokud se změnilo něco kolem dashboardu, dat, n8n migrace nebo aplikace.

## Jak zapisovat kontext

- Piš stručně, věcně a česky.
- Nové informace přidávej jako datované bloky.
- Neopisuj celé konverzace.
- U rozhodnutí uveď, kdo rozhodl nebo z čeho rozhodnutí vyplývá.
- U otevřených bodů piš jasně, na co se čeká.

## Co je zdroj pravdy

- `data.json` je aktuální historická datová vrstva starého dashboardu.
- `index.html` je aktuální vizuální reference starého dashboardu.
- n8n JSON exporty jsou reference původních automatizací.
- `memory/CONTEXT.md` je hlavní lidsky čitelná projektová paměť.
- `memory/DASHBOARD.md` je technická paměť dashboardu a budoucí aplikace.

## Pracovní režim

Uživatel může pracovat střídavě v Codexu a Claudu. Každý asistent se má chovat tak, jako by navazoval na živý projekt:

- nejdřív načíst paměť,
- pokračovat od posledního stavu,
- neptat se znovu na věci, které jsou už zapsané,
- na konci paměť aktualizovat.

## Krátká startovací instrukce pro nový chat

Pokud uživatel napíše: "pokračuj podle paměti", asistent má přečíst `memory/CONTEXT.md` a `memory/WORKFLOW.md` a pokračovat podle nich.
