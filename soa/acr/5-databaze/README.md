[Seminární práce](../../../README.md) / [Architektura orientovaná na služby](../../README.md) / ACR / [Rozhodnutí o databázi aplikace](README.md)

# Rozhodnutí o databázi aplikace

## ID
5

## Datum
12.1.2025

## Status
Schválené

## Context
Je nutné vybrat typ databáze. Je zvažována relační nebo NoSQL databáze.

## Decision
Bude použita relační databáze PostgreSQL. Tento typ databáze byl zvolen kvůli podpoře dobře definované datové struktury, transakčním vlastnostem (ACID) pro zajištění integrity dat a rozšíření PostGIS pro práci s geolokacemi.

## Consequences
Použití PostgreSQL zajistí vysokou integritu dat díky transakčním vlastnostem (ACID), efektivní práci s geolokačními daty díky rozšíření PostGIS a širokou podporu pro pokročilé dotazy. Databáze umožňuje škálování a je bezplatná, což snižuje náklady. Změny ve struktuře dat mohou být náročné na správu a výkon při zpracování velkého objemu nestrukturovaných dat, jako jsou příspěvky nebo komentáře, může být omezen, což si v budoucnu může vyžádat zavedení NoSQL databáze.
