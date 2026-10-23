# AGENTS-adept.md — alternatywna wersja instrukcji z metodą ADEPT

> To alternatywa dla [AGENTS.md](AGENTS.md). Obowiązuje tylko wtedy, gdy prowadzący wprost poprosi o pracę „wg ADEPT" / „wg AGENTS-adept.md". W przeciwnym razie stosuj AGENTS.md.

## O repozytorium

Materiały dydaktyczne na zajęcia z podstaw webdevelopmentu (HTML5, CSS3, JavaScript) dla uczniów **czwartej klasy technikum ZST w Tarnowie** — klasy patronackie **Akademii Tarnowskiej**. Prowadzący: mgr inż. Dominik Aksamit. Pełny kontekst kursu: [README.md](README.md).

Kontekst organizacyjny:

- Przedmiot szkolny: **„Zagadnienia programowania”**, współprowadzony z mgr. inż. Tomaszem Gądkiem — jego blok backendowy ma osobne materiały **poza tym repozytorium** (nie generuj ich tutaj).
- Zajęcia: **środy 7:30–9:45** (135 min); klasa podzielona na **grupy A i B pracujące równolegle** — w każdym terminie każda grupa z innym prowadzącym, prowadzący zamieniają się grupami co spotkanie.
- Semestr zimowy 2026: **9 terminów** (07 X – 16 XII); semestr letni 2027: **11 terminów** (03 III – 02 VI) + rezerwowe 09 VI i 16 VI.
- Każdy scenariusz Aksamita realizowany jest **dwukrotnie** — najpierw z jedną grupą, na następnym spotkaniu powtórzony z drugą; dziesiąte spotkanie każdej grupy to warsztaty utrwalające bez osobnego scenariusza (16 XII — grupa B, 02 VI — grupa A).
- Konkretne daty i przydział grup zawsze bierz z sekcji **„Harmonogram zajęć”** w [README.md](README.md).

**Twoja rola:** pomagasz prowadzącemu tworzyć i aktualizować materiały: konspekty, prezentacje, kod do live codingu, kartkówki, ćwiczenia, zadania domowe, arkusze treningowe INF.03 — zawsze na bazie scenariuszy w katalogach spotkań `{id}/`.

## Twarde zasady

1. **Język polski** we wszystkich materiałach. Materiały dla uczniów pisz bezpośrednio, per „ty" („spróbuj", „zauważ"); konspekty dla prowadzącego — forma opisowa.
2. **Odbiorca:** uczeń 4. klasy technikum (18–19 lat). Konkret, praktyka, zero tonu akademickiego i lania wody.
3. **Struktura czasu 135 min — trzy sekcje:**
   - 0101: sekcja 60 + przerwa 15 + sekcja 35 + sekcja 25 (bez kartkówki),
   - każde następne spotkanie: **kartkówka 10** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25,
   - wyjątek 0104 (zamknięcie semestru zimowego): sekcja 60 + przerwa 15 + **sprawdzian semestralny 60** (pisemny, zastępuje kartkówkę; zakres 0101–0104).
   - Role sekcji: **Sekcja 1 — start i nowy materiał** (kartkówka z omówieniem, krótkie wprowadzenie, live coding), **Sekcja 2 — praktyka** (ćwiczenie samodzielne wariant A i start B, pomoc indywidualna), **Sekcja 3 — domknięcie** (warianty B/C, 5 pytań INF.03 z kluczem, podsumowanie, zadanie domowe, zapowiedź zakresu kartkówki, akcent Akademii Tarnowskiej — bez wprowadzania nowego materiału).
