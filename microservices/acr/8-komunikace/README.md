# Rozhodnutí o komunikaci mezi jednotlivými komponenty aplikace
## ID
8
## Datum
10.1.2025
## Status
Schválené 
## Context
V aplikaci, která slouží hlavně k evidenci a hledání ztracených domacích mazlíčků je potřeba zajistit spolehlivou a efektivní komunikaci mezi mikroslužbami (Uživatele, Evidence mazlíčků, Komentáře a interakce, Odměny, Notifikace, Mapy, AR, Media) a také mezi backendem a frontendovými klienty (web, mobil). V návrhu architektury byly zvažovany následující možnosti, jak můžeme komunikaci pro tento případ řešit:

* **REST API:** pro synchronní volání
* **Event-driven:** pro asynchronní komunikaci
* **gRPC:** pro výkonnější komunikaci uvnitř backendu
  
## Decision
Primárně pro komunikaci mezi klientem (frontend) a backendem bude využit REST API (HTTP, JSON).

Asynchronní event-driven přístup (Kafka) bude využit u scénářů, kde chceme volnou vazbu, zpracování událostí a odeslání notifikací (Notifikační služba dostane od služby Evidence mazlíčků událost přes Kafku → na základě toho proběhne informování přirazeného majitele mazlíčka e-mailem nebo push notifikací: “Váš mazlíček byl zřejmě nalezen.”).

## Consequences
Zvolené řešení REST API je  široce podporované a snadno integrovatelné s webovými i mobilními aplikacemi. Co se týče Event-driven přístupu, tak ten zjednodušuje odeslání notifikací a aktualizaci dat, což pro případ této aplikace je vhodné. Avšak použití a provoz více komunikačních stylů, v tomto případě REST a eventů,vyžaduje promyšlené řízení a dohled v podobě monitoringu a loggingu.
