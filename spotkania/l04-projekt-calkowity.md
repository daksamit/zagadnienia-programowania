# L4 · Projekt zintegrowany HTML + CSS + JS

| | |
|---|---|
| **Semestr** | letni — spotkanie 4 z 11 (grupy A/B) |
| **Czas** | 135 min = **kartkówka 10** + blok 50 + przerwa 15 + blok 60 |
| **Poprzednie** | [L3 · Tablice, obiekty i dane](l03-js-dane.md) |
| **Następne** | [L5 · INF.03 — trening egzaminacyjny i co dalej](l05-inf03-trening.md) |

## Overview

### Cel spotkania

- Uczniowie **planują i budują kompletny projekt** (HTML + CSS + JS) w zespołach 2–3 osobowych — od pomysłu po publikację.
- Poznają **minimum Git/GitHub**: `init`/`clone` (albo fork), `add`, `commit`, `push` — „cztery komendy, które zmieniają świat” (przypomnienie: Pages już znają z Z4).
- Trenują **pracę zespołową**: podział zadań, wspólny plik stylów, konflikty łagodzimy rozmową.
- **Prezentują projekt** (2 minuty na zespół) i uczą się opisać go w portfolio/CV.

To spotkanie ma format **warsztatów projektowych** — minimum wykładu, maksimum pracy uczniów. Prowadzący krąży i pomaga (coach, nie wykładowca).

### Kartkówka (10 min) — zakres: L3

- Tablice: indeksowanie, `push`, `length`; co robi `map`/`filter`; dostęp do właściwości obiektu; `JSON.parse` vs `JSON.stringify`; `localStorage` (jakie typy można zapisywać?).
- Format: 4–5 pytań, w tym min. 2 zamknięte (A–D) w stylu INF.03; klucz + punktacja.

### Blok 1 (50 min) — start projektu

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Ramy projektu** — przypomnienie wymagań (poniżej); przypomnienie propozycji pomysłów; dobór zespołów i wybór pomysłu; **kontrakt zespołu**: kto co robi (3 role: struktura/HTML, style/CSS, logika/JS — role mogą się mieszać) | pomysły przygotowane w zadaniu domowym z L3 |
| 10' | **Planowanie na kartce** — szkic ekranu (mobile-first!), lista funkcji („MUST” vs „MAYBE”), struktura plików: `index.html`, `style.css`, `script.js`, katalog `img/` | nie zaczynamy kodować bez szkicu! |
| 10' | **Git w 15 minut — część 1** — po co Git (historia, praca zespołowa, portfolio!); GitHub: repozytorium projektu; najprostsza droga: edycja w VS Code → `git add .` → `git commit -m "..."` → `git push` | jeśli komendy zawadzają — tym razem może być drag&drop przez stronę GitHuba, ale komendy pokazujemy |
| 20' | **Sprint 1: szkielet działa** — HTML semantyczny + nawigacja + pierwsza sekcja ostylowana; demo na Live Server; `commit` po każdym małym kroku | prowadzący przechodzi między zespołami |

### Przerwa (15 min)

### Blok 2 (60 min) — budowa, publikacja, prezentacje

| Czas | Temat | Uwagi |
|---|---|---|
| 30' | **Sprint 2: funkcje JS** — interakcje (zdarzenia, DOM, localStorage/fetch — wszystko z L1–L3); testowanie na telefonie (device toolbar); kolejne `commit`/`push` | prowadzący: debugowanie zamiast poprawiania za uczniów |
| 10' | **Publikacja** — GitHub Pages z repozytorium projektu; test na telefonie **na żywo** (sieć!); poprawki ostatniej chwili | moment dumy #2 |
| 15' | **Prezentacje** — 2 min/zespół: co robi projekt, co było trudne, co dalej poprawicie; klasa klaska, prowadzący notuje plusy | wymóg: każdy zespół mówi, nie jeden prelegent |
| 5' | **Portfolio w 3 zdaniach** — jak opisać projekt na CV/LinkedIn (problem → rozwiązanie → technologie); **zapowiedź L5** (trening INF.03: arkusz, strategia, co dalej po technikum) i zakres kartkówki | |

### Wymagania projektu (kryteria oceny)

Projekt **musi** (MUST): mieć semantyczny HTML, responsywność (media queries), min. 2 interakcje JS (zdarzenia + DOM), być opublikowany na GitHub Pages, być prezentowany przez cały zespół.
Projekt **może** (MAYBE — na wyższą ocenę): localStorage lub fetch, walidacja formularza, animacje CSS, dbałość o a11y (kontrast, alt, Tab).

**Propozycje pomysłów:** quiz z kategoriami · memo (gra pamięciowa) · kalkulator (BMI/kalorie/waluty) · lista zadań rozszerzona · kamień-papier-nożyce lub wisielec · strona-wizytówka zespołu/kluby z interakcjami · mini „sklep” z koszykiem w localStorage · własny pomysł (zaaprobowany przez prowadzącego).

### Ćwiczenia

Ćwiczeniem jest projekt — warianty zależą od zakresu: **A** = wszystkie MUST; **B** = MUST + 2 pozycje z MAYBE; **C** = MUST + 3+ MAYBE i „polish” (dobre UX na telefonie).

### Zadanie domowe (30–45 min)

1. Dokończ/dopieść projekt — **przed L5 prezentacja finalna** (materiał na zakończenie kursu).
2. Napisz 3-zdaniowy opis projektu pod CV (problem → rozwiązanie → technologie).
3. **Przygotuj się do kartkówki**: kroki publikacji GitHub Pages, komendy `add/commit/push`, po co Git, podział ról w projekcie, MUST/MAYBE projektu.

