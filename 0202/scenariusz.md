# 0202 · DOM i zdarzenia — strona żyje

| | |
|---|---|
| **Semestr** | letni — spotkanie 2 z 11 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 |
| **Poprzednie** | [0201 · JavaScript — solidne podstawy języka](../0201/scenariusz.md) |
| **Następne** | [0203 · Tablice, obiekty i dane](../0203/scenariusz.md) |

## Overview

### Cel spotkania

- Uczeń rozumie, że **DOM to mapa strony**, którą JavaScript potrafi czytać i zmieniać.
- Wybiera elementy (`querySelector`/`querySelectorAll`) i zmienia je: `textContent`, `innerHTML`, `style`, **`classList`**, wartości pól formularza.
- Obsługuje **zdarzenia**: `click`, `input`, `submit` — i pisze **walidację formularza w JS** z komunikatami dla użytkownika.
- Buduje kompletne mini-projekty: licznik, galeria, quiz.

### Kartkówka (10 min) — zakres: 0201

- Operatory i `===` (co wypisze konsola); `if`/`else` i truthy/falsy; pętle (`for` — ile iteracji, co wypisze); funkcje: `return`, zapis arrow.
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Sekcja 1 (50 min) — DOM: czytanie i zmiana strony

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Czym jest DOM** — przeglądarka zamienia HTML w drzewo obiektów; zakładka Elements to właśnie DOM; „strona to obiekty, obiekty można zmieniać” | diagram drzewa na slajdzie; demo w Elements |
| 10' | **Wybieranie elementów** — `document.querySelector()` (selektory CSS — wszystko z 0103 działa!), `querySelectorAll()`; `getElementById` (spotkacie w starszym kodzie i arkuszach INF.03) | live: wybieramy nagłówek, przycisk, pola |
| 15' | **Zmiana elementów** — `textContent` (tekst), `innerHTML` (HTML — ostrożnie), `style.color` itd., **`classList.add/remove/toggle`** (tanie i szybkie — łączymy z CSS z 0103/0104!), `value` pól input, `setAttribute` (np. `src` obrazka) | to jest serce zajęć — dużo ćwiczenia |
| 15' | **Pierwsze zdarzenia** — `addEventListener('click', fn)`; funkcja jako wartość (arrow!); obiekt `event` (`.target`); zdarzenia: `click`, `input`, `change`, `submit`, `keydown` | od `onclick` z 0104 do pełnego `addEventListener` |

### Przerwa (15 min)

### Sekcja 2 (35 min) — formularz z walidacją, start projektu

| Czas | Temat | Uwagi |
|---|---|---|
| 15' | **Formularz z walidacją JS** — odczyt `value` z pól; `submit` + `preventDefault()`; walidacja: puste pole, za krótki tekst, zły e-mail (regex podany gotowo); komunikaty błędów wypisywane na stronie (nie w `alert`!); a11y: komunikaty powiązane z polami | INF.03 praktyka lubi formularze z walidacją |
| 20' | **Start ćwiczenia głównego — wybierz projekt:** (1) **Licznik** +/-/reset z zapisem w zmiennej; (2) **Galeria** — miniatury, klik podmienia duże zdjęcie (`setAttribute`); (3) **Quiz** — 5 pytań jednokrotnego wyboru, sprawdzenie odpowiedzi, punkty, wynik końcowy; prowadzący pomaga indywidualnie | każdy robi jeden projekt; szybcy dwa |

### Sekcja 3 (25 min) — domknięcie: projekty, code review, podsumowanie

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Ćwiczenie główne (cd.)** — dokończenie wybranego projektu; warianty B/C dla szybkich | warianty A/B/C poniżej |
| 15' | **Mini-prezentacje i code review** — 2–3 ochotników pokazuje projekt; klasa szuka ulepszeń; **podsumowanie + 5 pytań INF.03 + zadanie domowe + zapowiedź 0203** (dane: tablice, obiekty, localStorage — „twoja lista zadań zapamięta się po odświeżeniu”) i zakres kartkówki | budujemy kulturę pokazywania pracy |

### Ćwiczenia

- **A (podstawowy):** licznik z przyciskami +/−/reset (wynik na stronie, nie w alercie).
- **B (rozszerzający):** galeria z podmianą dużego zdjęcia LUB quiz z punktacją.
- **C (gwiazdka):** quiz + pasek postępu + podświetlenie poprawnych/błędnych odpowiedzi po sprawdzeniu.

