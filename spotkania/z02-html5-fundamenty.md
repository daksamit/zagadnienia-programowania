# Z2 · HTML5 — fundamenty i semantyka

| | |
|---|---|
| **Semestr** | zimowy — spotkanie 2 z 9 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + blok 50 + przerwa 15 + blok 60 |
| **Poprzednie** | [Z1 · Dlaczego web?](z01-wstep-przegladarki-devtools.md) |
| **Następne** | [Z3 · CSS3 — stylowanie i responsywność](z03-css3-stylowanie.md) |

## Overview

### Cel spotkania

- Uczeń buduje **semantyczny szkielet strony** w HTML5 i wie, po co (dostępność, SEO, czytelność — i punkty na INF.03).
- Zna i stosuje: znaczniki tekstu, listy, linki, obrazy, tabele, multimedia.
- Tworzy **formularz z walidacją HTML5** (ulubiony temat zadań egzaminacyjnych).
- Rozumie **dostępność (a11y)**: `alt`, kolejność nagłówków, `label`, nawigacja klawiaturą, ARIA i WCAG w pigułce.

### Kartkówka (10 min) — zakres: Z1

- Mikro-historia WWW (kiedy, kto, gdzie); klient–serwer i DNS w pigułce; do czego służą DevTools (Elements/Console); szkielet dokumentu HTML z Z1.
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja (0–5 pkt → oceny).

### Blok 1 (50 min) — szkielet strony i treść

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Semantyczny szkielet** — `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`; div vs elementy semantyczne; dlaczego semantyka: czytniki ekranu, SEO, punkty w kryteriach INF.03 | live: przekształcamy „ścianę divów” w semantyczny szkielet |
| 10' | **Tekst i listy** — `h1–h6` (kolejność ma znaczenie!), `p`, `strong`/`em`, `br`/`hr`, `blockquote`; `ul`/`ol`/`dl` — kiedy które | krótkie demo, dużo ćwiczenia |
| 10' | **Linki i ścieżki** — `a href`, względne vs bezwzględne, `target`, `rel="noopener"`, zakotwiczenia (`#id`) | pułapka egzaminacyjna: ścieżki względne |
| 10' | **Obrazy** — `img`, `alt` (naprawdę!), formaty: JPG/PNG/WebP/SVG i kiedy który; `figure`/`figcaption`; `width`/`height` a „skoki” layoutu | nawiązanie: formaty w zadaniach INF.03 |
| 10' | **Dostępność (a11y) — fundament** — po co: liczby osób korzystających z czytników, wymogi prawne UE (European Accessibility Act); `alt`, `lang`, kolejność nagłówków, `label` powiązany z polem, nawigacja klawiaturą (Tab), ARIA tylko tam, gdzie HTML nie wystarczy; WCAG w pigułce: spostrzegalne, funkcjonalne, zrozumiałe | demo: czytnik ekranu / nawigacja Tab bez myszy |

### Przerwa (15 min)

### Blok 2 (60 min) — tabele, multimedia, formularze, fanpage

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Tabele** — `table`, `tr`, `th`, `td`, `thead`/`tbody`, `caption`; tabela danych ≠ layout | INF.03 lubi zestawienia danych |
| 5' | **Multimedia** — `audio`, `video` (controls), `iframe` (mapa, film) | krótko, demo |
| 15' | **Formularze + walidacja HTML5** — `form`, `input` i jego typy (text, email, number, date, password, radio, checkbox, file, color, range), `label`, `textarea`, `select`, `button`; walidacja: `required`, `pattern`, `min`/`max`, komunikaty przeglądarki | niemal każda praca praktyczna INF.03 ma formularz |
| 25' | **Ćwiczenie główne: fanpage** — strona ulubionego zespołu/gracza/gry: semantyczny szkielet, galeria 3+ obrazków z `alt`, tabela (np. dyskografia/wyniki), formularz zapisu z walidacją; **checklista a11y**: alt, nagłówki po kolei, label przy każdym polu, przejście Tabem | warianty A/B/C poniżej |
| 5' | **Podsumowanie + zapowiedź Z3** (stylowanie fanpage'a) i zakresu kartkówki | |

### Ćwiczenia (fanpage)

- **A (podstawowy):** semantyczny szkielet + 2 sekcje + galeria z `alt` + formularz (imię, e-mail z walidacją).
- **B (rozszerzający):** + tabela danych + `select`/`radio` w formularzu + multimedia (audio/wideo/iframe).
- **C (gwiazdka):** + zakotwiczenia i menu wewnętrzne + sprawdzenie strony przejściem Tabem (czy da się dotrzeć wszędzie bez myszy?) + poprawa znalezionych problemów.

### Zadanie domowe (30–45 min)

1. Dokończ fanpage zgodnie z checklistą a11y.
2. Znajdź w internecie stronę z oczywistym błędem dostępności (brak `alt`, „ściana divów”) — zapisz link, omówimy na Z3.
3. **Przygotuj się do kartkówki**: semantyka, formularze i typy `input`, tabele, podstawy a11y.

