# Portfolio - Michal Sadowski

Portfolio UX/UI designera: strona glowna z wybranymi projektami oraz case study
projektu REC Registry (modernizacja 15-letniej platformy certyfikatow energii
odnawialnej).

## Struktura

```
index.html             strona glowna (hero, Selected work, About, Contact)
styles.css             wspolna powloka obu stron
case-study/index.html  case study REC Registry
assets/                obrazki
```

### Podzial CSS

`styles.css` zawiera to, co obie strony maja wspolne:

- tokeny (kolory, typografia, easing)
- reset i kontener `.wrap`
- naglowek: logo, wordmark, nawigacja
- pole kropek (dot-field)
- mechanizm odslaniania przy przewijaniu (`.reveal`)

Wszystko, co dotyczy tylko jednej strony, zostaje w jej bloku `<style>`.
**Naglowek jest zdefiniowany tylko w `styles.css`** - dzieki temu obie strony nie
moga sie juz rozjechac.

Jedyna rzecz, ktora kazda strona ustawia sama, to pozycjonowanie naglowka:
portfolio uzywa `sticky` (bo jego hero jest przyklejona kurtyna), a case study
`fixed`. Reszta wygladu naglowka jest wspolna.

### Obrazki

`assets/` trzyma szesc plikow. Wczesniej byly wklejone w HTML jako base64, co
oznaczalo +33% narzutu i trzy kopie tego samego screenshota. Teraz przegladarka
pobiera kazdy obrazek raz i korzysta z cache przy przejsciu miedzy stronami.

Wymiary w atrybutach `width`/`height` sa zgodne z rzeczywistymi plikami, wiec
przy wczytywaniu nie ma przesuniecia ukladu (CLS).

## Uruchomienie lokalne

Otworz `index.html` w przegladarce (dwuklik). Nie jest potrzebny zaden serwer
ani proces budowania.

## Wprowadzanie zmian

Edytuj pliki bezposrednio i zatwierdzaj zmiany w GitHub Desktop.
Repozytorium jest jedynym zrodlem prawdy dla strony.

Przy zmianie naglowka pamietaj, ze jest on w `styles.css` - zmiana tam zadziala
na obu stronach jednoczesnie.