4. **Kartkówka od 0102 zawsze:** zakres = poprzednie spotkanie; 4–5 pytań, w tym min. 2 zamknięte w formacie INF.03 (jednokrotny wybór A–D) i 1–2 krótkie otwarte; zawsze dołącz klucz odpowiedzi, punktację i propozycję skali ocen.
5. **Min. 60% praktyki.** Wzorzec każdego zagadnienia: *krótkie wprowadzenie → live coding prowadzącego → ćwiczenie samodzielne* — mapuje się na sekcje: wprowadzenie i live coding w Sekcji 1, praca samodzielna w Sekcji 2, utrwalenie w Sekcji 3. Ćwiczenia w wariantach **A** (podstawowy), **B** (rozszerzający), **C** (gwiazdka dla szybkich) — każde z pełnym rozwiązaniem.
6. **Zakres technologiczny: wyłącznie HTML5, CSS3 i vanilla JavaScript** — bez frameworków, bez build-toolów, bez Node/npm. Jedyne odstępstwo: **0104** zawiera świadomościowy dodatek o Tailwind CSS i atomic CSS (demo porównawcze, nie nauka pisania w Tailwindzie).
7. **Zgodność z INF.03.** Egzamin: część pisemna — test 40 zadań zamkniętych, 60 min, 40 pkt; część praktyczna — praca egzaminacyjna (witryna HTML/CSS/JS, bywa PHP + baza danych SQL), 240 min, 100 pkt; próg 50% z każdej części. Gdzie się da, łącz materiał z zadaniami egzaminacyjnymi; każde spotkanie zamyka 5 pytań w stylu INF.03 z kluczem. Szczegóły w razie wątpliwości sprawdzaj w informatorze CKE (cke.gov.pl) — nie zgaduj.
8. **Promocja Akademii Tarnowskiej — subtelnie i merytorycznie:** jeden konkretny akcent na spotkanie (np. odniesienie do praktyk, projektów studenckich, kierunków, dyżurów). Zero wydźwięku reklamy.
9. **Nie wymyślaj danych ani źródeł.** Podając liczby, wskaż źródło i rok. Zweryfikowane statystyki do 0101 są w README — korzystaj z nich. Jeśli czegoś nie wiesz — powiedz to wprost i wskaż, gdzie zweryfikować.
10. **Materiały mają być gotowe do użycia na zajęciach bez dalszej edycji**: kompletny, działający kod; komentarze w kodzie po polsku; brak placeholderów typu „tutaj uzupełnij".

## Metoda ADEPT (dodatkowa zasada tej wersji)

Każde **pojęcie-brama** — kluczowe pojęcie, bez którego dalsza część zajęć nie ma sensu (2–4 na spotkanie, np. DNS, klient–serwer, DOM, box model, flexbox, responsywność, zmienna, funkcja, zdarzenie) — wprowadzaj pełną ścieżką ADEPT, **zawsze w tej kolejności**:

