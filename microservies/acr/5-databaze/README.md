# Rozhodnutí o databázi aplikace 
## ID
5
## Datum
10.1.2025
## Status
Schválené 
## Context
Je potřeba zvolit vhodný typ databáze. Aplikace pro správu a hledání pohřešovaných domacích mazlíčků potřebuje efektivní správu různých typů dat: 
* **Strukturovaná data:** profily uživatelů, záznamy o mazličcích včetně parametrů, odměny
* **Geolokační data:** Ukládání a vyhledávání podle poslední aktualizované polohy mazlíčků
* **Nestrukturovaná data:** Komentáře
* **Multimediální obsah:** Fotografie mazlíčků

Byly zvažovany následující možnosti: 

Pro strukturovaná a geolokační data:
* PostgreSQL + PostGIS
* MySQL 
* MongoDB 
  
Pro uživatelské interakce a komentáře:
* MongoDB 
* PostgreSQL 

Pro multimediální obsah:
* Amazon S3 
* Google Cloud Storage

Pro správu a dočasné ukládání front notifikací: 
* Redis 
  
## Decision
Pro strukturovaná data bude použita relační databáze PostgreSQL. Tento typ databáze byl zvolen kvůli podpoře dobře definované datové struktury, transakčním vlastnostem (ACID) pro zajištění integrity dat a rozšíření PostGIS pro práci s geolokacemi.

Pro komentáře a dynamická data bude použita databáze MongoDB, což je NoSQL databáze. Tento typ databáze byl zvolen díky možnostem ukládat rychle se měnící data, rychlého čtění a snadnější horizontální škálovatelnosti. 

Pro fotografie bude použito cloudové objektové uložiště Amazon S3 z důvodu, že je to vysoce škalovatelné řešení a umožnuje snadnou integraci s dalšími službami. 

Pro správu notifikací bude použita databáze Redis. Tento typ dataváze je nejvíc vyhovující pro notifikace, protože umožňuje rychlý přístup k datum (in-memory) a zároveň odlehčuje jinou databázi tím, že podporuje ukládání často použivaných dat. 

## Consequences
Zvolené řešení MongoDB pro nestrukturovaná data eliminuje problémy se zpracováním velkého objemu nestrukturovaných dat. Nicméně nasazená a správa několika databází pro různé typy dat vyžaduje pozornost a pokročilé znalostí konfigurace. Rovněž je potřeba zajistit konzistenci mezi PostgreSQL a MongoDB. 
