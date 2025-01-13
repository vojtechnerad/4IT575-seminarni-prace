# Rozhodnutí o infrastruktuře

## ID

6

## Datum

12.1.2025

## Status

Schválené

## Context

Systém je potřeba někde provozovat.

## Decision

Vzhledem k povaze aplikace je potřeba dbát na výkonnost, dostupnost, agilnost, škálovatelnost,.. Z tohoto důvodu bylo rozhodnuto systém provozovat v cloud řešení.
Pro nasazení bude využita platforma AWS (Amazon Web Services) s nasazením klíčových komponent v rámci služeb, které umožní splnění požadavků na výkon, flexibilitu a bezpečnost. 

## Consequences

Nasazení na AWS umožní flexibilní škálování aplikace v závislosti na aktuálním zatížení, vysokou dostupnost díky geografické redundanci. Správa infrastruktury bude zjednodušena díky využití služeb s řízeným provozem, což eliminuje potřebu ruční správy serverů. Na druhou stranu je využití AWS spojeno s měsíčními provozními náklady, které porostou s rozšířením uživatelské základny a objemu dat. Toto řešení je však připraveno na budoucí expanzi a umožní soustředit se na vývoj aplikace namísto provozní podpory.