# 0102 · PLAN zajęć - „HTML5: fundamenty i semantyka + dostępność (a11y)"

| | |
|---|---|
| **Semestr** | zimowy 2026 - spotkanie 2 z 9 |
| **Realizacja** | 28 X 2026 (grupa B) · 04 XI 2026 (grupa A) |
| **Czas** | 135 min = kartkówka 10 + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 - tj. **3 bloki** (między nimi 5-minutowe przerwy wg dzwonków) |
| **Prowadzący** | mgr inż. Dominik Aksamit - Akademia Tarnowska |
| **Materiały** | Pakiet prowadzącego (ten katalog): [scenariusz.md](scenariusz.md) · [konspekt.md](konspekt.md) (rozpiska co 2–10 min) · [prezentacja.md](prezentacja.md) (18 slajdów) · [kartkowka.md](kartkowka.md) · [rozwiazania/](rozwiazania/README.md) (**tylko prowadzący**) · **pakiet ucznia**: [../0102/](../0102/README.md) - instrukcja ćwiczeń z planem spotkania + start do live codingu (`index.html`) |

## Nazwy bloków (wpisy do dziennika)

| Blok | Czas | Nazwa |
|---|---|---|
| 1 | 0:00–0:45 | „HTML5: semantyczny szkielet strony, tekst i linki" |
| 2 | 0:45–1:30 | „Obrazy, tabele i multimedia - z dostępnością (a11y)" |
| 3 | 1:30–2:15 | „Formularze z walidacją HTML5 - ćwiczenie: fanpage" |

Wpis dla bloku 1 może zaczynać się od „Kartkówka z zakresu 0101." - kartkówka to forma sprawdzania, nie temat.

Granica bloków 1/2 (0:45) przecina blok obrazów (0:40–0:50). Naturalny punkt cięcia: **część 1 (img, src, alt) domyka blok 1, część 2 (formaty, figure) otwiera blok 2** i prowadzi prosto do a11y. Jeśli dzwonek pozwoli przesunąć, można cały blok przenieść do bloku 2 - kosztem 5 minut ćwiczenia fanpage w bloku 3.

## Cel spotkania - po zajęciach uczeń:

