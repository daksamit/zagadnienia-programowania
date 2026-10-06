# Technologie webowe — zajęcia klas patronackich ZST × Akademia Tarnowska

Materiały dydaktyczne do zajęć z podstaw webdevelopmentu (**HTML5, CSS3, JavaScript**) prowadzonych dla uczniów **Zespołu Szkół Technicznych w Tarnowie** w ramach **klas patronackich Akademii Tarnowskiej**.

| | |
|---|---|
| **Prowadzący** | mgr inż. Dominik Aksamit — Akademia Tarnowska |
| **Odbiorcy** | uczniowie czwartej klasy technikum ZST w Tarnowie |
| **Cykl** | semestr zimowy: 9 spotkań · semestr letni: 11 spotkań · grupy **A** i **B** na przemian |
| **Jednostka zajęć** | **135 minut** (z 15-minutową przerwą) |

---

## Cel zajęć

1. **Praktyczne opanowanie podstaw HTML5, CSS3 i JavaScript** — od pierwszej strony po działającą interaktywną aplikację webową.
2. **Przygotowanie do egzaminu zawodowego INF.03** — kartkówki, zadania i ćwiczenia w formacie zbliżonym do egzaminu, na finał trening na arkuszu próbnym.
3. **Zachęcenie uczniów do podjęcia studiów na Akademii Tarnowskiej** — merytorycznie: ścieżka „technikum → studia → praca w IT”, praktyki, projekty i życie uczelniane.

## Format zajęć

Spotkanie trwa **135 minut** wg stałego schematu:

| Element | Czas | Uwagi |
|---|---|---|
| Kartkówka | 10 min | **od drugiego spotkania (Z2)**; zakres: poprzednie spotkanie; min. 2 pytania zamknięte w formacie INF.03 |
| Blok 1 | 50 min | teoria + live coding + ćwiczenia |
| Przerwa | 15 min | |
| Blok 2 | 60 min | praktyka, ćwiczenia, projekt |
| **Razem** | **135 min** | |

*Spotkanie Z1 rozpoczyna kurs, więc nie zaczyna się kartkówką — ma wtedy 60 + 15 + 60 minut.*

Zasady metodyczne:

- **min. 60% czasu to praktyka uczniowska** i live coding prowadzącego,
- wzorzec każdego zagadnienia: *krótkie wprowadzenie → demo na żywo → uczeń robi sam*,
- ćwiczenia w trzech wariantach: **A** (podstawowy), **B** (rozszerzający), **C** (gwiazdka dla szybkich),
- każde spotkanie kończy się zadaniem domowym i podaniem zakresu najbliższej kartkówki.

## Organizacja roku — grupy A i B

Zajęcia odbywają się na przemian dla dwóch grup, dlatego liczba spotkań wypada nieparzyście:

| Semestr | Spotkań łącznie | Grupa A | Grupa B |
|---|---|---|---|
| zimowy | 9 | 5 | 4 |
| letni | 11 | 6 | 5 |

Repozytorium zawiera **9 bazowych scenariuszy** (4 zimowy + 5 letnich) wspólnych dla obu grup. **Nadwyżkowe spotkania grupy A** (piąte zimą i szóste latem) pełnią rolę **warsztatów utrwalających**: powtórka materiału, ćwiczenia dodatkowe, dokańczanie projektów i indywidualna praca z uczniami — bez osobnych scenariuszy.

## Ramowy program

### Semestr zimowy

