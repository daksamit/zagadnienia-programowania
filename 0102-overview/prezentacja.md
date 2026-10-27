# 0102 · Prezentacja — „HTML5: fundamenty i semantyka + dostępność (a11y)"

| | |
|---|---|
| **Spotkanie** | 0102 · semestr zimowy 2026 (realizacja: 28 X — grupa B, 04 XI — grupa A) |
| **Slajdów** | 18 |
| **Czas prezentacji** | ok. 40 min łącznie z demo i live codingiem (slajdy 1–2 kartkówka; 3–12 Sekcja 1; 13–16 Sekcja 2; 17–18 Sekcja 3 — towarzyszą pracy uczniów) |

Konwencja: przy slajdzie znacznik **[NA ŻYWO]** = przełącz się na przeglądarkę/VS Code i pokaż demo. Wszystkie statystyki występują wyłącznie ze źródłem i rokiem — nie doklejaj do nich żadnych innych liczb.

---

## Slajd 1 · Tytułowy

- **Technologie webowe — HTML5 · CSS3 · JavaScript**
- 0102: HTML5 — fundamenty i semantyka + dostępność (a11y)
- mgr inż. Dominik Aksamit · Akademia Tarnowska × ZST w Tarnowie
- efekt dnia: **własny fanpage** — gotowy szkielet pod stylowanie na 0103

## Slajd 2 · Kartkówka na start

- **10 minut · 5 pytań · max 5 pkt** — ocena cząstkowa do dziennika
- pytania 1–3 zamknięte (A–D) — dokładnie jedna odpowiedź
- pytania 4–5 otwarte: szkielet HTML + DevTools
- pisz czytelnie; skończysz — odłóż długopis i poczekaj spokojnie
- zakres: całe 0101 (historia WWW, klient–serwer/DNS, DevTools, szkielet HTML)

## Slajd 3 · Plan na dziś

- **Sekcja 1:** semantyczny szkielet → tekst i listy → linki → obrazy → dostępność (a11y)
- **przerwa 15 minut**
- **Sekcja 2:** tabele → multimedia → formularze z walidacją HTML5 (live coding krok po kroku)
- **Sekcja 3:** budujesz własny fanpage (warianty A/B/C) + checklista a11y
- wzorzec dnia jak zawsze: krótko mówię → pokazuję → **Ty piszesz**

## Slajd 4 · „Ściana divów" — strona, która nic nie znaczy

- wszystko w `div`-ach: działa, wygląda… i tyle
- czytnik ekranu nie ma pojęcia, co jest menu, a co treścią
- wyszukiwarka nie rozpoznaje nawigacji ani nagłówków (SEO)
- po pół roku sam nie pamiętasz, który div jest który
- na INF.03: praca praktyczna **z semantyką jest wyżej punktowana** niż ta sama strona w samych divach

## Slajd 5 · Semantyczny szkielet — mapa znaczników

- `header` — nagłówek strony: logo, nazwa, hasło
- `nav` — blok nawigacji (menu) · `main` — główna treść (**dokładnie jeden**)
- `section` — wydzielona część tematyczna (z własnym nagłówkiem)
- `article` — samodzielna, powtarzalna całość: news, post, wpis
- `aside` — treść poboczna · `footer` — stopka

**[NA ŻYWO — LIVE CODING]** Otwórzcie `live-coding-start.html` — zamieniamy ścianę divów w szkielet semantyczny (etap 1).

## Slajd 6 · Tekst: nagłówki i akapity

- `h1`–`h6`: **dokładnie jeden `h1`** na stronę, dalej **po kolei** (h1 → h2 → h3, bez przeskoku h2 → h5)
- `p` akapit · `strong` = ważność · `em` = nacisk (czytnik ekranu zmienia intonację)
- `br` nowa linia (np. adres) — **nie** do robienia odstępów · `hr` przerwa tematyczna
- `blockquote` = dłuższy cytat (+ podanie autora)
- kolejność nagłówków = spis treści czytany przez czytniki ekranu i roboty

