# Portfolio - Michal Sadowski

Portfolio UX/UI designera: strona glowna z wybranymi projektami oraz case study
projektu REC Registry (modernizacja 15-letniej platformy certyfikatow energii
odnawialnej).

## Struktura

```
index.html             strona glowna (hero, Selected work, About, Contact)
case-study/index.html  case study REC Registry
```

Oba pliki sa samowystarczalne - wszystkie obrazki sa wklejone jako base64, wiec
strona dziala bez zadnych dodatkowych zasobow. Jedyne zewnetrzne odwolania to
linki pomiedzy tymi dwoma plikami.

## Uruchomienie lokalne

Otworz `index.html` w przegladarce (dwuklik). Nie jest potrzebny zaden serwer
ani proces budowania.

## Wprowadzanie zmian

Edytuj pliki HTML bezposrednio i zatwierdzaj zmiany w GitHub Desktop.
Repozytorium jest jedynym zrodlem prawdy dla strony.

## Uwaga o obrazkach

Obrazki sa osadzone w HTML jako base64. Kazdy z nich zajmuje jedna bardzo dluga
linie, przez co diff w gicie dla takiej linii jest nieczytelny. Jesli to zacznie
przeszkadzac, mozna wyniesc obrazki do osobnych plikow i podlinkowac je zwyklymi
sciezkami.
