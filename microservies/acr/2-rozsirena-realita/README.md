[Seminární práce](../../../README.md) / [Mikroservisní architektura](../../README.md) / ACR / [Rozšířená realita](README.md)

# Rozhodnutí o podobě rozšířené reality v systému

## ID

2

## Datum

11.1.2025

## Status

Schválené

## Context

V zadání je požadavek pro přidání možnosti rozšířené reality. 

## Decision

Pro systém bude využita služba pro rozšířenou realitu od mateřské služby, která tuto službu právě spouští. Ta bude oddělena jako samostatný modul, který bude napojen na hlavní aplikaci.

## Consequences

Rozhodnutí využít službu pro rozšířenou realitu od mateřské organizace přináší rychlou implementaci a snížení nákladů na vývoj, protože není nutné vytvářet vlastní řešení. Toto řešení zároveň zajišťuje vysokou škálovatelnost a usnadňuje udržování aktuálnosti funkcionality. Na druhou stranu přináší závislost na externí službě, což může ovlivnit systém při výpadcích, změnách podmínek nebo zdražení služby. Celkově jde o efektivní řešení pro rychlé nasazení, ale vyžaduje průběžné sledování spolehlivosti a dostupnosti služby.