**[NA ŻYWO]** Dopisujemy skład, historię i słowniczek (etap 2).

## Slajd 7 · Listy: ul / ol / dl — kiedy które

- `ul` — kolejność **nie** ma znaczenia: skład zespołu, cechy, tagi
- `ol` — numeracja ma znaczenie: kroki, ranking, historia (2022 → 2024 → 2026)
- `dl` — lista definicyjna: **termin** (`dt`) + **opis** (`dd`) — słowniczki, parametry
- każda pozycja `ul`/`ol` to `li`
- pytanie kontrolne: „instrukcja montażu — `ul` czy `ol`?"

## Slajd 8 · Linki i ścieżki

- `a href="…"` — ścieżka **względna**: plik w naszym projekcie (`obrazy/koncert.jpg`)
- ścieżka **bezwzględna**: pełny adres (`https://developer.mozilla.org`)
- `target="_blank"` (nowa karta) **zawsze z `rel="noopener"`**
- zakotwiczenie: `href="#id"` skacze do elementu o tym `id` — tak działa menu
- `mailto:adres` otwiera program pocztowy · pułapka INF.03: rozpoznaj ścieżkę względną vs bezwzględną

**[NA ŻYWO]** Menu staje się klikalne (etap 3).

## Slajd 9 · Obrazy: img, alt, width/height

- `img` + `src` + **`alt` opisujący treść obrazu** — nie „obrazek", nie „foto"!
- `alt` czyta czytnik ekranu; pokazuje się też, gdy plik się nie wczyta
- `width` i `height` rezerwują miejsce — strona nie „skacze" przy ładowaniu
- `figure` + `figcaption` = obraz z widocznym podpisem
- INF.03: podpisywanie obrazów w galerii to standardowe kryterium punktowania

**[NA ŻYWO]** Budujemy galerię (etap 4).

## Slajd 10 · Formaty obrazów — kiedy który

- **JPG** — zdjęcia (miliony kolorów, brak przezroczystości)
- **PNG** — zrzuty ekranu, grafiki z ostrymi krawędziami, **przezroczystość**
- **WebP** — jak JPG/PNG, ale ~25–35% lżejszy (dokumentacja Google WebP) — coraz częstszy standard
- **SVG** — ikony i logotypy: skaluje się bez utraty jakości, waży kilobajty
- zasada: zdjęcie → JPG/WebP · ikony/wykreślna grafika → SVG · potrzebna przezroczystość → PNG/WebP

## Slajd 11 · Dostępność (a11y) — po co, w liczbach

- **1 na 6 osób na świecie** żyje z istotną niepełnosprawnością — ok. 1,3 mld, 16% populacji (WHO, 2023)
- **European Accessibility Act** (dyrektywa UE 2019/882) **obowiązuje od 28 czerwca 2025** — e-commerce i usługi konsumenckie w UE muszą być dostępne
- **95,9% z miliona badanych stron głównych** ma wykrywalne błędy dostępności (WebAIM Million, 2026) — typowa strona jest **niedostępna**
- a11y to też **kryteria punktowania** w pracach praktycznych INF.03
- po polsku „dostępność", skrót **a11y** = „a" + 11 liter + „y"

## Slajd 12 · a11y w praktyce — i WCAG w pigułce

- `alt` na obrazach · `html lang="pl"` · nagłówki **po kolei**
- każde pole formularza z `label` (`for` ↔ `id`) · `iframe` z `title`
- strona obsługiwana **samym Tabem** — mysz pod biurko!
- **ARIA tylko tam, gdzie HTML nie wystarcza** (najpierw dobry HTML!)
- WCAG, 4 zasady: **spostrzegalna · funkcjonalna · zrozumiała · solidna**

**[NA ŻYWO]** Odłóż mysz — przechodzę stronę samym Tabem; potem audyt Waszych stron (etap 5).

## Slajd 13 · Tabele — do danych, nie do układu

