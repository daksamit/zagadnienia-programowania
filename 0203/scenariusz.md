# 0203 · Tablice, obiekty i dane

| | |
|---|---|
| **Semestr** | letni - spotkanie 3 z 11 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 |
| **Poprzednie** | [0202 · DOM i zdarzenia](../0202/scenariusz.md) |
| **Następne** | [0204 · Projekt zintegrowany HTML + CSS + JS](../0204/scenariusz.md) |

## Overview

### Cel spotkania

- Uczeń pracuje z **tablicami** (dodawanie, iteracja) i najważniejszymi metodami (`map`, `filter`, `find` - na dostępnym poziomie).
- Modeluje dane w **obiektach** (właściwości, metody, dostęp `.kropką` i `["nawiasem"]`).
- Rozumie **JSON** - format, którym rozmawia cały internet.
- Zapisuje dane w **localStorage** - aplikacja pamięta po odświeżeniu (efekt: „wow, działa!”).
- Mierzy czas: `setTimeout`/`setInterval`.
- Ma pierwszy kontakt z **`fetch` i API** - strona pobiera prawdziwe dane z sieci.
- Wie, **jak działają PWA od kuchni** (service worker + manifest - w pigułce, bez implementacji).

### Kartkówka (10 min) - zakres: 0202

- `querySelector` vs `getElementById`; `textContent` vs `innerHTML`; `classList.toggle`; `addEventListener` i `event.target`; po co `preventDefault()`.
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Sekcja 1 (50 min) - struktury danych

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Tablice - podstawy** - tworzenie, indeks (od 0!), `length`, `push`/`pop`; iteracja `for` i `for...of` | live: lista zakupów / lista ocen w konsoli |
| 10' | **Metody tablic** - `map` (przekształć każdy), `filter` (zostaw pasujące), `find` (znajdź pierwszy); `join` do wyświetlenia | zasadniczo: pętle już umiemy - teraz narzędzia wyższego poziomu |
| 10' | **Obiekty** - literał `{ klucz: wartość }`, właściwości, metody, dostęp `.nazwa` i `["nazwa"]`; tablica obiektów (np. lista kontaktów) - najczęstszy kształt danych w sieci | diagram „obiekt = etykiety na pudełku” |
| 10' | **JSON** - `JSON.stringify` / `JSON.parse`; dlaczego JSON (tekst! wymienialny między systemami); podobieństwo do literału obiektu | pokaż prawdziwy JSON z publicznego API |
| 10' | **`localStorage`** - `setItem`/`getItem` (tylko stringi → JSON!); `removeItem`; zapis i odczyt stanu; ograniczenia (per przeglądarka, brak sekretów) | live: licznik z 0202, który pamięta wynik |

### Przerwa (15 min)

### Sekcja 2 (35 min) - czas, sieć, start aplikacji „Lista zadań”

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **`setTimeout` / `setInterval`** - opóźnione i cykliczne akcje (zegar na stronie, countdown, automatyczny slider); `clearInterval` | live: zegar HH:MM:SS |
| 10' | **`fetch` - pierwsze kroki** - co to API; `fetch(url)` → `.then(res => res.json())` → dane renderujemy na stronie; publiczne, bezkluczowe API (np. losowy cytat/porada, dane o walutach); obsługa błędu na razie trywialna (`.catch`) | pokazujemy, nie wgłębiamy się w asynchroniczność |
| 5' | **PWA od kuchni (wzmianka)** - „pamiętacie instalację strony z 0101?”: **manifest** (nazwa, ikony) + **service worker** (pracuje w tle, obsługuje offline); dziś nie implementujemy - wiecie, jak to się nazywa i po co | domknięcie wątku z 0101 |
| 10' | **Start ćwiczenia głównego: „Lista zadań” (todo)** - dodawanie zadania z inputa, render listy (`map` + `innerHTML`); uczniowie pracują samodzielnie, prowadzący pomaga indywidualnie | kompletna aplikacja - może być projekt na 0204! |

### Sekcja 3 (25 min) - domknięcie: „Lista zadań”, INF.03, podsumowanie

| Czas | Temat | Uwagi |
|---|---|---|
| 20' | **Ćwiczenie główne (cd.): „Lista zadań”** - odhaczanie zrobionych (`classList.toggle`), usuwanie, **zapis w localStorage** (JSON!) - po odświeżeniu wszystko wraca; warianty B/C dla szybkich | warianty A/B/C poniżej |
| 5' | **Podsumowanie + 5 pytań INF.03 + zadanie domowe + zapowiedź 0204** - projekt zintegrowany w zespołach (Git/GitHub, publikacja, prezentacje); podanie wymagań projektowych i zakresu kartkówki | |

### Ćwiczenia

- **A (podstawowy):** lista zadań: dodawanie + render + zapis w localStorage.
- **B (rozszerzający):** + odhaczanie zrobionych (przekreślenie) + usuwanie pojedynczych zadań.
- **C (gwiazdka):** + filtr „pokaż tylko niezrobione” (`filter`) + licznik pozostałych zadań + pobranie losowego cytatu przez `fetch` i wyświetlenie go w stopce.