- buduje **semantyczny szkielet** strony (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`) i uzasadnia, dlaczego nie „ściana divów",
- strukturuje tekst: nagłówki `h1`–`h6` po kolei, akapity, wyróżnienia, listy `ul`/`ol`/`dl`,
- robi linki (ścieżki względne/bezwzględne, `target` + `rel="noopener"`, zakotwiczenia `#id`) i wstawia obrazy z sensownym `alt`,
- tworzy **tabelę danych** (`caption`, `thead`/`th`, `tbody`/`td`) i wstawia multimedia (`audio`/`video`/`iframe`),
- buduje **formularz z walidacją HTML5** (`label`, typy `input`, `required`, `pattern`, `min`/`max`) - bez JavaScriptu,
- rozumie **dostępność (a11y)**: po co, co robić w HTML i jakie są 4 zasady WCAG,
- zaczął **własny fanpage** - szkielet pod ostylowanie na 0103.

## Agenda

### Blok 1 · 0:00–0:45 - „HTML5: semantyczny szkielet strony, tekst i linki"

| Czas | Blok | Forma |
|---|---|---|
| 0:00–0:10 | **Kartkówka nr 1** - zakres 0101; 3 pytania zamknięte (A–D) + 2 otwarte, max 5 pkt, ocena cząstkowa | PRACA SAMODZIELNA |
| 0:10–0:12 | Omówienie kartkówki na skróty - pułapki: `h1` vs `title`; dlaczego F5 kasuje zmiany z DevTools | - |
| 0:12–0:22 | **Ściana divów → szkielet semantyczny**: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`; po co semantyka (czytniki ekranu, SEO, INF.03) | LIVE CODING · etap 1 |
| 0:22–0:31 | **Tekst i listy**: `h1`–`h6` bez przeskoków, dokładnie jeden `h1`; `strong`/`em`, `br`/`hr`, `blockquote`; `ul`/`ol`/`dl` | LIVE CODING · etap 2 |
| 0:31–0:40 | **Linki i ścieżki**: względne vs bezwzględne, `target="_blank"` + `rel="noopener"`, zakotwiczenia `#id`, `mailto:` | LIVE CODING · etap 3 |
| 0:40–0:45 | **Obrazy cz. 1**: `img`, `src`, `alt` opisuje treść (nie „obrazek"!), `width`/`height` | LIVE CODING · etap 4 (start) |

**Kluczowe punkty i pułapki INF.03:** semantyka = znaczniki mówią, *czym* jest treść · `article` vs `div` · `ol` gdy kolejność ma znaczenie · rozpoznać ścieżkę względną i bezwzględną w kodzie · jeden `h1` na stronę.

### Blok 2 · 0:45–1:30 - „Obrazy, tabele i multimedia - z dostępnością (a11y)"

| Czas | Blok | Forma |
|---|---|---|
| 0:45–0:50 | **Obrazy cz. 2**: formaty JPG/PNG/WebP/SVG - kiedy który; `figure` + `figcaption` | LIVE CODING · etap 4 (cd.) |
| 0:50–1:00 | **Dostępność (a11y)**: liczby (WHO 2023: 1 na 6 ludzi; EAA od 28 VI 2025; WebAIM Million 2026: 95,9% stron z błędami) · praktyka: `alt`, `lang`, nagłówki po kolei, `label`, nawigacja Tabem · WCAG: 4 zasady · ARIA tylko, gdy HTML nie wystarcza | DEMO + AUDYT · etap 5 |
| 1:00–1:15 | **Przerwa** - na tablicy zostają: wzór zakotwiczenia (`href="#id"` + `id`) i 4 zasady WCAG | - |
| 1:15–1:25 | **Tabele danych**: `table`, `caption`, `thead` z `th` (`scope`), `tbody` z `td`; tabela to nie layout | LIVE CODING · etap 6 |
| 1:25–1:30 | **Multimedia**: `video`/`audio` z `controls`, `iframe` **zawsze z `title`** (YouTube przez `iframe`, nie `video`) | LIVE CODING · etap 7 |

**Kluczowe punkty i pułapki INF.03:** SVG na logo/ikony, JPG na zdjęcia · tabela danych ≠ układ strony · `th`/`td` + `caption` w zestawieniach danych · `iframe` bez `title` = błąd dostępności.

### Blok 3 · 1:30–2:15 - „Formularze z walidacją HTML5 - ćwiczenie: fanpage"

| Czas | Blok | Forma |
|---|---|---|
| 1:30–1:45 | **Formularze + walidacja HTML5**: `form`, `label` powiązany `for`/`id`, dobór typu `input` do danych (text, email, date, number…), `select`, `textarea`, `checkbox`; walidacja za darmo: `required`, `pattern`, `min`/`max`; finał: „Wyślij" przy pustym formularzu · **akcent Akademii Tarnowskiej** (jedno zdanie) | LIVE CODING · etapy 8–14 |
| 1:45–1:50 | **Start ćwiczenia głównego: fanpage** - katalog `fanpage/`, wybór tematu (zespół/gracz/gra), szkielet semantyczny | PRACA SAMODZIELNA |
| 1:50–2:10 | **Fanpage (cd.)** - warianty A/B/C; checklista a11y (8 punktów); 2 min przed końcem bloku: „odłóżcie myszy, przejdźcie swoje strony Tabem" | PRACA SAMODZIELNA |
| 2:10–2:15 | **Domknięcie**: mini-quiz ustny · podsumowanie rundą · zadanie domowe · zapowiedź 0103 (CSS3 - stylowanie fanpage'a) + zakres kartkówki | - |

**Kluczowe punkty i pułapki INF.03:** formularz i tabela to stałe elementy pracy praktycznej · dobór typu pola do danych (e-mail → `type="email"`) · `label`/`for`/`id` = a11y i punkty · walidacja bez JavaScriptu (`required`, `pattern`, `min`/`max`).

## Logistyka - przed zajęciami

- [ ] Chrome + VS Code z rozszerzeniem **Live Server** na komputerach uczniowskich i prowadzącego (stan jak po 0101).
- [ ] **Rozdrukki kartkówki** - po 1 egzemplarzu na ucznia ([kartkowka.md](kartkowka.md), drukuj bez klucza).
- [ ] **Pakiet ucznia** ([../0102/](../0102/README.md)) - do pobrania z [daksamit.pl/zp/0102](https://daksamit.pl/zp/0102): opublikuj zip katalogu i **przetestuj link przed zajęciami**. Zawiera instrukcję z planem spotkania i start do live codingu (`index.html`). Plan B: pendrive / dysk klasowy.
- [ ] Projektor czytelny z ostatniej ławki (powiększ czcionkę w VS Code i Chrome).
- [ ] Przetestuj linki: `unsplash.com` (uczniowie będą stamtąd pobierać zdjęcia - sprawdź, czy działa w sieci szkolnej), `placehold.co`, `picsum.photos`, mp3 SoundHelix, film Big Buck Bunny, embed YouTube.
- [ ] Otwarte karty na start: prezentacja + [MDN Web Docs](https://developer.mozilla.org/pl/docs/Web/HTML).
- [ ] **Plan B offline:** lokalny katalog `obrazy/` na maszynach uczniowskich; `iframe` → zrzut ekranu; formularz i walidacja działają w całości offline.

## Linki - źródła i narzędzia

**Statystyki a11y (odśwież u źródła przed każdym terminem):**

- WHO, Disability - fact sheet (1,3 mld / 16% / „1 na 6", wydanie 2023): https://www.who.int/news-room/fact-sheets/detail/disability-and-health
- WebAIM Million 2026 (95,9% stron głównych z błędami WCAG 2): https://webaim.org/projects/million/
- European Accessibility Act - dyrektywa (UE) 2019/882, obowiązuje od 28 VI 2025: https://eur-lex.europa.eu/eli/dir/2019/882/oj

**Narzędzia (opcjonalnie na zajęciach):**

- [Walidator W3C](https://validator.w3.org/) - demo na żywo: wklej adres dowolnej strony i pokaż listę błędów (dobre w bloku a11y albo przy omówieniu kartkówki).
- [Rozszerzenie WAVE do Chrome](https://wave.webaim.org/extension/) - automatyczny audyt dostępności; działa też na localhost (strona z Live Servera), więc można go pokazać na projekcie live codingu jako rozszerzenie audytu Tabem z etapu 5.
- [WCAG 2 Quick Reference (W3C WAI)](https://www.w3.org/WAI/WCAG22/quickref/) - wszystkie kryteria z filtrami, gdy ktoś zapyta: „a co dokładnie mówi WCAG?".

## Domknięcie dnia - obowiązki wynikające ze spotkania

- **Zadanie domowe (30–45 min):** dokończ fanpage z checklistą a11y · „detektyw dostępności" - znajdź stronę z oczywistym błędem (brak `alt`, ściana divów), zapisz adres i co jest nie tak (omówimy na 0103) · powtórka do kartkówki.
- **Zakres kartkówki na 0103:** semantyczne znaczniki (`article` vs `div`, `nav`/`header`/`footer`) · typy `input` i dobór do danych · `label` + a11y · tabele (`th`/`td`, `caption`) · walidacja HTML5 (`required`, `pattern`, `min`/`max`).
- **Kontynuacja:** fanpage wraca na 0103 (stylowanie CSS) i 0104 (publikacja + pierwszy JS) - przypomnij uczniom o zabezpieczeniu katalogu `fanpage/` z podkatalogiem `obrazy/`.
- **Akcent Akademii Tarnowskiej** (jedno zdanie, w bloku formularzy): „Dokładnie takie formularze studenci Akademii Tarnowskiej robią na zaliczeniowe projekty aplikacji - niedługo będziecie mieli przewagę na starcie."

## Alternatywne nazwy bloków (do wyboru przy wpisie)

| Blok | Wariant krótki | Wariant chwytliwy |
|---|---|---|
| 1 | „HTML5 - szkielet semantyczny i treść" | „Ściana divów musi upaść - HTML, który coś znaczy" |
| 2 | „Obrazy, tabele, multimedia i dostępność" | „Strona dla wszystkich - od `alt` do WCAG" |
| 3 | „Formularze HTML5 i fanpage" | „Zapisz się! - formularz, który sam pilnuje danych" |
