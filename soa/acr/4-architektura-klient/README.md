# Rozhodnutí o architektuře klientské aplikace

## ID

4

## Datum

11.1.2025

## Status

Schválené

## Context

Ze zadání vyplývá, že je potřeba zajistit vyvážení mezi funkcionalitou, uživatelským komfortem a výkonem, a to jak pro mobilní zařízení, tak pro web.

## Decision

Navrhovaná architektura bude vycházet z modulárního přístupu, který umožňuje flexibilitu, rozšiřitelnost a jednoduchou údržbu.

## Consequences

Aplikace bude rozdělena do následujících vrstev:

- Prezenční vrsta
  - Technologie React a React Native, které v určité míře umožňují sdílení kódu mezi platformami
  - Komponenty budou navrženy modulárně, aby bylo snadné přidávat nové funkce (např. zeď s příspěvky uživatelů nebo rozhraní pro AR)
- Aplikační vrstva (Business Logic Layer)
  - State management bude realizován pomocí nástrojů jako Redux
- Komunikační vrstva
  - Knihovna Axios
- Datová vrstva (Data Storage Layer)
  - Pro cacheování dat bude použiy localStorage pro web nebo AsyncStorage.

- [Zpět na rozpis ACR](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/soa/acr/README.md)