- `table` + `caption` (tytuł tabeli) + `thead` z `th` + `tbody` z `td`
- `th` = komórka **nagłówkowa**; `scope="col"`/`"row"` — wskazówka dla czytników ekranu
- tabela do **danych** (zestawienia, cenniki, wyniki) — układ strony tabelą to antyk z lat 90.
- INF.03 uwielbia zestawienia danych — tabela wraca w każdej pracy praktycznej

**[NA ŻYWO]** Sekcja „Koncerty" z tabelą trasy (etap 6).

## Slajd 14 · Multimedia: audio · video · iframe

- `audio controls` — odtwarzacz dźwięku bez żadnego JS
- `video controls width` — odtwarzacz wideo; `source` = plik, tekst w środku = fallback
- `iframe` — wstawka **innej strony** w naszą (YouTube, mapa)
- **`title` na iframe** obowiązkowo — czytnik ekranu musi wiedzieć, co jest w ramce
- uwaga: film z YouTube wstawiamy przez `iframe` (kod „Udostępnij → Umieść")

**[NA ŻYWO]** Wstawiamy wszystkie trzy (etap 7).

## Slajd 15 · Formularz — budowa

- `form` z `action` (dokąd idą dane) i `method` (np. `post`)
- **każde pole z `label`**: `for` etykiety = `id` pola (klik w etykietę uaktywnia pole — a11y!)
- `input` ma typy pod dane: `text` `email` `number` `date` `password` `radio` `checkbox` `file` `color` `range`
- dłuższy tekst: `textarea` · wybór z listy: `select` + `option` · `fieldset` + `legend` grupują radio
- prawie każda praca praktyczna INF.03 zawiera formularz — budujemy go w stylu egzaminacyjnym

**[NA ŻYWO — LIVE CODING]** Formularz „Klub Fana" krok po kroku (etapy 8–13).

## Slajd 16 · Walidacja HTML5 — przeglądarka pilnuje za darmo

- `required` — nie wyślesz pustego formularza · `minlength` — minimalna długość
- `pattern` — wzorzec (wyrażenie regularne), np. kod `BP-2026` = `[A-Z]{2}-[0-9]{4}`; `title` = podpowiedź
- `min`/`max` — zakresy liczb i dat
- wszystko **bez linijki JavaScriptu** — komunikaty po polsku rysuje przeglądarka

**[NA ŻYWO]** Klikamy „Wyślij" przy pustym formularzu — przeglądarka krzyczy; potem zły kod promocyjny (etap 14).

## Slajd 17 · Ćwiczenie główne: Twój fanpage

- temat: **ulubiony zespół · gracz · gra** — wybierz to, o czym umiesz pisać
- **A:** szkielet semantyczny + 2 sekcje + galeria 3 obrazów z `alt` + formularz (imię, e-mail, zgoda)
- **B:** + tabela danych + `select` i `radio` w `fieldset` + multimedia
- **C ⭐:** menu wewnętrzne + audyt Tabem (mysz pod biurko) + poprawki
- koniec = przejście **checklisty a11y** z instrukcji (8 punktów)
- 25 minut teraz, dokończenie w domu — **projekt zostaje na 0103!**

## Slajd 18 · Podsumowanie i zapowiedź

- dziś masz: semantyczny szkielet, tekst i listy, linki, obrazy, tabele, multimedia, formularz z walidacją — i checklistę a11y
- **zadanie domowe (30–45 min):** dokończ fanpage z checklistą a11y · **detektyw dostępności** — znajdź stronę z błędem (brak `alt`, ściana divów), zapisz link — omawiamy na 0103
- **0103 — CSS3:** Twoj fanpage dostanie wygląd: kolory, fonty, flexbox i wersja mobilna
- **kartkówka na 0103:** semantyka · typy `input` i formularze · `label` + a11y · tabele · walidacja HTML5
- po drodze: 0104 — publikacja strony w internecie i **pierwszy JavaScript** (strona zacznie reagować na kliknięcia)