| # | Spotkanie | Główne tematy | Kartkówka z |
|---|---|---|---|
| Z1 | [Dlaczego web? Wstęp, przeglądarki i DevTools](spotkania/z01-wstep-przegladarki-devtools.md) | przedstawienie się i mapa semestru; technologie webowe w liczbach; PWA — strona może być „natywna”; jak działa internet; przeglądarki i silniki; **Chrome DevTools**; VS Code + Live Server; **AI jako tutor** (po co znać fundamenty, gotowe prompty); pierwsza strona HTML na żywo | — |
| Z2 | [HTML5 — fundamenty i semantyka](spotkania/z02-html5-fundamenty.md) | semantyczny szkielet strony; tekst, listy, linki, obrazy; tabele; multimedia; formularze i walidacja HTML5; **dostępność (a11y)**: alt, nagłówki, `label`, klawiatura, ARIA/WCAG w pigułce; ćwiczenie: fanpage z checklistą dostępności | Z1 |
| Z3 | [CSS3 — stylowanie i responsywność](spotkania/z03-css3-stylowanie.md) | selektory i kaskada; box model; kolory i jednostki; typografia; flexbox; media queries i responsywność; a11y cd.: kontrast i czytelność; stylowanie fanpage'a z Z2 | Z2 |
| Z4 | [CSS w praktyce + pierwsze kroki w JavaScript](spotkania/z04-js-pierwsze-kroki.md) | mini-powtórka CSS z Z3; grid, animacje, pozycjonowanie sticky; publikacja strony (GitHub Pages); dodatek „Jak w branży”: **Tailwind CSS i atomic CSS**; **wprowadzenie do JS**: „moment wow”, konsola, zmienne, pierwszy skrypt, reakcja na kliknięcie | Z3 |

### Semestr letni

| # | Spotkanie | Główne tematy | Kartkówka z |
|---|---|---|---|
| L1 | [JavaScript — solidne podstawy języka](spotkania/l01-js-podstawy.md) | operatory; warunki; pętle; funkcje (także arrow); `alert`/`prompt`/`confirm`; debugowanie w DevTools (breakpointy) | Z4 |
| L2 | [DOM i zdarzenia — strona żyje](spotkania/l02-js-dom-zdarzenia.md) | drzewo DOM; wybieranie i zmiana elementów; zdarzenia; formularz z walidacją JS; projekty: licznik, galeria, quiz | L1 |
| L3 | [Tablice, obiekty i dane](spotkania/l03-js-dane.md) | tablice i metody; obiekty; JSON; localStorage (lista zadań); `setTimeout`/`setInterval`; wprowadzenie do `fetch` i API; wzmianka o PWA: service worker i manifest w pigułce | L2 |
| L4 | [Projekt zintegrowany HTML + CSS + JS](spotkania/l04-projekt-calkowity.md) | warsztaty projektowe w zespołach; podstawy Git/GitHub; publikacja; prezentacje projektów; projekt w portfolio i CV | L3 |
| L5 | [INF.03 — trening egzaminacyjny i co dalej](spotkania/l05-inf03-trening.md) | strategia części pisemnej i praktycznej; test próbny; mini-arkusz praktyczny wg schematu CKE z kryteriami punktowania; ścieżki rozwoju i rekrutacja na Akademię Tarnowską; ankieta podsumowująca | L4 |

## Efekty kształcenia — po kursie uczeń potrafi:

- zbudować semantyczną, dostępną i responsywną stronę internetową w HTML5 i CSS3 (flexbox, grid, media queries),
- dodać interaktywność w czystym JavaScriptcie: obsługa zdarzeń, manipulacja DOM, formularze z walidacją, localStorage,
- opublikować stronę w internecie (GitHub Pages) i pracować z podstawami Gita,
- korzystać z Chrome DevTools do analizy, stylowania i debugowania stron,
- świadomie korzystać z AI jako tutora: rozwijać tematy, dopytywać o niezrozumiałe rzeczy (ELI5), precyzyjnie zamawiać rozwiązania i krytycznie oceniać wynik,
- rozwiązywać zadania w formacie egzaminu INF.03 i znać strategię rozkładu czasu na egzaminie.

## Egzamin INF.03 w pigułce

Kwalifikacja **INF.03 — „Tworzenie i administrowanie stronami i aplikacjami internetowymi oraz bazami danych”** (m.in. technik programista, technik informatyk).

