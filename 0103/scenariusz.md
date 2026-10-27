# 0103 · CSS3 - stylowanie i responsywność

| | |
|---|---|
| **Semestr** | zimowy - spotkanie 3 z 9 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 |
| **Poprzednie** | [0102 · HTML5 - fundamenty i semantyka](../0102-overview/scenariusz.md) |
| **Następne** | [0104 · CSS w praktyce + pierwsze kroki w JavaScript](../0104/scenariusz.md) |

## Overview

### Cel spotkania

- Uczeń wiąże CSS z HTML-em trzema sposobami i wie, dlaczego **zewnętrzny arkusz** to standard.
- Rozumie **selektory, kaskadę i specyficzność** - i potrafi przewidzieć, która reguła wygra.
- Opanowuje **box model** (z `box-sizing: border-box`), kolory i jednostki, typografię.
- Układa elementy **flexboxem** i tworzy stronę **responsywną** (media queries, mobile-first).
- Kontynuuje a11y: **kontrast i czytelność**.
- Efekt spotkania: **ostylowany fanpage z 0102**, działa na telefonie.

### Kartkówka (10 min) - zakres: 0102

- Semantyczne znaczniki (co wybierasz: `article` czy `div`?); typy `input` i dopasowanie do danych; `label` + a11y; tabele; walidacja HTML5 (`required`, `pattern`).
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Sekcja 1 (50 min) - jak CSS działa

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Trzy sposoby wpięcia CSS** - inline, `<style>`, zewnętrzny `link`; składnia reguły (selektor { właściwość: wartość; }); dlaczego zewnętrzny arkusz | live: ta sama zmiana w 3 wariantach |
| 10' | **Selektory** - element, `.klasa`, `#id`, potomek (spacja), `[atrybut]`, `:hover`; grupowanie; specyficzność i kaskada - „która reguła wygra” na prostych przykładach | mini-ćwiczenie zgadywania wyniku (gra) |
| 10' | **Box model** - content, padding, border, margin; `box-sizing: border-box`; szerokości i „dziura pod obrazkiem” (`display: block`) | DevTools: włączamy widok box model |
| 10' | **Kolory i jednostki** - nazwy, `#hex`, `rgb()`/`rgba()`, `hsl()`; `px` vs `%` vs `em`/`rem` vs `vh`/`vw` - kiedy które | tabela-ściąga na slajdzie |
| 10' | **Typografia** - `font-family` + Google Fonts, `font-size`, `line-height`, `font-weight`, `text-align`; hierarchia tekstu | nawiązanie do kolejności nagłówków z 0102 |

### Przerwa (15 min)

### Sekcja 2 (35 min) - układy, responsywność, start stylowania fanpage'a

| Czas | Temat | Uwagi |
|---|---|---|
| 15' | **Flexbox** - `display: flex`, `flex-direction`, `justify-content`, `align-items`, `gap`, `flex-wrap`; klasyczne wzorce: pasek nawigacji, karty obok siebie, wyśrodkowanie w pionie i poziomie | live: gra Flexbox Froggy jako nagroda dla szybkich? (wariant C) |
| 10' | **Responsywność** - `meta viewport` (przypomnienie z 0101), media queries, strategia **mobile-first**; `max-width: 100%` na obrazkach; jednostki relatywne | demo device toolbar: telefon/tablet/desktop |
| 5' | **a11y cd.** - kontrast tekstu i tła (WebAIM Checker / Lighthouse w DevTools), czytelny rozmiar bazowy, `:focus-visible` a nawigacja Tabem | wracamy do listy błędów a11y z zadania domowego |
| 5' | **Start ćwiczenia głównego: ostyluj fanpage** - paleta kolorów i fonty Google; uczniowie pracują samodzielnie, prowadzący pomaga indywidualnie | warianty A/B/C poniżej |

### Sekcja 3 (25 min) - domknięcie: fanpage, INF.03, podsumowanie

| Czas | Temat | Uwagi |
|---|---|---|
| 20' | **Ćwiczenie główne: ostyluj fanpage (cd.)** - nawigacja pozioma (flexbox), karty galerii, tabela w paski (zebra), stopka; wersja mobilna: nawigacja i karty w kolumnę; warianty B/C dla szybkich | warianty A/B/C poniżej |
| 5' | **Podsumowanie + 5 pytań INF.03 + zadanie domowe + zapowiedź 0104** (grid, animacje, publikacja strony w internecie, dodatek o Tailwind i **pierwszy JavaScript**) i zakres kartkówki | rozbudzić ciekawość: „następnie strona zacznie reagować na klik” |

### Ćwiczenia (ostyluj fanpage)

