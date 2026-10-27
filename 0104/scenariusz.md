# 0104 · CSS w praktyce + pierwsze kroki w JavaScript

| | |
|---|---|
| **Semestr** | zimowy - spotkanie 4 z 9 (grupy A/B) |
| **Czas** | 135 min = **sekcja 60** + przerwa 15 + **sprawdzian semestralny 60** (pisemny; zastępuje kartkówkę - zakres: cały semestr 0101–0104) |
| **Poprzednie** | [0103 · CSS3 - stylowanie i responsywność](../0103/scenariusz.md) |
| **Następne** | [0201 · JavaScript - solidne podstawy języka](../0201/scenariusz.md) (semestr letni) |

## Overview

### Cel spotkania

- Uczeń domyka warsztat CSS: **grid, animacje i pozycjonowanie sticky**.
- **Publikuje stronę w internecie** - własny adres URL do pokazania.
- Widzi „jak w branży”: **Tailwind CSS i atomic/utility-first CSS** (świadomość, nie nauka).
- Przeżywa „moment wow”: **JavaScript sprawia, że strona reaguje** - i pisze swoje pierwsze skrypty (zmienne, konsola, reakcja na kliknięcie).

### Sprawdzian semestralny (60 min, pisemny) - zakres: cały semestr 0101–0104

Sprawdzian zamyka semestr zimowy i **zastępuje kartkówkę** z 0103 (materiał 0103 jest i tak w zakresie). Pada **na końcu spotkania**, więc obejmuje również podstawy JS nauczone tego dnia.

- **Format mieszany, 50 pkt łącznie:**
  - **Część 1 - 30 pytań zamkniętych A–D** (styl INF.03), 30 pkt (1 pkt za pytanie). Rozkład: 0101 (sieć, DevTools) - 5, 0102 (HTML5, semantyka, formularze, a11y) - 8, 0103 (CSS: selektory, box model, flexbox, media queries) - 9, 0104 (grid, publikacja, podstawy JS) - 8.
  - **Część 2 - 6–8 pytań otwartych**, 20 pkt, w tym min. 2 z pisaniem/uzupełnianiem fragmentu kodu na kartce (np. domknij znaczniki formularza, dopisz regułę media query, uzupełnij skrypt licznika kliknięć) oraz 1 pytanie „wyjaśnij własnymi słowami" (np. jak działa DNS, czym jest box model).
- **Do dołączenia w materiałach:** klucz odpowiedzi, punktacja i propozycja skali ocen 1–6 (np. 91%+ celujący, 76–90% bardzo dobry, 56–75% dobry, 41–55% dostateczny, 26–40% dopuszczający, poniżej 26% niedostateczny).
- **Zasady na zajęciach:** bez komputerów i bez AI - kartka i długopis; pytania w formacie zbliżonym do części pisemnej INF.03 (trening przed egzaminem).

### Sekcja 1 (60 min) - CSS w praktyce i pierwsze kroki JavaScript

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Powtórka semestralna** - szybka runda pytań z całego semestru: sieć i DevTools (0101), HTML5 i formularze (0102), selektory, box model, flexbox, media queries (0103); kto odpowie, dostaje „plusa” | rozgrzewka i ostatnia powtórka przed sprawdzianem (części 0101–0103) |
| 10' | **Grid** - `display: grid`, `grid-template-columns`, `repeat()`, `gap`, `grid-column: span`; galeria obrazków w siatce; grid vs flexbox - kiedy które | live: galeria fanpage'a w grid |
| 10' | **Animacje i pozycjonowanie sticky** - `transition`, `transform` (`scale`, `rotate`, `translate`), `@keyframes`; `position: sticky` na nawigacji | efekty „jak na prawdziwych stronach” |
| 5' | **Dodatek „Jak w branży”: Tailwind CSS i atomic CSS** - jedno demo: ta sama karta raz w czystym CSS (nasz sposób), raz w Tailwind; plusy (szybkość, spójność) i minusy („obcy” HTML) w skrócie; wniosek: **najpierw fundamenty, potem narzędzia** | świadomość branżowa - NIE uczymy się Tailwinda |
| 10' | **Publikacja strony w internecie** - założenie konta hostingowego, wgranie plików strony, włączenie własnego publicznego adresu URL | „twoja strona jest w internecie” - moment dumy; zrzut ekranu na grupę |
| 15' | **Pierwsze kroki JavaScript - „moment wow” i pierwszy skrypt** - demo: klik → menu hamburger rozwija się, klik → przełącznik **dark mode** zmienia całą stronę („to jest JavaScript; za chwilę zrobicie to samo”); czym jest JS: jedyny język przeglądarek, 98,9% stron (W3Techs - liczba z 0101); `<script>` na końcu `body`, `console.log()`, komentarze, **zmienne** `let`/`const` (i dlaczego nie `var`), typy: string/number/boolean, szablony `` `Witaj, ${imie}` ``; reakcja na kliknięcie: `onclick` inline dla startu → `addEventListener('click', ...)` + `document.querySelector` (magia na razie - pełnia w 0201) | prowadzący kodzi, uczniowie powtarzają; pełne ćwiczenia A/B/C domykamy w zadaniu domowym |

