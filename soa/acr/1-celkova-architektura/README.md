[Seminární práce](../README.md) / [Architektura orientovaná na služby](README.md) / ACR / [Rozhodnutí o celkové architektuře systému](README.md)

# Rozhodnutí o celkové architektuře systému

## ID
1

## Datum
11.1.2025

## Status
Schválené

## Context
Je potřeba zvolit architekturu systému pro software sloužící k vyhledávání domácích mazlíčků.

## Decision
Pro systém bude využita architektura SOA (service oriented architecture) a pro komunikaci bude použit REST.

## Consequences
Systém bude rozdělen na samostatné služby, což umožní snadné přidávání nových funkcionalit. V plánu je další rozšiřování aplikace o další služby, proto je modularita a rozšířitelnost pro tuto aplikaci klíčová.
Díky kombinaci REST a SOA bude snadné integrovat externí systémy, jako jsou třeba reklamy, městské registry nebo geolokační systémy.
Jednotlivé služby se dají škálovat, což zajistí potřebný výkon při narůstajícím počtu uživatelů nebo například růst o další regiony.
Vzhledem k tomu, že je v této aplikaci klíčové, aby byli uživatelé aplikace spokojení, je vhodná vlastnost SOA, kdy oddělení funkcionalit do samostatných služeb usnadní údržbu a aktualizace systému, aniž by to ovlivnilo ostatní části aplikace.
Requesty a response budou v JSONu.
Jako nevýhoda tohoto řešení se může projevit komplexita a údržba, nebo cena návrhu.

[![Diagram architektury](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/assets/diagram-celkova-architektura/soa/SOA-global.png)](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/assets/diagram-celkova-architektura/soa/SOA-global.png)
