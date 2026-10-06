# L1 · JavaScript — solidne podstawy języka

| | |
|---|---|
| **Semestr** | letni — spotkanie 1 z 11 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + blok 50 + przerwa 15 + blok 60 |
| **Poprzednie** | [Z4 · CSS w praktyce + pierwsze kroki w JavaScript](z04-js-pierwsze-kroki.md) |
| **Następne** | [L2 · DOM i zdarzenia — strona żyje](l02-js-dom-zdarzenia.md) |

## Overview

### Cel spotkania

- Uczeń porządkuje i pogłębia start z Z4: **zmienne, typy, operatory**.
- Opanowuje **warunki** (`if`/`else`, operatory logiczne), **pętle** (`for`, `while`) i **funkcje** (deklaracja, parametry, `return`, arrow function).
- Poznaje szybkie interakcje: `alert`/`prompt`/`confirm` — i wie, że to tylko do prototypów.
- UCZY SIĘ **debugować**: `console.log`, breakpointy w DevTools, czytanie komunikatów błędów.
- Pisze pierwsze małe programy działające w konsoli (kalkulator BMI, „zgadnij liczbę”).

### Kartkówka (10 min) — zakres: Z4

- Grid i media queries; publikacja GitHub Pages (kroki); podstawy JS z Z4: `let`/`const`, typy, `console.log`, `addEventListener('click', ...)`.
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Blok 1 (50 min) — język: wartości, decyzje, powtórzenia

| Czas | Temat | Uwagi |
|---|---|---|
| 5' | **Rozgrzewka: co pamiętasz z Z4?** — szybkie live: uruchamiamy konsolę, przypominamy `let`/`const` i `console.log` | po przerwie semestralnej bez tego ani rusz |
| 10' | **Operatory** — arytmetyczne (`+ - * / %`), przypisanie (`+=`), inkrementacja; porównania: `==` vs `===` (**zawsze `===`**); logiczne `&&`/`\|\|`/`!`; konkatenacja vs szablony `` `${}` `` | mini-zagadki „co wypisze konsola” |
| 15' | **Warunki** — `if` / `else if` / `else`; zagnieżdżania unikamy; `switch` (kiedy czytelniejszy); wartości prawdziwe/fałszywe (truthy/falsy) na 3 przykładach | live: kalkulator ocen / pełnoletniość |
| 15' | **Pętle** — `for` (klasyczny licznik), `while`; iterowanie po znakach stringu i po liczbach; kiedy pętla nieskończona i jak przerwać (`break`) | ćwiczenie: tabliczka mnożenia w konsoli |
| 5' | **`alert`/`prompt`/`confirm`** — szybkie prototypy interakcji; dlaczego na produkcji ich nie używamy (blokują stronę) | mostek do DOM w L2 |

### Przerwa (15 min)

### Blok 2 (60 min) — funkcje, debugowanie, pierwszy program

| Czas | Temat | Uwagi |
|---|---|---|
| 15' | **Funkcje** — deklaracja `function`, parametry i argumenty, `return` (funkcja bez `return` zwraca `undefined`); wywołanie przed definicją? (hoisting tylko wspomnieć); **arrow function** `() => {}` — nowoczesny zapis, który zobaczą w każdej dokumentacji | przepisywanie 3 funkcji z function na arrow |
| 10' | **Debugowanie** — czytanie błędów w konsoli (SyntaxError vs TypeError); `console.log` ze wglądem; **breakpointy** w zakładce Sources; przechodzenie krok po kroku | „błąd to nie porażka, to informacja” |
| 25' | **Ćwiczenie główne: dwa mini-programy** — (1) **Kalkulator BMI**: `prompt` → oblicz → wynik + kategoria (funkcja zwraca tekst); (2) **„Zgadnij liczbę”**: losowa liczba, pętla `while`, podpowiedzi „za dużo/za mało”, licznik prób (`Math.random` podany gotowo) | w konsoli; warianty A/B/C poniżej |
| 10' | **Podsumowanie + zapowiedź L2** (DOM: te funkcje przeniesiemy na prawdziwą stronę — przyciski, inputy, live zmiany) i zakres kartkówki | pokazać gotowy efekt L2 jako teaser |

### Ćwiczenia

- **A (podstawowy):** Kalkulator BMI z funkcją zwracającą wynik i kategorię.
- **B (rozszerzający):** + „Zgadnij liczbę” z licznikiem prób i grą na nowo.
- **C (gwiazdka):** + konwerter temperatur (°C ↔ °F) z wyborem kierunku (`prompt` + warunek) albo FizzBuzz w konsoli.

