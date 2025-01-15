[Seminární práce](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/README.md) / [Mikroservisní architektura](https://github.com/vojtechnerad/4IT575-seminarni-prace/edit/main/microservies/README.md)

# Mikroservisní architektura

## Dokumenty
1. [Rozhodnutí o celkové architektuře systému](./acr/1-celkova-architektura/README.md)
2. [Rozhodnutí o podobě rozšířené reality v systému](./acr/2-rozsirena-realita/README.md)
3. [Rozhodnutí o autorizaci a autentizaci uživatelů](./acr/3-autantizace-autorizace/README.md)
4. [Rozhodnutí o architektuře klientské aplikace](./acr/4-architektura-klient/README.md)
5. [Rozhodnutí o databázi aplikace](./acr/5-databaze/README.md)
6. [Rozhodnutí o infrastruktuře](./acr/6-infrastruktura/README.md)
7. [Rozhodnutí o vlastnostech systému](./acr/7-decisions/README.md)

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