### Zadanie domowe (30–45 min)

1. Dokończ listę zadań (poziom co najmniej B).
2. **Wybierz projekt na 0204** (solo lub w zespole 2–3 os.) i przygotuj 1-punktowy opis: co robi, jakie ma 2–3 funkcje. Lista propozycji przyjdzie od prowadzącego.
3. **Przygotuj się do kartkówki**: tablice (`push`, `length`, indeksy), `map`/`filter`, obiekty i dostęp do właściwości, `JSON.stringify/parse`, `localStorage`.

### Powiązanie z INF.03

- Tablice/obiekty i odczyt danych pojawiają się w pytaniach testowych (co zwraca `filter`?, jaki jest indeks pierwszego elementu?).
- Praca praktyczna: dane w formacie JSON to standard w zadaniach z witryną + bazą - dziś uczymy się je czytać i zapisywać.

### Akcent Akademia Tarnowska

Przy `fetch`/API: „dokładnie tak aplikacje studenckie na AT łączą się z systemami zewnętrznymi - to brama do pełnego stacku, który poznacie na studiach”. Jedno zdanie, konkretnie.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na trzecie spotkanie semestru letniego kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe - HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już: HTML5 + a11y, CSS3 (flexbox, grid, responsywność), podstawy JS (zmienne, warunki, pętle, funkcje arrow), DOM i zdarzenia (querySelector, classList, addEventListener, walidacja formularza, mini-projekty: licznik/galeria/quiz).
- Temat TEGO spotkania: tablice, obiekty, JSON, localStorage, setTimeout/setInterval, pierwszy kontakt z fetch i API + wzmianka o PWA (manifest + service worker - bez implementacji).
- Następne spotkanie (0204): warsztaty projektowe w zespołach (Git/GitHub, publikacja, prezentacje) - na koniec ogłoś wymagania projektowe.
- Czas: 135 minut = kartkówka (10 min) + sekcja 1 (50 min) + przerwa (15 min) + sekcja 2 (35 min) + sekcja 3 (25 min).

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Wzorzec „3×P”; min. 60% praktyki.
- Kod kompletny i działający; komentarze po polsku; wyłącznie vanilla JS; do fetch używaj publicznych API bez kluczy (np. losowy cytat/porada) i z podstawową obsługą błędu (.catch).
- Spinaj materiał z INF.03 (tablice/obiekty/JSON w pytaniach testowych; dane JSON w pracy praktycznej); kartkówka w formacie testu.
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (np. fetch jako brama do pełnego stacku ze studiów).

### Zakres merytoryczny spotkania
1. Tablice: tworzenie, indeks od 0, length, push/pop, iteracja for i for...of.
2. Metody: map, filter, find, join - na przystępnym poziomie, z analogiami.
3. Obiekty: literał, właściwości, metody, dostęp .nazwa i ["nazwa"]; tablice obiektów.
4. JSON: stringify/parse; dlaczego JSON (wymiana danych); podobieństwo do literału obiektu.
5. localStorage: setItem/getItem/removeItem; tylko stringi → JSON; ograniczenia.
6. setTimeout/setInterval/clearInterval (zegar, countdown, slider).
7. fetch: fetch(url).then(res => res.json()).then(...) - pobranie danych i render na stronie.
8. PWA od kuchni (wzmianka, bez kodu): manifest + service worker = instalacja i offline (domknięcie tematu z 0101).
9. Ćwiczenie główne: aplikacja „Lista zadań” - dodawanie, render (map + innerHTML), odhaczanie (classList.toggle), usuwanie, zapis w localStorage, odtwarzanie po odświeżeniu.

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu 0202 (querySelector vs getElementById, textContent vs innerHTML, classList, addEventListener, preventDefault): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 35 + 25) co 5–10 minut, z oznaczeniem live coding i pracy samodzielnej.
3. Prezentacja (12–18 slajdów): tytuł + 3–5 punktów + [NA ŻYWO]; obowiązkowe slajdy: „tablica obiektów” (jak wyglądają dane w sieci), localStorage krok po kroku, fetch - schemat przepływu, PWA: manifest + service worker.
4. Materiały live coding: (a) tablica obiektów w konsoli; (b) zapis/odczyt localStorage; (c) zegar z setInterval; (d) fetch cytatu i render; (e) lista zadań budowana krok po kroku.
5. Ćwiczenia A/B/C (poziomy jak w zakresie pkt 9; C: filtr niezrobionych + licznik + cytat z API w stopce) z pełnymi rozwiązaniami - kompletne pliki HTML+CSS+JS.
6. Zadanie domowe (30–45 min): dokończenie listy zadań (min. poziom B) + wybór pomysłu na projekt 0204 (opis 1 akapit: co robi, 2–3 funkcje) + zakres kartkówki na 0204 (tablice, map/filter, obiekty, JSON.parse/stringify, localStorage).
7. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Kod przetestowany mentalnie: poprawne nazwy metod, domknięte then/catch, JSON w localStorage.
- Materiały gotowe do użycia na zajęciach bez dalszej edycji.
```