| Część | Forma | Czas | Punkty | Próg zdawalności |
|---|---|---|---|---|
| pisemna | test — 40 zadań zamkniętych | 60 min | 40 | 20 pkt (50%) |
| praktyczna | praca egzaminacyjna — wykonanie witryny internetowej (HTML/CSS/JS, bywa PHP) oraz bazy danych (SQL) | 240 min | 100 | 50 pkt (50%) |

Źródło: informator o egzaminie zawodowym CKE (cke.gov.pl → Egzaminy zawodowe → Informatory). Przed sesją warto zweryfikować aktualną wersję informatora.

## Struktura repozytorium

```text
.
├── README.md          # ten plik — przegląd kursu
├── AGENTS.md          # instrukcje dla asystentów AI pracujących w repo
└── spotkania/         # 9 scenariuszy: overview + meta prompt
    ├── z01-wstep-przegladarki-devtools.md
    ├── z02-html5-fundamenty.md
    ├── z03-css3-stylowanie.md
    ├── z04-js-pierwsze-kroki.md
    ├── l01-js-podstawy.md
    ├── l02-js-dom-zdarzenia.md
    ├── l03-js-dane.md
    ├── l04-projekt-calkowity.md
    └── l05-inf03-trening.md
```

Planowane katalogi na wygenerowane materiały: `prezentacje/` (outline'y slajdów), `cwiczenia/` (materiały dla uczniów), `rozwiazania/` (klucze odpowiedzi i rozwiązania) — konwencje opisane w [AGENTS.md](AGENTS.md).

## Jak korzystać z meta promptów

Każdy scenariusz w `spotkania/` zawiera sekcję **Meta prompt** — gotowe do skopiowania polecenie dla asystenta AI (ZCode, Claude, ChatGPT…), które generuje **pełny pakiet materiałów** na dane spotkanie: kartkówkę z kluczem, konspekt z rozpiską czasową, outline prezentacji, kod do live codingu, ćwiczenia w 3 wariantach z rozwiązaniami, zadanie domowe i pytania w stylu INF.03.

1. Otwórz plik spotkania, np. [spotkania/z02-html5-fundamenty.md](spotkania/z02-html5-fundamenty.md).
2. Skopiuj całą zawartość bloku **Meta prompt**.
3. Wklej do nowej rozmowy z asystentem AI i wyślij.
4. Wynik zapisz w repozytorium zgodnie z konwencjami z [AGENTS.md](AGENTS.md).

## Technologie webowe w liczbach (dane na Z1)

Zweryfikowane statystyki używane na pierwszym spotkaniu — z podaniem źródeł (stan: październik 2026):

| Liczba | Źródło |
|---|---|
| JavaScript — najczęściej używany język wśród programistów **13. rok z rzędu** (~66% respondentów; kolejne miejsca: HTML/CSS, SQL, Python); 49 000+ odpowiedzi ze 177 krajów | [Stack Overflow Developer Survey 2025](https://survey.stackoverflow.co/2025/technology) |
| JavaScript działa po stronie klienta na **98,9% wszystkich stron internetowych** | [W3Techs — Usage Statistics of JavaScript](https://w3techs.com/technologies/details/cp-javascript) |
| Ponad **1,2 mld stron internetowych** na świecie (w 2000 r. tylko 17 mln; aktywnych ok. 15%) | [Internet Live Stats](https://www.internetlivestats.com/total-number-of-websites/) |
| **Chrome ~70–72%** globalnego udziału w rynku przeglądarek (rekord w historii pomiarów; Safari, Edge i Firefox daleko w tyle) | [StatCounter Global Stats](https://gs.statcounter.com/browser-market-share/all/worldwide/2025) |
| **84% programistów** używa lub planuje używać narzędzi AI do kodowania | [Stack Overflow Developer Survey 2025](https://survey.stackoverflow.co/2025) |

> Przed każdym użyciem na zajęciach odśwież dane u źródła — statystyki przedawniają się szybko.

---

**Kontakt:** mgr inż. Dominik Aksamit · Akademia Tarnowska · [zst.tarnow.pl](https://www.zst.tarnow.pl/) · [akademia.tarnowska.pl](https://akademia.tarnowska.pl/)
