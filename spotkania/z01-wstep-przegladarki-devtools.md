# Z1 · Dlaczego web? Wstęp, przeglądarki i DevTools

| | |
|---|---|
| **Semestr** | zimowy — spotkanie 1 z 9 (grupy A/B) |
| **Czas** | 135 min = blok 60 + przerwa 15 + blok 60 (**bez kartkówki** — spotkanie otwierające kurs) |
| **Następne spotkanie** | [Z2 · HTML5 — fundamenty i semantyka](z02-html5-fundamenty.md) (zaczyna się kartkówką z tego spotkania) |

## Overview

### Cel spotkania

- Uczniowie wiedzą, **kto prowadzi zajęcia, jak one wyglądają i co czeka ich w semestrze** (mapa Z2–Z4 i letniego).
- Rozumieją, **dlaczego technologie webowe warto znać** — na konkretnych, zweryfikowanych liczbach, nie na obietnicach.
- Widzą, że **strona może być „natywna”** (PWA) i wiedzą, jak działa internet w pigułce.
- Potrafią otworzyć **Chrome DevTools**, podejrzeć i pozmieniać każdą stronę na żywo.
- Znają **narzędzia warsztatu**: VS Code + Live Server.
- Wiedzą, **jak sami używać AI do nauki** (w tym: dlaczego fundamenty czynią prompty precyzyjniejszymi).
- Piszą i oglądają w przeglądarce **swoją pierwszą stronę HTML**.

### Blok 1 (60 min) — wstęp, liczby, kontekst

| Czas | Temat | Uwagi |
|---|---|---|
| 10' | **Przedstawienie się i zasady** — kim jestem (ścieżka: studia → praca w IT → Akademia Tarnowska), jak wyglądają zajęcia: 135 min, od Z2 kartkówka na start, przerwa w środku, pytania w każdej chwili | budujemy relację, nie wykład |
| 5' | **Mikro-historia WWW** — 1989: Tim Berners-Lee propozycja w CERN; 1991: pierwsza strona; 1995: JavaScript; dziś: ponad 1,2 mld stron | krótko! to ciekawostka, nie program zajęć |
| 10' | **Dlaczego warto: web w liczbach** — tabela statystyk (sekcja poniżej): JS nr 1 po raz 13., 98,9% stron, 1,2 mld stron, 84% programistów używa AI; kariera: frontend/fullstack, popyt na rynku | każdy numer ze źródłem na slajdzie |
| 5' | **PWA — strona „natywna”** — instalacja z przeglądarki, działanie offline, powiadomienia; przykłady (np. Starbucks, Twitter/X Lite); demo: instalacja PWA z paska adresu | „wow”, 3 zdania teorii max |
| 10' | **Jak działa internet w pigułce** — klient–serwer, DNS („książka telefoniczna internetu”), HTTP(S), URL; przeglądarka pobiera HTML/CSS/JS i renderuje | analogie z życia, zero głębi protokołów |
| 10' | **Przeglądarki** — co robi przeglądarka; udziały rynkowe: Chrome ~70–72%, Safari, Edge, Firefox (StatCounter 2025); silniki: Blink, WebKit, Gecko; dlaczego testujemy na kilku | nawiązanie: „dlaczego strona u klienta działa inaczej” |
| 10' | **Mapa semestru + INF.03 + AT** — co dokładnie będzie: **Z2** HTML5 (semantyka, formularze, dostępność), **Z3** CSS3 (stylowanie, flexbox, responsywność), **Z4** CSS w praktyce + publikacja + **pierwszy JavaScript**; semestr letni: JS na poważnie → DOM → dane → **projekt zespołowy** → trening INF.03; egzamin w skrócie (pisemny test + praktyka: strona + baza) | slajd „mapa semestru”; akcent AT: jak te technologie wykorzystujemy ze studentami |

### Przerwa (15 min)

### Blok 2 (60 min) — warsztat: DevTools, narzędzia, AI, pierwsza strona

| Czas | Temat | Uwagi |
|---|---|---|
| 20' | **Chrome DevTools** — otwarcie (F12 / Ctrl+Shift+I / menu → Więcej narzędzi); panel **Elements**: inspekcja i edycja HTML/CSS na żywo (demo: zmieniamy nagłówek i kolor dowolnej strony, np. strony szkoły); **Console**: pierwsze komendy; **device toolbar**: podgląd mobilny; sedno: zmiany są tylko lokalne — odświeżenie przywraca oryginał | każdy uczeń sam modyfikuje wybraną stronę |
| 5' | **Warsztat** — VS Code + rozszerzenie Live Server; struktura projektu: katalog + `index.html` | jeśli sala gotowa, skrócić do 2' |
| 10' | **AI jako Twój tutor** — (a) *dlaczego fundamenty*: porównanie promptów — „utwórz mi stronę internetową wizytówkę i daj linka” **vs** „zaprojektuj stronę-wizytówkę zgodnie ze standardami, z a11y, SEO, systemem kontroli wersji Git, deploymentem na Netlify, w najnowszym Astro.js” — ekspercki prompt = ekspercki wynik, a tak rozmawiać z AI można tylko znając fundamenty; (b) *jak się uczyć z AI*: ELI5, rozwinięcie tematu, pytania kontrolne, „znajdź błąd w moim kodzie”; (c) *zasady*: AI się myli (weryfikuj), na kartkówkach i egzaminie bez AI, używaj do zrozumienia — nie do kopiowania | mini-ściąga z promptami = element zadania domowego |
| 15' | **Live coding: pierwsza strona** — `<!DOCTYPE html>`, `<html lang="pl">`, `<head>` (meta charset, viewport, title), `<body>`: nagłówki, akapity, lista, link, obrazek; zapis i podgląd w Live Server | uczniowie piszą razem z prowadzącym |
| 10' | **Ćwiczenie samodzielne** — mini-strona „Kim jestem” (3 sekcje); zapowiedź Z2 + **zakres kartkówki**: historia WWW, klient–serwer, DevTools, szkielet HTML | obsłuż szybkich wariantem C |

