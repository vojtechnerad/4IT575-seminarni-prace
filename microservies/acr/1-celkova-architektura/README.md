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
Pro systém bude využita architektura mikroservis a pro komunikaci bude použit REST.

## Consequences
Systém bude navržen tak, že jednotlivé funkce budou rozděleny do samostatných mikroservis.
Toto řešení umožní vysokou flexibilitu a snadné přidávání nebo upravování konkrétních částí aplikace bez zásahu do ostatních.
Díky této modularitě a nezávislosti je aplikace připravena na budoucí rozšiřování, například o nové funkce spojené s rozšířenou realitou.

Mikroservisy mezi sebou budou komunikovat pomocí REST API a data budou přenášena ve formátu JSON.
Takto navržená architektura umožňuje snadnou integraci s externími systémy, jako jsou například geolokační nástroje, reklamní platformy nebo analytické systémy.
Tato flexibilita zvyšuje šance na budoucí spolupráci s dalšími partnery a rozšiřuje možnosti monetizace.

Velkou výhodou mikroservis je jejich nezávislé škálování.
To znamená, že pokud dojde k výraznému nárůstu uživatelů nebo hlášení, lze škálovat pouze tu část systému, která je nejvíce zatížena, například mikroservisu spravující záznamy o pohřešovaných zvířatech.
Ostatní části aplikace zůstanou beze změny, což výrazně šetří zdroje.

Další přínos spočívá v jednodušší údržbě a aktualizacích.
Díky oddělení jednotlivých funkcí mohou být změny prováděny jen v příslušné mikroservise, aniž by došlo k výpadkům nebo problémům v jiných částech systému.
Tímto způsobem lze zlepšit stabilitu aplikace a zvýšit spokojenost uživatelů.

Na druhou stranu má tento přístup i své nevýhody.
Mikroservisní architektura je složitější na návrh i správu, což znamená vyšší nároky na orchestraci a monitorování jednotlivých částí systému.
Zároveň může být počáteční implementace časově i finančně náročnější, což je třeba vzít v úvahu při plánování projektu.