### Przerwa (15 min)

### Sprawdzian (60 min) - zamyka spotkanie

Bezpośrednio po przerwie: 2–3 zdania podsumowania semestru i zapowiedzi 0201 (semestr letni: solidne podstawy JS - operatory, warunki, pętle, funkcje; zakres kartkówki: grid, media queries, publikacja strony w internecie, podstawy JS - zmienne, `console.log`, `addEventListener`) - potem rozdanie kartek.

Patrz sekcja **„Sprawdzian semestralny”** u góry: 30 pytań zamkniętych A–D + 6–8 otwartych (w tym kod na kartce), 50 pkt, klucz i skala ocen w materiałach prowadzącego. Uczniowie piszą do końca spotkania - bez komputerów i bez AI.

### Ćwiczenia (JavaScript na fanpage)

Ćwiczenia startują razem z prowadzącym w sekcji 1 (licznik kliknięć i dark mode - uczniowie powtarzają kod) - pełne warianty domykamy w zadaniu domowym, bo zajęcia zamyka sprawdzian semestralny.

- **A (podstawowy):** przycisk „Policz kliknięcia” (licznik wyświetlany na stronie) + zmiana tekstu nagłówka po kliknięciu.
- **B (rozszerzający):** + dark mode toggle (`classList.toggle`) + ukrywanie/pokazywanie sekcji przyciskiem.
- **C (gwiazdka):** + menu hamburger (na mobile) albo „dymek” z liczbą sekund od otwarcia strony (`setInterval` - zapowiedź 0203).

### Zadanie domowe (30–45 min)

1. Dokończ interakcje z ćwiczeń; upewnij się, że strona działa i jest opublikowana (zaktualizuj opublikowaną wersję).
2. Podeślij link do swojej strony koledze/koleżance - zrób „mini audyt”: co działa, co poprawić.
3. Jeżeli sprawdzian pokazał słabszy dział - powtórz go z notatek przed 0201.
4. **Przygotuj się do kartkówki** (0201): grid, media queries, publikacja strony w internecie, podstawy JS (zmienne, typy, `console.log`, `addEventListener`).

### Powiązanie z INF.03

- Praca praktyczna INF.03 często wymaga prostej interakcji JS (np. przycisk zmieniający treść/styl) - dzisiejsze ćwiczenia to właśnie format egzaminacyjny.
- Publikacja w internecie uczy workflow „pliki → repozytorium → adres publiczny”, zgodnego z duchem pracy egzaminacyjnej (oddajesz kompletny, działający projekt).

### Akcent Akademia Tarnowska

Przy publikacji: „właśnie zrobiłeś deployment - pierwszego deploya nasi studenci robią na pierwszym roku; dzisiaj zaliczyliście ten kamień milowy przed studiami”. (Jedno zdanie, uśmiech, dalej pracujemy.)

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na czwarte (ostatnie jesienne bazowe) spotkanie kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe - HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już (0101–0103): DevTools, VS Code + Live Server, HTML5 (semantyka, formularze, a11y), CSS3 (selektory, box model, jednostki, typografia, flexbox, media queries); mają responsywny fanpage (galeria, tabela, formularz).
- Temat TEGO spotkania: domknięcie CSS (grid, animacje, sticky), publikacja strony w internecie, dodatek świadomościowy „Jak w branży: Tailwind i atomic CSS” oraz PIERWSZE KROKI W JAVASCRIPT („moment wow”).
- Następne spotkanie (0201, semestr letni): solidne podstawy JS - operatory, warunki, pętle, funkcje, debugowanie. Zapowiedz je.
- Czas: 135 minut = sekcja 1 (60 min: CSS w praktyce + skompresowane pierwsze kroki JS) + przerwa (15 min) + **pisemny sprawdzian semestralny (60 min)**, który zamyka spotkanie - zastępuje kartkówkę, zakres: cały semestr 0101–0104 (w tym podstawy JS z tego dnia).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P”; min. 60% praktyki.
- Kod kompletny i działający; komentarze po polsku. Core zajęć: czysty HTML/CSS/vanilla JS. Wyjątek: krótki DODATEK o Tailwind/atomic CSS wyłącznie jako świadomość branżowa (demo porównawcze „czysty CSS vs Tailwind”, plusy/minusy) - bez nauki pisania w Tailwind.
- Spinaj materiał z INF.03 (prosta interakcja JS bywa elementem pracy praktycznej; pytania kartkówkowe w formacie testu).
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (np. „to był Twój pierwszy deployment”).

