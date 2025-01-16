[Seminární práce](../README.md) / [Architektura orientovaná na služby](README.md) / ACR / [Rozhodnutí o vlastnostech systému](README.md)

# Rozhodnutí o vlastnostech systému

## ID
7

## Datum
12.1.2025

## Status
Schválené

## Context
Je potřeba blíže definovat některé explicitní požadavky.
Požadavky:
- Seznam pohřešovaných mazlíčků
- Možnost přidávat k jednotlivým mazlíčkům stavy (nalezeno, spatřeno,..)
- Přidávat fotodůkazy
- Reklamy od partnerů

## Decision
Chování systému podle výše zmíněných požadavků bylo navrhnuto následovně:

### Seznam pohřešovaných mazlíčků
- Každý uživatel může přidat pouze 10 mazlíčků do seznamu, tím se zabrání uživatelům, kteři by chtěli spamovat
- Ka každému mazlíčkovi půjde přidat 5 fotek mazlíčka
- Ke každému mazlíčkovi lze přidat popis a jméno mazlíčka
- Seznam se ve výchozím stavu bude zobrazat od nejnovějšího po nejstarší
- Seznam lze filtrovat, buď podle textového řetězce nebo "vlastností" zvířete - rasa, barva, jméno

### Možnost přidávat k jednotlivým mazlíčkům stavy (nalezeno, spatřeno,..)
- Každý uživatel má možnost nahlásit nalezení nebo spatření mazlíčka
- U každého mazlíčka může uživatel dát stav "nelezen" pouze jednou a to s fotodůkazem
- U každého mazlíčka může uživatel vybrat stav "spatřeno", ale jen jednou za 10 minut
- Po vybrání stavu spatřeno/nalezen může vystavitel inzerátu kontaktovat uživatele, který zvolil stav

### Přidávat fotodůkazy
- Každý uživatel může k mazlíčkům přidávat fotodůkazy, maximálně ale 5 fotek

### Reklamy od partnerů
- Každý páty příspěvek bude obsahovat reklamu od partnera
- Každý příspěvek mazlíčka bude mít jako poslední fotku reklamu od partnera