### Powiązanie z INF.03

- Praca praktyczna to projekt „od zera do działającej witryny pod specyfikację” — dziś uczniowie przechodzą ten proces w skali (plan → budowa → publikacja → prezentacja).
- Kultura `commitów` małych kroków ratuje na egzaminie praktycznym (i w każdej pracy zawodowej).

### Akcent Akademia Tarnowska

Przy portfolio: „projekt na GitHubie to pierwsza rzecz, na którą patrzymy u kandydatów na studia i u studentów na praktyki — zaczęliście budować swoje dziś”. Konkret, jedno zdanie.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym. Przygotuj kompletny pakiet materiałów dydaktycznych na czwarte spotkanie semestru letniego kursu webdevelopmentu — WARSZTATY PROJEKTOWE.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, 18–19 lat).
- Uczniowie znają już: HTML5 + a11y, CSS3 (flexbox, grid, responsywność, animacje), JS (podstawy języka, DOM, zdarzenia, formularze z walidacją, tablice/obiekty/JSON, localStorage, setTimeout/setInterval, podstawy fetch), publikację GitHub Pages. W zadaniu domowym z L3 wybrali pomysł na projekt (solo lub zespoły 2–3 os.).
- Temat TEGO spotkania: projekt zintegrowany HTML+CSS+JS w zespołach: planowanie, Git/GitHub (add/commit/push), budowa (2 sprinty), publikacja, prezentacje, opis projektu pod portfolio/CV.
- Następne spotkanie (L5): trening egzaminacyjny INF.03 (strategia, test próbny, mini-arkusz praktyczny) + ścieżki rozwoju i rekrutacja na Akademię Tarnowską. Zapowiedz je.
- Czas: 135 minut = kartkówka (10 min) + blok 1 (50 min) + przerwa (15 min) + blok 2 (60 min).
- Format: warsztaty — minimum wykładu (Git: łącznie ok. 15 min), maksimum pracy uczniów; prowadzący jako coach krążący między zespołami.

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny; odbiorca: technikum. Praktyka ≥ 80% tego spotkania.
- Kod kompletny i działający; komentarze po polsku; wyłącznie HTML/CSS/vanilla JS.
- Spinaj materiał z INF.03: proces „plan → budowa → publikacja” odzwierciedla pracę praktyczną; małe commity = bezpieczeństwo na egzaminie.
- Subtelna promocja Akademii Tarnowskiej: jeden konkretny akcent (projekt na GitHubie jako pierwsza rzecz oglądana u kandydatów/studentów na praktyki).

### Zakres merytoryczny spotkania
1. Ramy projektu i kontrakt zespołu (role: HTML / CSS / JS).
2. Planowanie: szkic ekranu mobile-first, lista funkcji MUST/MAYBE, struktura plików.
3. Git minimum: po co; add/commit/push; repozytorium na GitHub; dopuszczalna droga przez stronę (drag&drop), ale komendy pokazane.
4. Sprint 1: szkielet (HTML semantyczny + nawigacja + pierwsza sekcja).
5. Sprint 2: funkcje JS (zdarzenia, DOM, opcjonalnie localStorage/fetch), testy device toolbar.
6. Publikacja GitHub Pages + test na telefonie.
7. Prezentacje 2 min/zespół (mówi cały zespół).
8. Portfolio w 3 zdaniach: problem → rozwiązanie → technologie.
9. Wymagania projektu — MUST: semantyczny HTML, responsywność, min. 2 interakcje JS, publikacja, prezentacja zespołu; MAYBE: localStorage/fetch, walidacja, animacje, a11y.

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Kartkówka (10 min) z zakresu L3 (tablice, map/filter, obiekty, JSON, localStorage): 4–5 pytań, min. 2 zamknięte A–D w formacie INF.03 + 1–2 otwarte; klucz, punktacja 0–5, skala ocen.
2. Konspekt z rozpiską czasową (10 + 50 + 15 + 60) co 5–10 minut — z wyraźnym oznaczeniem momentów: kontrakt zespołu, oba sprinty, publikacja, prezentacje.
3. Prezentacja (8–12 slajdów — krótko!): zasady projektu, MUST/MAYBE, Git w 4 komendach, plan sprintów, punktacja projektu, „portfolio w 3 zdaniach”.
4. Materiały wsparcia: (a) szablon kontraktu zespołu (do wydruku); (b) checklista przed publikacją; (c) 3 przykładowe szkice ekranów dla trzech pomysłów; (d) ściągawka komend Git (init/clone, add, commit -m, push + GitHub Pages).
5. „Karty pomocy” dla prowadzącego: 5 najczęstszych problemów zespołów (nic nie działa po podmianie plików, konflikt stylów, script.js nie widzi elementów, przecinek/poważny błąd składni, „u mnie działa”) + jak reagować pytaniem, nie rozwiązaniem.
6. Ćwiczenia: zdefiniowane poziomy projektu A (MUST), B (MUST + 2 MAYBE), C (MUST + 3+ MAYBE i polish) + przykładowe kryteria oceny punktowanej (tabela 0–20 pkt).
7. Zadanie domowe (30–45 min): dopieszczenie projektu przed finałem, opis pod CV, zakres kartkówki na L5 (GitHub Pages, add/commit/push, po co Git, role zespołu, MUST/MAYBE).
8. 5 pytań w stylu INF.03 z zakresu TEGO spotkania (zamknięte A–D) z kluczem i krótkim uzasadnieniem.

### Jakość
- Komendy Git poprawne i działające w opisanym środowisku (VS Code + GitHub, HTTPS).
- Materiały gotowe do użycia na zajęciach bez dalszej edycji.
```