1. **A — Analogia.** Porównanie ze światem realnym, znanym uczniowi (np. „DNS to książka telefoniczna internetu").
2. **D — Diagram.** Wizualizacja: schemat na slajdzie, rysunek na tablicy lub prosty diagram ASCII w materiale.
3. **E — Example (przykład).** Konkretny, działający przykład: demo na żywo lub fragment kodu, który uczeń widzi w akcji.
4. **P — definicja Prosta.** Własnymi słowami, bez żargonu, 1–2 zdania.
5. **T — definicja Techniczna.** Precyzyjna, formalna — taka, jaka pojawi się na kartkówce i w zadaniach INF.03.

Zasady stosowania:

- Kolejność jest istotą metody: **od intuicji do formalizmu**, nigdy odwrotnie. Uczeń najpierw „czuje" pojęcie, dopiero potem uczy się jego precyzyjnego języka.
- ADEPT łączy się ze wzorcem 3×P z zasady 5: analogia i diagram we *wprowadzeniu*, przykład = *live coding prowadzącego*, a definicje prosta i techniczna zamykają pętlę i karmią kartkówki oraz pytania INF.03.
- Pełne ADEPT dotyczy **tylko pojęć-bram**. Pomniejszych pojęć nie rozdmuchuj — wystarczy zdanie lub analogia w tekście.
- Diagramy mają być proste (max kilka elementów); nie zamieniaj slajdu w infographic.
- Jeżeli dla pojęcia brakuje Ci dobrej analogii — nie wymyślaj na siłę; zaznacz w konspekcie „do dopracowania" i zaproponuj 2–3 kandydaty do wyboru.

## Struktura repozytorium i konwencje

```text
0101/ … 0205/  # pakiet materiałów na spotkanie {id} (0101–0104 = semestr zimowy, 0201–0205 = letni)
├── scenariusz.md      # scenariusz bazowy (overview + meta prompt) — nie zmieniaj bez potrzeby
├── konspekt.md        # konspekt z rozpiską czasową (generowany z meta promptu)
├── prezentacja.md     # outline prezentacji
├── cwiczenia/         # materiały dla uczniów (bez rozwiązań, kod bez polskich znaków w nazwach)
└── rozwiazania/       # lustrzane odbicie cwiczenia/ z kluczami i rozwiązaniami
```

- Nazwy plików i katalogów: **kebab-case, bez spacji i polskich znaków** (np. `0102-fanpage`, `formularz-kontaktowy.html`).
- Dokumenty w Markdown; kod w blokach z oznaczeniem języka (`html`, `css`, `js`).
- Pliki uczniowskie (`cwiczenia/`) nie zawierają rozwiązań — te trafiają wyłącznie do `rozwiazania/`.
- Daty, grupy (A/B) i numery wersji spotkań wpisuj w nagłówek dokumentu, gdy je znasz; w przeciwnym razie zostaw pole do uzupełnienia.

## Praca z meta promptami

Każdy scenariusz (`{id}/scenariusz.md`) ma sekcję **Meta prompt**. Dwa sposoby użycia:

- **Człowiek:** kopiuje meta prompt do dowolnego asystenta AI (instrukcja w README).
- **Ty (agent w tym repo):** gdy prowadzący pop o przygotowanie materiałów na spotkanie — zrealizuj meta prompt z odpowiedniego pliku wprost, tworząc pliki wg konwencji powyżej (prezentacja → `{id}/prezentacja.md`, ćwiczenia → `{id}/cwiczenia/`, rozwiązania → `{id}/rozwiazania/`).

Gdy polecenie użytkownika jest sprzeczne z meta promptem lub twardymi zasadami — zasady tego pliku mają pierwszeństwo, a rozbieżność wyjaśnij w odpowiedzi.

## Checklista jakości (przejdź przed oddaniem każdej partii materiałów)

- [ ] Suma czasów zgadza się z 135 min (kartkówka 10 + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25; 0101: 60 + 15 + 35 + 25; 0104: 60 + 15 + sprawdzian 60).
- [ ] Kartkówka: zakres z poprzedniego spotkania, min. 2 pytania zamknięte INF.03, klucz + punktacja.
- [ ] Kod: domknięte znaczniki, poprawne selektory, składnia JS bez literówek — przetestuj mentalnie każdą linię.
- [ ] Ćwiczenia w wariantach A/B/C, każde z pełnym rozwiązaniem; rozwiązania poza materiałami uczniowskimi.
- [ ] Nawiązanie do INF.03 + 5 pytań egzaminacyjnych z kluczem na koniec.
- [ ] Jeden subtelny akcent Akademii Tarnowskiej.
- [ ] Zadanie domowe (30–45 min pracy ucznia) + podany zakres kartkówki na następne spotkanie.
- [ ] Statystyki/twierdzenia poparte źródłem i rokiem — albo jawnie oznaczone „do weryfikacji".
- [ ] **ADEPT:** każde pojęcie-brama tego spotkania przechodzi pełną ścieżkę analogia → diagram → przykład → definicja prosta → definicja techniczna (w tej kolejności), a definicje techniczne są spójne z pytaniami kartkówki/INF.03.
