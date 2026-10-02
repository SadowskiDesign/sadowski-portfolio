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

### Typografia

Dwie rodziny, zadeklarowane tylko raz, w `styles.css`:

- `--font-display` - **Georgia**, szeryf do naglowkow i elementow redakcyjnych
- `--font-sans` - **Segoe UI**, do tekstu ciaglego i interfejsu

Zadnych webfontow - strona nie wykonuje zewnetrznych zapytan, wiec nie ma
migniecia tekstu (FOUT) ani zaleznosci od dostepnosci cudzego serwera.

Uwaga przy zmianach: Georgia ma tylko dwie wagi, **400 i 700**. Case study
uzywa wag 500 i 600, ktore przy Georgii spadaja na najblizsza dostepna -
500 na 400, a 600 na 700. Dlatego naglowki sekcji w case study sa pogrubione,
a te same naglowki w portfolio nie.

### Obrazki

`assets/` trzyma siedem plikow. Wczesniej byly wklejone w HTML jako base64, co
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
