# 0101 · PLAN zajęć - „Dlaczego web? Wstęp, przeglądarki i DevTools"

| | |
|---|---|
| **Semestr** | zimowy 2026 - spotkanie 1 z 9 |
| **Realizacja** | 07 X 2026 (grupa B) · 21 X 2026 (grupa A) |
| **Czas** | 135 min = ankieta zapoznawcza 10 (nieoceniana) + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 - tj. **3 bloki** (między nimi 5-minutowe przerwy wg dzwonków) |
| **Prowadzący** | mgr inż. Dominik Aksamit - Akademia Tarnowska |
| **Materiały** | Pakiet prowadzącego (ten katalog): [scenariusz.md](scenariusz.md) (+ wariant [ADEPT](scenariusz-adept.md)) · [konspekt.md](konspekt.md) (rozpiska co 2–15 min) · [prezentacja.md](prezentacja.md) (20 slajdów; wersje HTML: [prezentacja.html](prezentacja.html), [prezentacja-czytana.html](prezentacja-czytana.html)) · [ankieta-zapoznawcza.md](ankieta-zapoznawcza.md) (rozdrukka) · [rozwiazania/](rozwiazania/README.md) (**tylko prowadzący**) · **pakiet ucznia**: [../0101/](../0101/README.md) - instrukcja z planem spotkania, ściąga, poradnik, mini-ściąga „AI jako tutor" |

## Nazwy bloków (wpisy do dziennika)

| Blok | Czas | Nazwa |
|---|---|---|
| 1 | 0:00–0:45 | „Dlaczego web? Historia WWW i działanie internetu" |
| 2 | 0:45–1:30 | „Przeglądarki internetowe i Chrome DevTools" |
| 3 | 1:30–2:15 | „Warsztat programisty: VS Code i pierwsza strona HTML" |

Wpis dla bloku 1 może zaczynać się od „Ankieta zapoznawcza." - ankieta to forma diagnozy grupy, nie temat.