### Zadanie domowe (30–45 min)

1. Dokończ wybrany projekt; dodaj walidację formularza kontaktowego na swoim fanpage'u (z komunikatami na stronie).
2. Zrób „test użytkownika”: poproś domownika o klikanie i obejrzyj, co go zmyliło — zanotuj 1 wniosek.
3. **Przygotuj się do kartkówki**: `querySelector` vs `getElementById`, `textContent` vs `innerHTML`, `classList`, `addEventListener`, `preventDefault`.

### Powiązanie z INF.03

- „Skrypt ma działać po kliknięciu przycisku i zmienić zawartość/style elementu” — klasyka pracy praktycznej; dziś dokładnie to robimy.
- Część pisemna: kolejność zdarzeń, cel `preventDefault`, różnica metod DOM — format kartkówki.

### Akcent Akademia Tarnowska

Przy code review: „właśnie robicie to, co studenci na obronie projektu — pokazujecie kod i przyjmujecie feedback; to się wyczuwa tylko w praktyce”. Jedno zdanie.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na drugie spotkanie semestru letniego kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już: HTML5 (semantyka, formularze, a11y), CSS3 (flexbox, grid, responsywność), podstawy JS (zmienne, typy, operatory ===, if/else, pętle, funkcje i arrow function, debugowanie) oraz pierwszy kontakt z querySelector/addEventListener z 0104.
- Temat TEGO spotkania: DOM i zdarzenia — wybieranie i zmiana elementów, obsługa zdarzeń, formularz z walidacją JS, mini-projekty (licznik, galeria, quiz).
- Następne spotkanie (0203): tablice, obiekty, JSON, localStorage („lista zadań zapamięta się po odświeżeniu”), setTimeout/setInterval, fetch. Zapowiedz je.
- Czas: 135 minut = kartkówka (10 min) + sekcja 1 (50 min) + przerwa (15 min) + sekcja 2 (35 min) + sekcja 3 (25 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P”; min. 60% praktyki.
- Kod kompletny i działający; komentarze po polsku; wyłącznie vanilla JS; błędy walidacji pokazujemy na stronie (nie w alert).
- Spinaj materiał z INF.03: „skrypt po kliknięciu przycisku zmienia treść/style” to klasyka pracy praktycznej; kartkówka w formacie testu.
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (np. code review jak na obronie projektu studenckiego).

### Zakres merytoryczny spotkania
1. DOM jako drzewo obiektów; zakładka Elements = DOM.
2. Wybieranie: querySelector / querySelectorAll (selektory CSS), getElementById (starszy kod, arkusze INF.03).
3. Zmiana: textContent, innerHTML (ostrożnie), style, classList.add/remove/toggle, value pól, setAttribute (src).
4. Zdarzenia: addEventListener (click, input, change, submit, keydown), funkcja zwrotna (arrow), obiekt event i event.target.
5. Formularz z walidacją JS: odczyt value, submit + preventDefault, reguły (puste pole, długość, e-mail — regex podany gotowo), komunikaty na stronie, a11y komunikatów.
6. Projekty do wyboru: licznik (+/−/reset), galeria z podmianą zdjęcia, quiz z punktacją.

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu 0201 (operatory ===, if/else, pętle, funkcje i return, arrow function): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 (w tym pytania „co wypisze konsola”) + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 35 + 25) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej; zaplanuj mini-prezentacje uczniowskie na koniec.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO]; obowiązkowe slajdy: diagram drzewa DOM, tabela „co chcesz zmienić → właściwość”, schemat addEventListener.
4. Materiały live coding: (a) zmiana nagłówka i stylu po kliknięciu; (b) classList.toggle (dark mode z 0104 — teraz rozumiany w pełni); (c) formularz z walidacją krok po kroku.
5. Ćwiczenia A/B/C (A: licznik; B: galeria lub quiz; C: quiz z paskiem postępu i podświetleniem odpowiedzi) z pełnymi rozwiązaniami — kompletne pliki HTML+CSS+JS.
6. Zadanie domowe (30–45 min): dokończenie projektu, walidacja formularza na fanpage, „test użytkownika” z domownikiem + zakres kartkówki na 0203 (querySelector vs getElementById, textContent vs innerHTML, classList, addEventListener, preventDefault).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Każdy przykład działa po wklejeniu (skrypt na końcu body, poprawne selektory, domknięte nawiasy).
- Materiały gotowe do użycia na zajęciach bez dalszej edycji.
```
