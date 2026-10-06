# Z1 (ADEPT) · Dlaczego web? Wstęp, przeglądarki i DevTools

> Alternatywna wersja scenariusza [z01-wstep-przegladarki-devtools.md](z01-wstep-przegladarki-devtools.md) wzięta pod kątem metody ADEPT (analogia → diagram → przykład → definicja prosta → definicja techniczna). Struktura czasowa i zakres merytoryczny identyczne z wersją bazową; różnica: kluczowe pojęcia mają rozpisaną pełną ścieżkę ADEPT.

| | |
|---|---|
| **Semestr** | zimowy — spotkanie 1 z 9 (grupy A/B) |
| **Czas** | 135 min = blok 60 + przerwa 15 + blok 60 (**bez kartkówki** — spotkanie otwierające kurs) |
| **Wariant** | ADEPT (wg [AGENTS-adept.md](../AGENTS-adept.md)) |
| **Następne spotkanie** | [Z2 · HTML5 — fundamenty i semantyka](z02-html5-fundamenty.md) (zaczyna się kartkówką z tego spotkania) |

## Pojęcia-bramy tego spotkania (pełna ścieżka ADEPT)

1. **Klient–serwer** (z HTTP w tle)
2. **DNS**
3. **DevTools (inspekcja strony)**
4. **Szkielet dokumentu HTML**

Pozostałe elementy (historia WWW, statystyki, PWA, przeglądarki i silniki, VS Code, AI jako tutor) prowadzimy jak w wersji bazowej — bez rozwijania ADEPT.

---

## Blok 1 (60 min) — wstęp, liczby, kontekst

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Przedstawienie się i zasady** — kim jestem (ścieżka: studia → praca w IT → Akademia Tarnowska), jak wyglądają zajęcia: 135 min, od Z2 kartkówka na start, przerwa w środku, pytania w każdej chwili | budujemy relację, nie wykład |
| 5' | **Mikro-historia WWW** — 1989: Tim Berners-Lee propozycja w CERN; 1991: pierwsza strona; 1995: JavaScript; dziś: ponad 1,2 mld stron | krótko! to ciekawostka, nie program zajęć |
| 10' | **Dlaczego warto: web w liczbach** — JS nr 1 po raz 13. (Stack Overflow 2025, ~66% respondentów), 98,9% stron (W3Techs 2026), 1,2 mld stron (Internet Live Stats), Chrome ~70–72% (StatCounter 2025), 84% programistów używa AI (Stack Overflow 2025) | każdy numer ze źródłem na slajdzie |
| 5' | **PWA — strona „natywna"** — instalacja z przeglądarki, działanie offline, powiadomienia; przykłady (Starbucks, Twitter/X Lite); demo: instalacja PWA z paska adresu | „wow", 3 zdania teorii max |
| 15' | **Jak działa internet w pigułce — ADEPT: klient–serwer + DNS** | rozpisanie poniżej |
| 10' | **Przeglądarki** — co robi przeglądarka; udziały: Chrome ~70–72%, Safari, Edge, Firefox (StatCounter 2025); silniki: Blink, WebKit, Gecko; dlaczego testujemy na kilku | nawiązanie: „dlaczego strona u klienta działa inaczej" |
| 10' | **Mapa semestru + INF.03 + AT** — Z2 HTML5, Z3 CSS3, Z4 CSS w praktyce + publikacja + pierwszy JS; semestr letni: JS → DOM → dane → projekt zespołowy → trening INF.03; egzamin w skrócie | slajd „mapa semestru"; akcent AT: jak te technologie wykorzystujemy ze studentami |

### Rozpiska ADEPT: klient–serwer + DNS (15')

