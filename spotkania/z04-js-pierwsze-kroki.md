# Z4 · CSS w praktyce + pierwsze kroki w JavaScript

| | |
|---|---|
| **Semestr** | zimowy — spotkanie 4 z 9 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + blok 50 + przerwa 15 + blok 60 |
| **Poprzednie** | [Z3 · CSS3 — stylowanie i responsywność](z03-css3-stylowanie.md) |
| **Następne** | [L1 · JavaScript — solidne podstawy języka](l01-js-podstawy.md) (semestr letni) |

## Overview

### Cel spotkania

- Uczeń domyka warsztat CSS: **grid, animacje i pozycjonowanie sticky**.
- **Publikuje stronę w internecie** (GitHub Pages) — własny adres URL do pokazania.
- Widzi „jak w branży”: **Tailwind CSS i atomic/utility-first CSS** (świadomość, nie nauka).
- Przeżywa „moment wow”: **JavaScript sprawia, że strona reaguje** — i pisze swoje pierwsze skrypty (zmienne, konsola, reakcja na kliknięcie).

### Kartkówka (10 min) — zakres: Z3

- Selektory i specyficzność (która reguła wygra); box model i `box-sizing`; jednostki (`rem` vs `px`); flexbox (`justify-content` vs `align-items`); media queries i mobile-first.
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Blok 1 (50 min) — CSS: powtórka, grid, animacje, publikacja, Tailwind

| Czas | Temat | Uwagi |
|---|---|---|
| 5' | **Mini-powtórka Z3** — szybka runda pytań: selektory, box model, flexbox, media queries (kto odpowie, dostaje „plusa”) | rozgrzewka po kartkówce |
| 10' | **Grid** — `display: grid`, `grid-template-columns`, `repeat()`, `gap`, `grid-column: span`; galeria obrazków w siatce; grid vs flexbox — kiedy które | live: galeria fanpage'a w grid |
| 10' | **Animacje i przejścia** — `transition`, `transform` (`scale`, `rotate`, `translate`), `@keyframes`; `position: sticky` na nawigacji | efekty „jak na prawdziwych stronach” |
| 10' | **Dodatek „Jak w branży”: Tailwind CSS i atomic CSS** — koncepcja: tysiące małych klas użyteczności zamiast własnego CSS; demo: ta sama karta raz w czystym CSS (nasz sposób) raz w Tailwind; plusy (szybkość, spójność) i minusy („obcy” HTML, nauka nazw klas); wniosek: **najpierw fundamenty, potem narzędzia** | świadomość branżowa — NIE uczymy się Tailwinda |
| 15' | **Publikacja: GitHub Pages** — konto GitHub, nowe repozytorium, wgranie plików strony (drag & drop przez stronę), włączenie Pages, własny adres `login.github.io/repo` | „twoja strona jest w internecie” — moment dumy; zrzut ekranu na grupę |

### Przerwa (15 min)

### Blok 2 (60 min) — JavaScript: strona zaczyna żyć

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **„Moment wow”** — prowadzący na gotowym przykładzie: klik — menu hamburger rozwija się, klik — przełącznik **dark mode** zmienia całą stronę; „to jest JavaScript; za chwilę sami zrobicie to samo” | demo z realną stroną ucznia, jeśli się uda |
| 5' | **Czym jest JavaScript** — jedyny język przeglądarek; działa też poza nimi (Node.js, VS Code napisany w JS/TS, aplikacje desktopowe i mobilne); wróćmy do liczby z Z1: 98,9% stron | spiąć klamrą do statystyk z Z1 |
| 15' | **Pierwszy skrypt** — `<script>` na końcu `body`; `console.log()`; komentarze; **zmienne**: `let` i `const` (i dlaczego nie `var`); typy: string, number, boolean; szablony `` `Witaj, ${imie}` `` | wszystko w konsoli + na stronie |
| 15' | **Reakcja na kliknięcie** — `onclick` inline dla startu → `addEventListener('click', ...)` (zapowiedź pełni w L2); funkcja: `function` + wywołanie; zmiana strony: `document.querySelector(...)` (magia na razie, szczegóły w L2) | prowadzący kodzi, uczniowie powtarzają |
| 15' | **Ćwiczenie samodzielne** — na własnym fanpage: przycisk licznika kliknięć, przycisk zmieniający tytuł strony, dark mode toggle (klasa `.dark` + zmiana kolorów w CSS) | warianty A/B/C poniżej |
| (w ramach ćwiczeń) | **Podsumowanie semestru + zapowiedź L1** i zakresu kartkówki (grid, media queries, publikacja, podstawy JS: zmienne, `console.log`, `addEventListener`) | | 

### Ćwiczenia (JavaScript na fanpage)

- **A (podstawowy):** przycisk „Policz kliknięcia” (licznik wyświetlany na stronie) + zmiana tekstu nagłówka po kliknięciu.
- **B (rozszerzający):** + dark mode toggle (`classList.toggle`) + ukrywanie/pokazywanie sekcji przyciskiem.
- **C (gwiazdka):** + menu hamburger (na mobile) albo „dymek” z liczbą sekund od otwarcia strony (`setInterval` — zapowiedź L3).

### Zadanie domowe (30–45 min)