### Powiązanie z INF.03

- Semantyczny szkielet, formularz z walidacją i tabela to stałe elementy prac praktycznych — ćwiczymy dokładnie w formacie egzaminacyjnym.
- Pytania zamknięte na kartkówce odwzorowują format części pisemnej (40 zadań, jednokrotny wybór).

### Akcent Akademia Tarnowska

Jedno zdanie przy formularzach: „dokładnie takie formularze studenci AT robią na zaliczeniowe projekty aplikacji — niedługo będziecie mieli przewagę na starcie”. Konkretnie, z humorem, bez reklamy.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na drugie spotkanie kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już (Z1): mikro-historię WWW, klient–serwer/DNS/HTTP, przeglądarki i silniki, Chrome DevTools (Elements/Console/device toolbar), VS Code + Live Server, szkielet pierwszej strony HTML, zasady nauki z AI (ELI5 itd.).
- Temat TEGO spotkania: HTML5 — fundamenty i semantyka + dostępność (a11y).
- Następne spotkanie (Z3): CSS3 — stylowanie i responsywność (fanpage zostanie ostylowany). Zapowiedz je i zaplanuj pomost.
- Czas: 135 minut = kartkówka (10 min) + blok 1 (50 min) + przerwa (15 min) + blok 2 (60 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny, bez lania wody; odbiorca: technikum.
- Wzorzec „3×P”: krótkie wprowadzenie → PROWADZĄCY pokazuje na żywo → UCZEŃ robi sam. Min. 60% czasu to praktyka uczniowska.
- Kod kompletny i działający po wklejeniu; komentarze po polsku.
- Gdzie się da, spinaj materiał z egzaminem INF.03 (część praktyczna: witryna + baza; część pisemna: test 40 zadań zamkniętych).
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent na spotkanie, bez tonu reklamy.

### Zakres merytoryczny spotkania
1. Semantyczny szkielet: header, nav, main, section, article, aside, footer; div vs semantyka (dostępność, SEO, czytelność).
2. Tekst: h1–h6 (kolejność!), p, strong/em, br/hr, blockquote; listy ul/ol/dl.
3. Linki: a href, ścieżki względne/bezwzględne, target, rel="noopener", zakotwiczenia #id.
4. Obrazy: img, alt, formaty (JPG/PNG/WebP/SVG) i kiedy które, figure/figcaption, width/height.
5. Dostępność (a11y): po co (osoby korzystające z czytników ekranu, wymogi prawne UE — European Accessibility Act); alt, lang, kolejność nagłówków, label powiązany z polem, nawigacja klawiaturą (Tab), ARIA tylko gdy HTML nie wystarcza; WCAG w pigułce (spostrzegalne, funkcjonalne, zrozumiałe); a11y jako kryterium punktowane w zadaniach INF.03.
6. Tabele: table/tr/th/td, thead/tbody, caption.
7. Multimedia: audio, video (controls), iframe.
8. Formularze + walidacja HTML5: form, input (text, email, number, date, password, radio, checkbox, file, color, range), label, textarea, select, button; required, pattern, min/max.
9. Ćwiczenie główne: fanpage (ulubiony zespół/gracz/gra) — szkielet semantyczny, galeria z alt, tabela, formularz z walidacją, checklista a11y.

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu Z1 (historia WWW, klient–serwer/DNS, DevTools, szkielet HTML): 4–5 pytań, w tym min. 2 zamknięte jednokrotnego wyboru A–D w formacie INF.03 i 1–2 krótkie otwarte; klucz odpowiedzi, punktacja 0–5, propozycja skali ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 60) co najmniej co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + wskazówka [NA ŻYWO] tam, gdzie demo; obowiązkowy slajd o a11y (z liczbami o osobach z niepełnosprawnościami korzystających z sieci — podaj źródło i rok, jeśli nie masz pewnej liczby, zamiast wymyślać zaproponuj ujęcie bez liczby).
4. Materiały live coding: „ściana divów” → przekształcenie w semantyczny szkielet; formularz krok po kroku.
5. Ćwiczenia A/B/C (fanpage — poziomy opisane wyżej w zakresie pkt 9) z pełnymi rozwiązaniami w osobnej sekcji.
6. Zadanie domowe (30–45 min): dokończenie fanpage z checklistą a11y, znalezienie strony z błędem dostępności + zakres kartkówki na Z3 (semantyka, formularze i typy input, tabele, podstawy a11y).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i jednozdaniowym uzasadnieniem.

### Jakość
- Sprawdź poprawność każdego fragmentu kodu (domknięte znaczniki, poprawne atrybuty, działająca walidacja formularza).
- Nie wymyślaj statystyk; gdzie brak danych — zaznacz „do weryfikacji”.
- Materiały gotowe do użycia na zajęciach bez dalszej edycji.
```