### Zadanie domowe (30–45 min)

1. Dokończ ćwiczenia A–B; przetestuj na brzegowych wartościach (0, liczba ujemna, bardzo duża).
2. Celowo zepsuj swój skrypt (usuń nawias), przeczytaj komunikat błędu, napraw — zapisz, co mówił błąd.
3. **Przygotuj się do kartkówki**: operatory i `===`, `if`/`else`, pętle, funkcje i `return`, arrow function.

### Powiązanie z INF.03

- Część pisemna regularnie sprawdza: wynik wyrażenia z `==`/`===`, działanie pętli, co zwraca funkcja — na kartkówce dokładnie ten format.
- W pracy praktycznej fragment JS (np. przeliczenie, walidacja) musi po prostu działać — dziś uczymy się pisać bez błędów składni.

### Akcent Akademia Tarnowska

Przy debugowaniu: „na studiach nikt nie pisze kodu bez błędów — debugowanie to codzienność programisty; dziś ćwiczycie supermoce, które na pierwszym roku dają przewagę”. Krótko.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na pierwsze spotkanie semestru letniego kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już (Z1–Z4): DevTools, HTML5 (semantyka, formularze, a11y), CSS3 (flexbox, grid, media queries, animacje), publikację GitHub Pages oraz PIERWSZE KROKI JS (konsola, let/const, typy, console.log, onclick/addEventListener w wersji „magia”, zmiana treści przez querySelector). Mieli przerwę semestralną — zacznij powtórką.
- Temat TEGO spotkania: JavaScript — solidne podstawy języka (operatory, warunki, pętle, funkcje, debugowanie).
- Następne spotkanie (L2): DOM i zdarzenia — te funkcje przeniesiemy na prawdziwą stronę. Zapowiedz to.
- Czas: 135 minut = kartkówka (10 min) + blok 1 (50 min) + przerwa (15 min) + blok 2 (60 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P”; min. 60% praktyki (dzisiaj: praca w konsoli DevTools).
- Kod kompletny i działający; komentarze po polsku; wyłącznie vanilla JS.
- Spinaj materiał z INF.03: wyniki wyrażeń, działanie pętli i zwracanie przez funkcje to klasyczne pytania testowe; kartkówka w formacie egzaminu.
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (np. debugowanie jako codzienność studenta IT), bez reklamy.

### Zakres merytoryczny spotkania
1. Rozgrzewka po przerwie semestralnej: konsola, let/const, console.log.
2. Operatory: arytmetyczne (+ - * / %), przypisanie (+=), inkrementacja; == vs === (zawsze ===); && || !; konkatenacja vs szablony ${}.
3. Warunki: if / else if / else, switch, truthy/falsy na przykładach.
4. Pętle: for, while, iterowanie, break; pętla nieskończona — jak powstaje.
5. alert/prompt/confirm — szybkie prototypy, dlaczego nie na produkcji.
6. Funkcje: deklaracja, parametry, return (undefined bez return), arrow function () => {}.
7. Debugowanie: czytanie błędów (SyntaxError vs TypeError), console.log, breakpointy w Sources.
8. Ćwiczenia główne: kalkulator BMI (funkcja zwraca wynik + kategorię) i „zgadnij liczbę” (Math.random, while, licznik prób).

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu Z4 (grid, media queries, GitHub Pages, podstawy JS): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 60) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO]; obowiązkowe slajdy: „co wypisze konsola?” (zagadki), schemat if/for, function vs arrow, „czytamy błędy”.
4. Materiały live coding: zagadki operatorów, BMI krok po kroku, zgadywanka krok po kroku.
5. Ćwiczenia A/B/C (A: BMI; B: + zgadywanka z licznikiem prób; C: konwerter temperatur albo FizzBuzz) z pełnymi rozwiązaniami.
6. Zadanie domowe (30–45 min): dokończenie ćwiczeń, testy brzegowe, „celowo zepsuj i napraw skrypt” + zakres kartkówki na L2 (operatory ===, if/else, pętle, funkcje i return, arrow function).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Każdy fragment kodu poprawny składniowo i przetestowany mentalnie (nawiasy, średniki, zwracane typy).
- Materiały gotowe do użycia na zajęciach bez dalszej edycji.
```