1. Dokończ interakcje z ćwiczeń; upewnij się, że strona działa i jest opublikowana (zaktualizuj GitHub Pages).
2. Podeślij link do swojej strony koledze/koleżance — zrób „mini audyt”: co działa, co poprawić.
3. **Przygotuj się do kartkówki** (L1): grid, media queries, publikacja GitHub Pages, podstawy JS (zmienne, typy, `console.log`, `addEventListener`).

### Powiązanie z INF.03

- Praca praktyczna INF.03 często wymaga prostej interakcji JS (np. przycisk zmieniający treść/styl) — dzisiejsze ćwiczenia to właśnie format egzaminacyjny.
- Publikacja na GitHub Pages uczy workflow „pliki → repozytorium → adres publiczny”, zgodnego z duchem pracy egzaminacyjnej (oddajesz kompletny, działający projekt).

### Akcent Akademia Tarnowska

Przy publikacji: „właśnie zrobiłeś deployment — pierwszego deploya nasi studenci robią na pierwszym roku; dzisiaj zaliczyliście ten kamień milowy przed studiami”. (Jedno zdanie, uśmiech, dalej pracujemy.)

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na czwarte (ostatnie jesienne bazowe) spotkanie kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już (Z1–Z3): DevTools, VS Code + Live Server, HTML5 (semantyka, formularze, a11y), CSS3 (selektory, box model, jednostki, typografia, flexbox, media queries); mają responsywny fanpage (galeria, tabela, formularz).
- Temat TEGO spotkania: domknięcie CSS (grid, animacje, sticky), publikacja GitHub Pages, dodatek świadomościowy „Jak w branży: Tailwind i atomic CSS” oraz PIERWSZE KROKI W JAVASCRIPT („moment wow”).
- Następne spotkanie (L1, semestr letni): solidne podstawy JS — operatory, warunki, pętle, funkcje, debugowanie. Zapowiedz je.
- Czas: 135 minut = kartkówka (10 min) + blok 1 (50 min) + przerwa (15 min) + blok 2 (60 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P”; min. 60% praktyki.
- Kod kompletny i działający; komentarze po polsku. Core zajęć: czysty HTML/CSS/vanilla JS. Wyjątek: krótki DODATEK o Tailwind/atomic CSS wyłącznie jako świadomość branżowa (demo porównawcze „czysty CSS vs Tailwind”, plusy/minusy) — bez nauki pisania w Tailwind.
- Spinaj materiał z INF.03 (prosta interakcja JS bywa elementem pracy praktycznej; pytania kartkówkowe w formacie testu).
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (np. „to był Twój pierwszy deployment”).

### Zakres merytoryczny spotkania
1. Grid: display:grid, grid-template-columns, repeat(), gap, span; galeria w siatce; grid vs flexbox — kiedy które.
2. Animacje: transition, transform (scale/rotate/translate), @keyframes; position: sticky na nawigacji.
3. Dodatek „Jak w branży”: Tailwind CSS i koncepcja atomic/utility-first CSS — demo tej samej karty w czystym CSS i w Tailwind; plusy/minusy; wniosek: najpierw fundamenty, potem narzędzia.
4. Publikacja: GitHub Pages — konto, repozytorium, wgrywanie plików, włączenie Pages, adres login.github.io/repo.
5. JavaScript — wprowadzenie:
   a) „moment wow”: menu hamburger i dark mode toggle na gotowym przykładzie;
   b) czym jest JS (przeglądarki, Node.js, VS Code napisany w JS/TS; 98,9% stron — W3Techs);
   c) pierwszy skrypt: <script> na końcu body, console.log, komentarze;
   d) zmienne let/const (dlaczego nie var), typy: string/number/boolean, szablony `Witaj, ${imie}`;
   e) reakcja na kliknięcie: onclick inline → addEventListener('click', ...) (zapowiedź pełni w L2);
   f) funkcja: function + wywołanie; pierwszy kontakt z document.querySelector (bez głębi — szczegóły w L2).
6. Ćwiczenie: na własnym fanpage — licznik kliknięć, zmiana tytułu, dark mode (klasa .dark).

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu Z3 (selektory/specyficzność, box model, jednostki, flexbox, media queries): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 60) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej; zaznacz „moment wow” na otwarcie bloku 2.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO]; obowiązkowe slajdy: diagram grid, porównanie „czysty CSS vs Tailwind”, „twoja strona w internecie” (GitHub Pages), pierwsze kroki JS.
4. Materiały live coding: (a) galeria grid z animacjami; (b) karta w czystym CSS i ta sama w Tailwind (CDN, tylko do demo); (c) kompletny przykład hamburger + dark mode; (d) skrypt licznika krok po kroku.
5. Ćwiczenia A/B/C (poziomy jak w zakresie pkt 6; C: menu hamburger albo licznik sekund z setInterval) z pełnymi rozwiązaniami.
6. Zadanie domowe (30–45 min): dokończenie interakcji, aktualizacja GitHub Pages, „mini audyt” strony kolegi + zakres kartkówki na L1 (grid, media queries, GitHub Pages, podstawy JS).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Każdy przykład JS ma działać po wklejeniu (domknięte nawiasy, poprawne selektory, skrypt na końcu body).
- Nie wymyślaj statystyk (98,9% — W3Techs, podałem źródło); materiały gotowe do użycia bez dalszej edycji.
```