Granica bloków 2/3 (1:30) przecina praktykę DevTools (1:20–1:35). Naturalny punkt cięcia: **do 1:30 domknij wrażenia z zadań** (krok „zbierz 2–3 wrażenia" z konspektu), a blok 3 otwórz warsztatem VS Code - ten blok jest samowystarczalny. Jeśli klasa kończy zadania szybciej, po prostu przejdź do warsztatu wcześniej.

## Cel spotkania - po zajęciach uczeń:

- wie, jak wyglądają zajęcia: 135 min, kartkówki od 0102 (oceny cząstkowe → ocena na koniec roku), sprawdzian semestralny na 0104 zamiast kartkówki,
- rozumie na zweryfikowanych liczbach, dlaczego technologie webowe warto znać,
- potrafi wyjaśnić w pigułce: klient–serwer, DNS, HTTP(S), URL, renderowanie strony,
- otwiera Chrome DevTools, edytuje HTML/CSS na żywo i wie, że zmiany są lokalne,
- ma przygotowany warsztat: VS Code + Live Server + katalog projektu z `index.html` (alternatywnie StackBlitz/CodeSandbox),
- zna sposoby uczciwej nauki z AI i ma mini-ścięgę z gotowymi promptami,
- napisał swoją pierwszą stronę HTML5 i zaczął ćwiczenie „Kim jestem".

## Agenda

### Blok 1 · 0:00–0:45 - „Dlaczego web? Historia WWW i działanie internetu"

| Czas | Blok | Forma |
|---|---|---|
| 0:00–0:10 | **Ankieta zapoznawcza** - 3 pytania otwarte o AI; nieoceniana, diagnoza poziomu grupy; przejrzyj odpowiedzi w przerwie | PRACA SAMODZIELNA |
| 0:10–0:15 | Przedstawienie się i zasady: 135 min w 3 sekcjach, kartkówki od 0102, oceny cząstkowe → ocena roczna, sprawdzian semestralny 0104 | - |
| 0:15–0:20 | **Mikro-historia WWW** (max 5 min!): 1989 Berners-Lee/CERN · 1991 pierwsza strona (nadal działa) · 1995 JavaScript | DEMO · info.cern.ch |
| 0:20–0:30 | **Web w liczbach** - każda liczba ze źródłem i rokiem: JS nr 1 od 13 lat · 98,9% stron · 1,2 mld stron · Chrome 70–72% · 84% programistów z AI | - |
| 0:30–0:35 | **PWA**: strona jak aplikacja - instalacja z przeglądarki, offline; Photopea | DEMO · instalacja PWA |
| 0:35–0:45 | **Jak działa internet**: klient–serwer (restauracja), DNS (książka telefoniczna), HTTP(S), URL, CDN, renderowanie | DEMO · strona szkoły |

**Kluczowe punkty i pułapki (baza kartkówki 0102):** DNS = nazwa → adres IP · HTTPS = szyfrowanie (kłódka) · URL = schemat + host + ścieżka · lata 1989/1991/1995.

### Blok 2 · 0:45–1:30 - „Przeglądarki internetowe i Chrome DevTools"

| Czas | Blok | Forma |
|---|---|---|
| 0:45–0:50 | **Przeglądarki i silniki**: Blink/WebKit/Gecko; „u mnie działa" to za mało - standard kursu: Chrome | - |
| 0:50–1:00 | **Mapa semestru + INF.03** (test 40 zadań + praca praktyczna) · **akcent Akademii Tarnowskiej** (jedno zdanie) | - |
| 1:00–1:15 | **Przerwa** - w jej trakcie przejrzyj ankiety: skalibruj głębokość bloku „AI jako tutor" | - |
| 1:15–1:20 | **DevTools - wprowadzenie**: F12, Elements ↔ strona, edycja tekstu i koloru na żywo | DEMO |
| 1:20–1:30 | **DevTools w praktyce (start)**: zmiana tekstu/kolorów, ukrywanie elementów (H), device toolbar, Console (`2 + 2`, `document.title`) | PRACA SAMODZIELNA |

**Kluczowe punkty i pułapki:** Elements = podgląd i edycja **lokalna** · F5 pobiera pliki ponownie z serwera - zmiany znikają.

### Blok 3 · 1:30–2:15 - „Warsztat programisty: VS Code i pierwsza strona HTML"

| Czas | Blok | Forma |
|---|---|---|
| 1:30–1:35 | DevTools w praktyce (coda): F5 = wszystko wraca; zbierz 2–3 wrażenia | PRACA SAMODZIELNA |
| 1:35–1:40 | **Warsztat VS Code + Live Server**: `file://` vs `http://127.0.0.1:5500` vs `https://…` (tabela „trzy adresy, jedna strona"); alternatywa: StackBlitz/CodeSandbox | DEMO + uczniowie równolegle |
| 1:40–1:50 | **AI jako tutor**: prompt „na lenia" vs ekspercki · ELI5 i metody nauki · zasady uczciwego użycia · **rozdanie mini-ściągi** · **przekaz o narzędziach** (notatki w konspekcie) | PREZENTACJA + dyskusja |
| 1:50–2:05 | **Live coding: pierwsza strona HTML** - szkielet → `h1`/`p` → lista → link → obrazek | LIVE CODING · etapy 1–5 |
| 2:05–2:12 | Ćwiczenie „Kim jestem" - warianty A/B/C (B: obrazek z `alt` + `ol`; C: przeróbka strony w DevTools, zrzut przed/po) | PRACA SAMODZIELNA |
| 2:12–2:15 | Domknięcie: podsumowanie rundą · zadanie domowe · zapowiedź 0102 + **zakres kartkówki** | - |

**Kluczowe punkty i pułapki:** szkielet = `<!DOCTYPE html>` + `html lang="pl"` + `head` (charset, viewport, `title`) + `body` · `127.0.0.1` = localhost = „ten komputer".

## Logistyka - przed zajęciami

- [ ] Chrome + VS Code z rozszerzeniem **Live Server** na komputerach uczniowskich i prowadzącego.
- [ ] **Rozdrukki ankiety zapoznawczej** - po 1 egzemplarzu na ucznia ([ankieta-zapoznawcza.md](ankieta-zapoznawcza.md), nieoceniana, bez klucza).
- [ ] **Rozdrukki mini-ściągi „AI jako tutor"** - po 1 egzemplarzu na ucznia ([../0101/ai-jako-tutor-sciega.md](../0101/ai-jako-tutor-sciega.md)).
- [ ] **Pakiet ucznia** ([../0101/](../0101/README.md)) - udostępnij przed zajęciami (zip / pendrive / dysk klasowy); zawiera instrukcję z planem spotkania, ściągę, poradnik i ścięgę AI.
- [ ] Projektor czytelny z ostatniej ławki (powiększ czcionkę w VS Code i Chrome).
- [ ] Przetestuj linki: `zst.tarnow.pl`, `photopea.com`, `info.cern.ch`, `picsum.photos`, `stackblitz.com` / `codesandbox.io`.
- [ ] Otwarte karty na start: prezentacja + strona szkoły + photopea.com.
- [ ] **Plan B offline:** obrazek do live codingu lokalnie (`obrazek.jpg`); demo PWA i info.cern.ch → zrzuty ekranu.

## Linki - źródła i narzędzia

**Statystyki „web w liczbach" (odśwież u źródła przed każdym terminem; pełna tabela: [../README.md](../README.md), sekcja „Technologie webowe w liczbach"):**

- Stack Overflow Developer Survey 2025 (JS nr 1 od 13 lat, ~66%; 84% z AI): https://survey.stackoverflow.co/2025/technology
- W3Techs - JavaScript na 98,9% stron: https://w3techs.com/technologies/details/cp-javascript
- Internet Live Stats - ponad 1,2 mld stron: https://www.internetlivestats.com/total-number-of-websites/
- StatCounter - Chrome ~70–72%: https://gs.statcounter.com/browser-market-share/all/worldwide/2025

**Demo na zajęciach:**

- Pierwsza strona WWW (1991, nadal działa): http://info.cern.ch/hypertext/WWW/TheProject.html
- Photopea - PWA-owy „Photoshop w przeglądarce": https://www.photopea.com
- Edytory w przeglądarce (uczniowie bez VS Code): https://stackblitz.com · https://codesandbox.io

## Domknięcie dnia - obowiązki wynikające ze spotkania

- **Zadanie domowe (30–40 min):** dokończ „Kim jestem" · „detektyw stron": podejrzyj 2–3 ulubione strony w DevTools (Elements) · wypróbuj 2 prompty ze ściągi AI (np. ELI5: „jak działa DNS").
- **Zakres kartkówki na 0102:** historia WWW · klient–serwer (DNS, HTTP(S), URL, 127.0.0.1/localhost) · Chrome DevTools · szkielet HTML.
- **Kontynuacja:** projekt „Kim jestem" nie wraca na 0102 - ale **warsztat** (VS Code + Live Server, otwieranie projektu) jest potrzebny od 0102 na każdym spotkaniu; fanpage z 0102 będzie nowym projektem.
- **Wyniki ankiety:** przejrzyj przed 0102 - jeśli grupa zna pojęcia AI, blok „AI jako tutor" na kolejnych spotkaniach można skracać na rzecz praktyki.
- **Akcent Akademii Tarnowskiej** (jedno zdanie, w Sekcji 1 przy mapie semestru): „To samo, co będziecie robić na zajęciach, nasi studenci na Akademii Tarnowskiej robią na projektach i praktykach - na końcu semestru pokażę wam, jak to wygląda od kuchni."

## Alternatywne nazwy bloków (do wyboru przy wpisie)

| Blok | Wariant krótki | Wariant chwytliwy |
|---|---|---|
| 1 | „Wstęp do zajęć i jak działa internet" | „Od CERN-u do Twojej przeglądarki" |
| 2 | „Przeglądarki i DevTools" | „F12 - pod maskę dowolnej strony" |
| 3 | „Pierwsza strona w VS Code" | „Warsztat gotowy: piszemy pierwszą stronę" |
