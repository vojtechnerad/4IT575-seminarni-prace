[Seminární práce](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/README.md) / [Mikroservisní architektura](https://github.com/vojtechnerad/4IT575-seminarni-prace/edit/main/microservies/README.md)

# Mikroservisní architektura

## Rozhodnutí
1. [Celková architektura](./acr/1-celkova-architektura/README.md)
2. [Rozšířená realita](./acr/2-rozsirena-realita/README.md)

## Důvody
- **Vysoká modularita**: Každá klíčová funce bude tvořena separátně jako samostatná služba - uživatelské účty, záznamy o pohřešovaných zvířatech, virtuální realita.

## Návrh architektury

## Dokumentace

## Přehled výhod a nevýhod využití mikroservisní architektury

### Výhody
- **Možnost budoucího rozšiřování**: Mikroservisní architektura umožňuje jednoduší rozšíření celé aplikace, ať už ve formě přidání nové mikroservisy, či úpravy stávající. Tato vlastnost může být pro mateřskou společnost užitečná, pokud bude plánovat integraci některých nově vyvíjených služeb rozšířené reality přímo do aplikace. 

### Nevýhody
- **Vyšší provozní náklady**
  - **Více nasazení**: Každá mikroservisa vyžaduje vlastní běhové prostředí (například kontejner nebo virtuální stroj). To zvyšuje náklady na cloudové zdroje.
  - **Monitoring**: Pro každou mikroservisu je nutné nastavit logování, monitorování a alerty, což může zvýšit provozní náklady.