- **A (podstawowy):** zewnętrzny arkusz `style.css`, paleta 3 kolorów, font z Google Fonts, nawigacja flexbox, karty galerii obok siebie, stopka.
- **B (rozszerzający):** + media query dla telefonu (karty w kolumnę, nawigacja pionowa), tabela zebra, `:hover` na kartach, poprawa kontrastu wg Lighthouse.
- **C (gwiazdka):** + 2–3 poziomy gry Flexbox Froggy do końca / własne cienie i zaokrąglenia (`box-shadow`, `border-radius`) / strona przechodzi audyt Lighthouse „Accessibility” bez czerwonych błędów.

### Zadanie domowe (30–45 min)

1. Dokończ stylowanie fanpage'a - tak, żeby dobrze wyglądał na telefonie (device toolbar!).
2. Uruchom Lighthouse (zakładka Accessibility) i popraw znalezione problemy.
3. **Przygotuj się do kartkówki**: selektory i specyficzność, box model, jednostki, flexbox, media queries.

### Powiązanie z INF.03

- W pracy praktycznej stylowanie wg specyfikacji (kolory, rozmiary, układy) jest **punktowane linia po linii** - ćwiczenie „zrób dokładnie wg wymagań” przygotowuje do formatu egzaminu.
- Na kartkówce pytania zamknięte o selektory/box model w formacie części pisemnej.

### Akcent Akademia Tarnowska

Przy Google Fonts / designie: „na AT projektowaniem interfejsów zajmują się zajęcia z UX - to, co dziś robimy wstępnie, tam rozwijecie w pełne projekty”. Jedno zdanie, koniec.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na trzecie spotkanie kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe - HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już (0101–0102): DevTools, VS Code + Live Server, szkielet HTML, semantykę, tekst/listy/linki/obrazy/tabele/multimedia, formularze z walidacją HTML5, podstawy dostępności (alt, nagłówki, label, Tab); mają własny fanpage (zespół/gracz/gra) z galerią, tabelą i formularzem.
- Temat TEGO spotkania: CSS3 - stylowanie i responsywność; efektem jest ostylowany fanpage działający na telefonie.
- Następne spotkanie (0104): grid, animacje, publikacja strony, dodatek „Jak w branży: Tailwind/atomic CSS” oraz PIERWSZE KROKI W JAVASCRIPT - zapowiedz je mocno („strona zacznie reagować na kliknięcia”).
- Czas: 135 minut = kartkówka (10 min) + sekcja 1 (50 min) + przerwa (15 min) + sekcja 2 (35 min) + sekcja 3 (25 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P” (wprowadzenie → demo → uczeń sam); min. 60% praktyki.
- Kod kompletny i działający; komentarze po polsku. Tylko czysty CSS (bez preprocesorów i frameworków).
- Spinaj materiał z INF.03: stylowanie wg specyfikacji jest punktowane w pracy praktycznej; pytania kartkówkowe w formacie testu egzaminacyjnego.
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent, bez reklamy.

### Zakres merytoryczny spotkania
1. Trzy sposoby wpięcia CSS (inline, style, zewnętrzny link) - dlaczego zewnętrzny; składnia reguły.
2. Selektory: element, .klasa, #id, potomek, atrybut, :hover; grupowanie; kaskada i specyficzność („która reguła wygra”).
3. Box model: content/padding/border/margin, box-sizing: border-box, display: block na obrazkach.
4. Kolory (nazwy, hex, rgb/rgba, hsl) i jednostki (px, %, em/rem, vh/vw) - kiedy które.
5. Typografia: font-family + Google Fonts, font-size, line-height, font-weight, text-align, hierarchia.
6. Flexbox: display:flex, flex-direction, justify-content, align-items, gap, flex-wrap; wzorce: nawigacja, karty, centrowanie.
7. Responsywność: meta viewport, media queries, mobile-first, max-width:100% obrazków.
8. a11y cd.: kontrast (WebAIM/Lighthouse), czytelny rozmiar bazowy, :focus-visible a nawigacja Tabem.
9. Ćwiczenie główne: ostylowanie fanpage'a (paleta, fonty, nawigacja flex, karty, tabela zebra, stopka + wersja mobilna).

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu 0102 (semantyka, typy input i formularze, walidacja, tabele, a11y): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 35 + 25) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO] tam, gdzie demo; obowiązkowe slajdy: diagram box modelu, tabela-ściąga jednostek, diagram flexboxa, media queries mobile-first.
4. Materiały live coding: pliki HTML+CSS budowane krok po kroku (nawigacja flex, karty, media query).
5. Ćwiczenia A/B/C dla fanpage (poziomy jak w zakresie pkt 9; C: Flexbox Froggy / cienie i zaokrąglenia / audyt Lighthouse bez błędów dostępności) z pełnymi rozwiązaniami.
6. Zadanie domowe (30–45 min): dokończenie responsywnego fanpage + Lighthouse accessibility + zakres kartkówki na 0104 (selektory i specyficzność, box model, jednostki, flexbox, media queries).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Sprawdź selektory i wartości (poprawna składnia, brak literówek, reguły realnie działają razem).
- Nie wymyślaj statystyk; materiały gotowe do użycia bez dalszej edycji.
```