### Zakres merytoryczny spotkania
1. Grid: display:grid, grid-template-columns, repeat(), gap, span; galeria w siatce; grid vs flexbox - kiedy które.
2. Animacje: transition, transform (scale/rotate/translate), @keyframes; position: sticky na nawigacji.
3. Dodatek „Jak w branży”: Tailwind CSS i koncepcja atomic/utility-first CSS - demo tej samej karty w czystym CSS i w Tailwind; plusy/minusy; wniosek: najpierw fundamenty, potem narzędzia.
4. Publikacja strony w internecie - konto hostingowe, wgrywanie plików, własny publiczny adres URL.
5. JavaScript - wprowadzenie:
   a) „moment wow”: menu hamburger i dark mode toggle na gotowym przykładzie;
   b) czym jest JS (przeglądarki, Node.js, VS Code napisany w JS/TS; 98,9% stron - W3Techs);
   c) pierwszy skrypt: <script> na końcu body, console.log, komentarze;
   d) zmienne let/const (dlaczego nie var), typy: string/number/boolean, szablony `Witaj, ${imie}`;
   e) reakcja na kliknięcie: onclick inline → addEventListener('click', ...) (zapowiedź pełni w 0202);
   f) funkcja: function + wywołanie; pierwszy kontakt z document.querySelector (bez głębi - szczegóły w 0202).
   Uwaga czasowa: w klasie część JS trwa łącznie ok. 15 min (moment wow + pierwszy skrypt + reakcja na klik - uczniowie powtarzają za prowadzącym); pełne ćwiczenia A/B/C domykane są w zadaniu domowym, a szczegółowa nauka JS należy do 0201.
6. Ćwiczenie: na własnym fanpage - licznik kliknięć, zmiana tytułu, dark mode (klasa .dark).

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. **Sprawdzian semestralny (60 min, pisemny)** - zakres: cały semestr 0101–0104. Format mieszany, 50 pkt: część 1 = 30 pytań zamkniętych A–D w stylu INF.03 (rozkład: 0101 sieć/DevTools - 5, 0102 HTML5 - 8, 0103 CSS - 9, 0104 grid/publikacja/JS - 8); część 2 = 6–8 pytań otwartych (w tym min. 2 z pisaniem/uzupełnianiem kodu na kartce i 1 „wyjaśnij własnymi słowami”). Dołącz klucz, punktację i skalę ocen 1–6.
2. Konspekt z rozpiską czasową (60 + 15 + sprawdzian 60) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej; zaznacz „moment wow” na otwarcie części JS w sekcji 1.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO]; obowiązkowe slajdy: diagram grid, porównanie „czysty CSS vs Tailwind”, „twoja strona w internecie”, pierwsze kroki JS.
4. Materiały live coding: (a) galeria grid z animacjami; (b) karta w czystym CSS i ta sama w Tailwind (CDN, tylko do demo); (c) kompletny przykład hamburger + dark mode; (d) skrypt licznika krok po kroku.
5. Ćwiczenia A/B/C (poziomy jak w zakresie pkt 6; C: menu hamburger albo licznik sekund z setInterval) z pełnymi rozwiązaniami.
6. Zadanie domowe (30–45 min): dokończenie interakcji, aktualizacja opublikowanej strony, „mini audyt” strony kolegi + zakres kartkówki na 0201 (grid, media queries, publikacja strony, podstawy JS).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Każdy przykład JS ma działać po wklejeniu (domknięte nawiasy, poprawne selektory, skrypt na końcu body).
- Nie wymyślaj statystyk (98,9% - W3Techs, podałem źródło); materiały gotowe do użycia bez dalszej edycji.
```
