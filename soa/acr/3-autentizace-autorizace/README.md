[Seminární práce](../../../README.md) / [Architektura orientovaná na služby](../../README.md) / ACR / [Rozhodnutí o autorizaci a autentizaci uživatelů](README.md)

# Rozhodnutí o autorizaci a autentizaci uživatelů

## ID
3

## Datum
11.1.2025

## Status
Schválené

## Context
Ze zadání plyne, že je požadována registrace a přihlašování uživatelů.

## Decision
Pro systém bude zvolen autentizační mechanismus OAuth 2.0, jehož pomocí bude aplikace obdržovat autentizační tokeny.

## Consequences
OAuth 2.0 poskytuje robustní bezpečnostní mechanismus, který minimalizuje riziko zneužití uživatelských přihlašovacích údajů. Uživatelé nebudou muset sdílet své heslo s aplikací, což výrazně snižuje pravděpodobnost úniku dat při zneužití aplikace nebo serveru.