### Ćwiczenia

- **A (podstawowy):** strona „Kim jestem” — nagłówek, 2–3 akapity o sobie, lista zainteresowań, link do ulubionej strony.
- **B (rozszerzający):** dodaj obrazek (optymalizowany!) i drugą podstronę/sekcję „Moje cele na ten rok”.
- **C (gwiazdka):** w DevTools zmień na żywo tytuł i kolorów ulubionej strony; zrób zrzut ekranu przed/po.

### Zadanie domowe (30–40 min)

1. Dokończ stronę „Kim jestem”.
2. Znajdź 2–3 strony, które Ci się podobają — podejrzyj je w DevTools (Elements) i zastanów się, z czego są zbudowane.
3. Wypróbuj 2 prompty z mini-ściągi „AI jako tutor” (np. ELI5 na temat „jak działa DNS”).
4. **Przygotuj się do kartkówki**: historia WWW, klient–serwer, DevTools, szkielet HTML.

### Powiązanie z INF.03

- Zapowiedź struktury egzaminu (test 40 zadań + praca praktyczna: witryna + baza danych) — szczegóły i trening na L5, na razie budujemy kontekst.
- Pierwszy kontakt z formatem zadań: na Z2 kartkówka będzie zawierać pytania zamknięte w stylu INF.03.

### Akcent Akademia Tarnowska

Prowadzący w 1. osobie: „to samo, co będziecie robić na zajęciach, nasi studenci robią na projektach i praktykach — na końcu semestru pokażę, jak wygląda to od kuchni”. Krótko, konkretnie, bez reklamy.

---

## Meta prompt

