# zda-sem
ZDA-sem


# Projekt pro predmet Zaklkady Datovych Analyz


## Situation:
Jako milovnik sachu mam velky zajem o nejlepsi strtegii a nejproduktivnejsi kombinace, Rozhodl jsem se odpovedet na otazku "jak spravne zacit hru?"

## Task:
Pouzit data z databaze online sachovnici www.lichess.org pro analyzu prvnich tahu, jeji frekvence opakovani a pravdepodobnosti vyhry pro stranu hrace a vizualizace vysledku.

## Action:
1) Naloadoval jsem si data za 3 mesice.
2) Kvuli tomu ze data jsou ve formatu .pgn.zst, tzn. zstandard archiv obsahujici .pgn file, vyuzil jsem knihovnu Zstandard pro Python
3) Po rozbaleni dat vypsal jsem je do data.pgn, aby vsechna potrabna data byli na jednom miste
4) Rasparsoval jsem data do csv souboru pro rychlejsi pristup
5) Provedl jsem analyzu a vizualizace potrebnych data
6) Vytvoril jsem si korrelacni matici prevdepodobnosti prvniho tahu oponenta

## Result:
Vystupem dane prace jsou statisticke odpovedi a neoverena v praxi data:
  - Nejcastejsim prvnim tahem Bile strany je "d2d4";
  - Nejcastejsim prvnim tahem Cerne strany je "c7c5";
  
  - Nejuspesnejsim tahem Bile strany je "a2a3";
  - Nejuspesnejsim tahem Cerne strany je "c7c5".

Kvuli tomu ze vyhra v sachach je hodnota zavisla na hodne parametrach vyhru se neda predikovat na prvnim tahu, tak ze svuj vysledek nazyvam neduverovhodnym na 100%.

## Review:
Co bych udelal jinak:
  1) Dal bych si vetsi pozor na zavislost prvniho tahu na parametrech jako "Opening" nebo Skill hrace.
  2) Vyuzil bych vice datovych souboru pro vetsi jasnost odpovedi.
  3) Nevynechavaval bych faktor zavislosti vyhry na kombinace prvnich tahu, kombinace openingu a na zkusenstech souperu.