**A — Analogia (2'):**
- Zamawiasz pizzę przez telefon. Ty = **klient** (prosisz), pizzeria = **serwer** (dostarcza). Nie interesuje Cię, jak pizzeria piecze — dostajesz gotowy produkt.
- DNS = **książka telefoniczna**: znasz nazwę (adres strony), nie znasz numeru (adresu IP). Książka podpowiada numer, zanim dodzwonisz się do pizzerii.

**D — Diagram (3')** — na slajdzie/tablicy:

```text
Ty (przeglądarka)                        Serwer (np. Wikipedia)
   │                                            ▲
   │ 1. „jaki IP ma wikipedia.org?"             │
   ▼                                            │
 DNS ──► „IP: 185.15.59.224"                    │
   │                                            │
   │ 2. „GET /strona"  ────────────────────────►│
   │◄──────────────────── 3. HTML + CSS + JS ───┘
   │
   ▼ 4. przeglądarka rysuje stronę
```

**E — Przykład (5'):**
- Prowadzący otwazuje stronę szkoły i pokazuje w DevTools (Network, po wcześniejszym 20-sekundowym teaserze — pełny warsztat DevTools jest w bloku 2): request do serwera, status 200, rozmiar pobranych plików. Uczniowie widzą, że „strona" to w rzeczywistości zestaw plików pobranych z serwera.

**P — definicja prosta (2'):**
- **Klient–serwer:** klient prosi, serwer daje. W sieci klientem jest przeglądarka, serwerem komputer, na którym leży strona.
- **DNS:** system, który tłumaczy nazwy stron (wikipedia.org) na adresy IP komputerów (185.15.59.224).

**T — definicja techniczna (3'):** (zapisuje się na slajdzie — w tej formie wraca na kartkówkę)
- **Model klient–serwer:** model obliczeń rozproszonych, w którym klient wysyła żądanie (np. HTTP `GET`), a serwer je przetwarza i odsyła odpowiedź (np. dokument HTML).
- **DNS (Domain Name System)**: rozproszona baza danych tłumacząca nazwy domen na adresy IP.
- **HTTP(S):** protokół warstwy aplikacji służący do przesyłania dokumentów hipertekstowych; HTTPS = HTTP z szyfrowaniem (TLS).

## Przerwa (15 min)

## Blok 2 (60 min) — warsztat: DevTools, narzędzia, AI, pierwsza strona

| Czas | Temat | Uwagi |
|---|---|---|
| 20' | **Chrome DevTools — ADEPT: inspekcja strony** | rozpiska poniżej; każdy uczeń sam modyfikuje wybraną stronę |
| 5' | **Warsztat** — VS Code + rozszerzenie Live Server; struktura projektu: katalog + `index.html` | jeśli sala gotowa, skrócić do 2' |
| 10' | **AI jako Twój tutor** — porównanie promptów („utwórz stronę i daj linka" vs „zaprojektuj wizytówkę z a11y, SEO, Git, Netlify, Astro"); jak się uczyć z AI (ELI5, pytania kontrolne, „znajdź błąd"); zasady: AI się myli, kartkówki bez AI, używaj do zrozumienia | mini-ściąga z promptami = element zadania domowego |
| 15' | **Live coding: pierwsza strona — ADEPT: szkielet dokumentu HTML** | rozpiska poniżej; uczniowie piszą razem z prowadzącym |
| 10' | **Ćwiczenie samodzielne** — mini-strona „Kim jestem" (3 sekcje); zapowiedź Z2 + **zakres kartkówki**: historia WWW, klient–serwer/DNS, DevTools, szkielet HTML | obsłuż szybkich wariantem C |

### Rozpiska ADEPT: DevTools (20')

**A — Analogia (2'):**
- Rentgen strony. Z zewnątrz widzisz efekt; DevTools pokazuje „kości" (HTML) i „skórę" (CSS). Jak lekarz prześwietlenie — patrzysz pod powierzchnię.
- Bonus: edycja w DevTools to **przymierzanie ubranu w sklepie** — możesz zobaczyć, jak leży, ale nie kupujesz (zmiany znikają po odświeżeniu).

**D — Diagram (3'):**

```text
┌─ Przeglądarka ──────────────────────────┐
│  ┌─ Okno strony (to, co widzi użytkownik)│
│  │                                        │
│  │   ┌─ DevTools (F12) ──────────────┐   │
│  │   │ Elements  → szkielet HTML     │   │
│  │   │ Styles   → reguły CSS         │   │
│  │   │ Console  → komunikaty JS      │   │
│  │   │ Device   → podgląd mobilny    │   │
│  │   └───────────────────────────────┘   │
└───┴────────────────────────────────────────┘
```

**E — Przykład (12'):** — sedno bloku, najdłuższy krok
1. Otwarcie: F12 / Ctrl+Shift+I / menu → Więcej narzędzi.
2. Panel **Elements**: prowadzący na żywo zmienia nagłówek i kolor dowolnej strony (np. strony szkoły).
3. Każdy uczeń: wybiera własną ulubioną stronę, zmienia tytuł i kolor tła.
4. **Console**: pierwsza komenda (np. `2 + 2`, `document.title`).
5. **Device toolbar**: podgląd mobilny.
6. Punchline: odświeżenie przywraca oryginał — zmiany są tylko lokalne, w Twojej przeglądarce.

**P — definicja prosta (1'):**
- DevTools to wbudowany w przeglądarkę zestaw narzędzi do podejrzenia i tymczasowej zmiany dowolnej strony: struktury (HTML), wyglądu (CSS) i zachowania (JS).

**T — definicja techniczna (2'):**
- **Narzędzia deweloperskie (DevTools)** — zintegrowane z przeglądarką środowisko diagnostyczne umożliwiające inspekcję modelu dokumentu (DOM), edycję arkuszy stylów w czasie rzeczywistym, wykonywanie kodu JavaScript w konsoli oraz symulację urządzeń mobilnych. Zmiany wprowadzone lokalnie nie modyfikują plików na serwerze.

### Rozpiska ADEPT: szkielet dokumentu HTML (15' live coding)

**A — Analogia (2'):**
- Dokument HTML jak **człowiek w gablocie**: `<head>` to metryka (dane o dokumencie — nie widać ich na pierwszy rzut oka: kodowanie, tytuł karty), `<body>` to to, co widać (treść). A `<!DOCTYPE html>` to Tablica przy wejściu: „ten budynek jest typu HTML5" — przeglądarka od razu wie, jak czytać resztę.

**D — Diagram (3'):** — rysowane równolegle z pisaniem kodu

```text
<!DOCTYPE html>          ← „to jest HTML5"
<html lang="pl">         ← początek dokumentu, język polski
├── <head>               ← metryka (niewidoczna)
│   ├── <meta charset="UTF-8">   ← polskie znaki działają
│   ├── <meta viewport>          ← strona działa na telefonie
│   └── <title>          ← napis na karcie przeglądarki
└── <body>               ← treść (widoczna)
    ├── nagłówki, akapity
    ├── lista, link
    └── obrazek
</html>
```

**E — Przykład (8'):** — live coding, uczniowie piszą razem
1. VS Code: nowy plik `index.html`, Live Server uruchomiony.
2. Budowa krok po kroku: DOCTYPE → `html lang="pl"` → `head` (charset, viewport, title) → `body` (nagłówek `h1`, akapity, lista `ul`/`li`, link `a href`, obrazek `img src` + `alt`).
3. Po każdym kroku zapis i rzut oka na podgląd w Live Server — uczniowie widzą skutek natychmiast.
4. Eksperyment: usuń `meta charset` → polskie znaki się sypią; przywróć. Analogia z metryką staje się konkret.

**P — def. prosta (1'):**
- Dokument HTML to plik tekstowy ze znacznikami w `<>`: te w `<head>` opisują stronę przeglądarce, te w `<body>` to jej widoczna treść.

**T — def. techniczna (1'):** — wraca na kartkówkę
- **Dokument HTML5** rozpoczyna się deklaracją `<!DOCTYPE html>`; korzeń stanowi element `<html>` z atrybutem `lang`, zawierający dokładnie jeden `<head>` (metadane: `charset`, `viewport`, `title`) i jeden `<body>` (treść renderowana przez przeglądarkę).

## Ćwiczenia

- **A (podstawowy):** strona „Kim jestem" — nagłówek, 2–3 akapity o sobie, lista zainteresowań, link do ulubionej strony.
- **B (rozszerzający):** dodaj obrazek (optymalizowany!) i drugą podstronę/sekcję „Moje cele na ten rok".
- **C (gwiazdka):** w DevTools zmień na żywo tytuł i kolory ulubionej strony; zrób zrzut ekranu przed/po.

## Zadanie domowe (30–40 min)

1. Dokończ stronę „Kim jestem".
2. Znajdź 2–3 strony, które Ci się podobają — podejrzyj je w DevTools (Elements) i zastanów się, z czego są zbudowane.
3. Wypróbuj 2 prompty z mini-ściągi „AI jako tutor" (np. ELI5 na temat „jak działa DNS").
4. **Przygotuj się do kartkówki**: historia WWW, klient–serwer i DNS, DevTools, szkielet HTML — definicje techniczne ze slajdów są podstawą pytań.

## Powiązanie z INF.03

- Zapowiedź struktury egzaminu (test 40 zadań + praca praktyczna: witryna + baza danych) — szczegóły i trening na L5, na razie budujemy kontekst.
- Definicje techniczne z kroków **T** sformułowane tak, by dało się z nich budować pytania zamknięte INF.03 — na Z2 kartkówka korzysta z nich wprost.

## Akcent Akademia Tarnowska

Prowadzący w 1. osobie: „to samo, co będziecie robić na zajęciach, nasi studenci robią na projektach i praktykach — na końcu semestru pokażę, jak wygląda to od kuchni". Krótko, konkretnie, bez reklamy.
