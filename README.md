# Semestrální práce
Tento repozitář obsahuje řešení semestrální práce z předmětu `4IT575 Softwarové architektury`.

## Řešitelé
- Brázda Jan
- Kozlova Olesia
- Nerad Vojtěch

## Odkazy
- [Microservices](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/microservies/README.md)
- [SOA](https://github.com/vojtechnerad/4IT575-seminarni-prace/blob/main/soa/README.md)

## Zadání
Původní znění zadání semestrální práce.

### Popis aplikace
Služba věnující se pohřešovaným domácím mazlíčkům. Služba nabízí popis pohřešovaných zvířat, jejich nálezů a údaje o místech, kde se dané zvířátko pohybovalo. Služba také využívá rozšířenou realitu k zobrazení místa, kde byl mazlíček spatřen naposledy.

Uživatelé: desítky majitelů pohřešovaných domácích mazlíčků, stovky "pozorovatelů" (zpočátku), v závislosti na úspěchu zavádění širší okruh uživatelů.

### Požadavky
- Uživatelé, kteří mají zájem o nalezení domácích mazlíčků, se zaregistrují na webu.
- Kdokoli si může prohlédnout seznam pohřešovaných domácích mazlíčků v blízkosti místa kde se pohybuje.
- Nálezci domácích mazlíčků mohou zveřejňovat zprávy "nalezeno" (s povinným důkazem v podobě fotografie) a po potvrzení od majitelů domácích mazlíčků sbírat odměny.
- Uživatelé mohou komentovat záznamy o pohřešovaných domácích mazlíčcích a nabízet údaje (spatřeno, zkontrolovaná oblast bez výsledku atd.)
- Dostupnost pro mobilní zařízení.

### Další souvislosti
- Jedna z řady služeb rozšířené reality, které spouští mateřská společnost.
- Místní škálovatelnost (na město), ale případně i rozšíření do dalších měst.
- Společnost chce vytvořit větší sociální komunitu kolem domácích zvířat.
- Potenciální příjmy z reklamy od partnerů, jako jsou obchody s domácími zvířaty, mají potenciál vydělat statisíce.