```text
Jesteś doświadczonym metodykiem nauczania oraz praktykującym programistą webowym (frontend/fullstack). Przygotuj kompletny pakiet materiałów dydaktycznych na pierwsze spotkanie kursu webdevelopmentu.

### Kontekst
- Kurs: „Technologie webowe — HTML5, CSS3, JavaScript” dla uczniów czwartej klasy technikum ZST w Tarnowie (klasa patronacka Akademii Tarnowskiej, wiek 18–19 lat).
- Cel kursu: podstawy HTML5, CSS3 i JavaScript, przygotowanie do egzaminu zawodowego INF.03 oraz zachęcenie uczniów do podjęcia studiów na Akademii Tarnowskiej.
- To spotkanie otwiera kurs — uczniowie nie znają jeszcze żadnego materiału.
- Następne spotkanie (Z2): HTML5 — fundamenty, semantyka, formularze, dostępność (a11y). Zaczyna się kartkówką z zakresu TEGO spotkania.
- Czas: 135 minut = blok 1 (60 min) + przerwa (15 min) + blok 2 (60 min). Bez kartkówki.

### Temat spotkania: „Dlaczego web? Wstęp, przeglądarki i DevTools”
1. Przedstawienie się prowadzącego (mgr inż. Dominik Aksamit, Akademia Tarnowska) i zasady zajęć (135 min, kartkówki od Z2, przerwa).
2. Mikro-historia WWW (5 min maximum!): 1989 Tim Berners-Lee (CERN), 1991 pierwsza strona, 1995 JavaScript, dziś ponad 1,2 mld stron.
3. Dlaczego warto znać technologie webowe — technologie w liczbach (użyj TYLKO poniższych zweryfikowanych danych, podając źródło i rok na slajdzie):
   - JavaScript: najczęściej używany język wśród programistów 13. rok z rzędu, ~66% respondentów (Stack Overflow Developer Survey 2025, 49 000+ odpowiedzi);
   - JavaScript działa po stronie klienta na 98,9% stron internetowych (W3Techs, 2026);
   - ponad 1,2 mld stron internetowych na świecie, w 2000 r. tylko 17 mln (Internet Live Stats);
   - Chrome ~70–72% udziału w rynku przeglądarek (StatCounter, 2025);
   - 84% programistów używa lub planuje używać narzędzi AI (Stack Overflow 2025).
4. PWA — strony mogą być „natywne”: instalacja z przeglądarki, offline, powiadomienia; znane przykłady (np. Starbucks, Twitter/X Lite); krótkie demo instalacji.
5. Jak działa internet w pigułce: klient–serwer, DNS, HTTP(S), URL; renderowanie strony przez przeglądarkę.
6. Przeglądarki i silniki (Blink, WebKit, Gecko); udziały rynkowe; dlaczego testujemy na kilku przeglądarkach.
7. Mapa semestru: co będzie na Z2 (HTML5: semantyka, formularze, a11y), Z3 (CSS3: stylowanie, flexbox, responsywność), Z4 (CSS w praktyce, publikacja na GitHub Pages, dodatek o Tailwind, pierwszy JavaScript) oraz semestr letni (podstawy JS → DOM → dane → projekt zespołowy → trening INF.03); egzamin INF.03 w skrócie (test 40 zadań + praca praktyczna: witryna + baza danych).
8. Chrome DevTools w praktyce: Elements (edycja HTML/CSS na żywo), Console, device toolbar; zmiany lokalne znikają po odświeżeniu.
9. Warsztat: VS Code + Live Server; struktura projektu (katalog, index.html).
10. Blok „AI jako Twój tutor”:
    a) dlaczego warto znać fundamenty — porównanie promptów: „utwórz mi stronę internetową wizytówkę i daj linka” VS „zaprojektuj stronę-wizytówkę zgodnie ze standardami, z a11y, SEO, systemem kontroli wersji Git, deploymentem na Netlify oraz najnowszym Astro.js” — omów różnicę jakości wyniku;
    b) sposoby nauki z AI: ELI5 („wyjaśnij, jakbym miał 12 lat”), rozwinięcie tematu, dopytywanie o niezrozumiałe fragmenty, prośba o pytania kontrolne, „znajdź błąd w moim kodzie”;
    c) zasady uczciwego użycia: AI się myli — weryfikuj; kartkówki i egzamin bez AI; używaj do zrozumienia, nie do kopiowania.
11. Live coding: pierwsza strona HTML (DOCTYPE, html lang="pl", head z meta charset/viewport/title, nagłówki, akapity, lista, link, obrazek) + podgląd w Live Server.

### Zasady metodyczne (niezmiennie)
- Język polski; ton konkretny, energiczny, bez lania wody; odbiorca: technikum.
- Wzorzec „3×P”: krótkie wprowadzenie → PROWADZĄCY pokazuje na żywo → UCZEŃ robi sam. Min. 60% czasu to praktyka (w tym spotkaniu: DevTools, warsztat, pierwsza strona).
- Kod kompletny i działający po wklejeniu; komentarze w kodzie po polsku.
- Historia i teoria mają być marginalne (łącznie ok. 15 min) — ciężar spotkania leży na liczbach, demach i praktyce.
- Subtelna promocja Akademii Tarnowskiej: jeden merytoryczny akcent (np. „te same technologie nasi studenci wykorzystują na projektach”), bez tonu reklamy.

### Do przygotowania (kolejność, format: Markdown, kod w blokach z językiem)
1. Konspekt zajęć z rozpiską czasową (60 + 15 + 60) co najmniej co 5–10 minut, z oznaczeniem momentów live coding i pracy samodzielnej uczniów.
2. Prezentacja (15–20 slajdów), w tym obowiązkowo: slajd „mapa semestru” (Z2, Z3, Z4 + semestr letni), slajd „web w liczbach” (każda liczba ze źródłem i rokiem), slajd o PWA, slajd „AI jako tutor” z porównaniem promptów. Dla każdego slajdu: tytuł + 3–5 punktów + wskazówka [NA ŻYWO], gdzie prowadzący ma pokazać demo.
3. Materiały live coding: kompletny plik index.html budowany krok po kroku (podziel na etapy z komentarzami).
4. Ćwiczenia uczniowskie w 3 wariantach — A: strona „Kim jestem” (nagłówek, akapity, lista, link); B: + obrazek i sekcja „Moje cele”; C: modyfikacja ulubionej strony w DevTools (zrzut przed/po). Do każdego pełne rozwiązanie/instrukcja oczekiwanego efektu.
5. Zadanie domowe (30–40 min) + wskazanie zakresu kartkówki na Z2 (historia WWW, klient–serwer, DevTools, szkielet HTML).
6. Mini-ściąga dla ucznia „AI jako tutor” (1 strona A4): 6 gotowych promptów do skopiowania (ELI5, rozwinięcie tematu, wyjaśnienie fragmentu kodu linia po linii, pytania kontrolne z oceną, szukanie błędu bez podawania rozwiązania, propozycja ćwiczenia utrwalającego) + 3 zasady uczciwego użycia.
7. 5 pytań w stylu INF.03 (zamknięte, jednokrotny wybór A–D) z zakresu tego spotkania — posłużą jako baza kartkówki na Z2; dołącz klucz odpowiedzi i jednozdaniowe uzasadnienia.

### Jakość
- Nie wymyślaj dodatkowych statystyk — używaj wyłącznie podanych wyżej i zawsze ze źródłem.
- Sprawdź poprawność każdego fragmentu kodu (domknięte znaczniki, poprawna struktura dokumentu).
- Materiały mają być gotowe do użycia na zajęciach bez dalszej edycji.
```
