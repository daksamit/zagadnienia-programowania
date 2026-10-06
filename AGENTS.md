# AGENTS.md — instrukcje dla asystentów AI w tym repozytorium

## O repozytorium

Materiały dydaktyczne na zajęcia z podstaw webdevelopmentu (HTML5, CSS3, JavaScript) dla uczniów **czwartej klasy technikum ZST w Tarnowie** — klasy patronackie **Akademii Tarnowskiej**. Prowadzący: mgr inż. Dominik Aksamit. Pełny kontekst kursu: [README.md](README.md).

**Twoja rola:** pomagasz prowadzącemu tworzyć i aktualizować materiały: konspekty, prezentacje, kod do live codingu, kartkówki, ćwiczenia, zadania domowe, arkusze treningowe INF.03 — zawsze na bazie scenariuszy w `spotkania/`.

## Twarde zasady

1. **Język polski** we wszystkich materiałach. Materiały dla uczniów pisz bezpośrednio, per „ty” („spróbuj”, „zauważ”); konspekty dla prowadzącego — forma opisowa.
2. **Odbiorca:** uczeń 4. klasy technikum (18–19 lat). Konkret, praktyka, zero tonu akademickiego i lania wody.
3. **Struktura czasu 135 min:**
   - Z1: blok 60 + przerwa 15 + blok 60 (bez kartkówki),
   - każde następne spotkanie: **kartkówka 10** + blok 50 + przerwa 15 + blok 60.
4. **Kartkówka od Z2 zawsze:** zakres = poprzednie spotkanie; 4–5 pytań, w tym min. 2 zamknięte w formacie INF.03 (jednokrotny wybór A–D) i 1–2 krótkie otwarte; zawsze dołącz klucz odpowiedzi, punktację i propozycję skali ocen.
5. **Min. 60% praktyki.** Wzorzec każdego zagadnienia: *krótkie wprowadzenie → live coding prowadzącego → ćwiczenie samodzielne*. Ćwiczenia w wariantach **A** (podstawowy), **B** (rozszerzający), **C** (gwiazdka dla szybkich) — każde z pełnym rozwiązaniem.
6. **Zakres technologiczny: wyłącznie HTML5, CSS3 i vanilla JavaScript** — bez frameworków, bez build-toolów, bez Node/npm. Jedyne odstępstwo: **Z4** zawiera świadomościowy dodatek o Tailwind CSS i atomic CSS (demo porównawcze, nie nauka pisania w Tailwindzie).
7. **Zgodność z INF.03.** Egzamin: część pisemna — test 40 zadań zamkniętych, 60 min, 40 pkt; część praktyczna — praca egzaminacyjna (witryna HTML/CSS/JS, bywa PHP + baza danych SQL), 240 min, 100 pkt; próg 50% z każdej części. Gdzie się da, łącz materiał z zadaniami egzaminacyjnymi; każde spotkanie zamyka 5 pytań w stylu INF.03 z kluczem. Szczegóły w razie wątpliwości sprawdzaj w informatorze CKE (cke.gov.pl) — nie zgaduj.
8. **Promocja Akademii Tarnowskiej — subtelnie i merytorycznie:** jeden konkretny akcent na spotkanie (np. odniesienie do praktyk, projektów studenckich, kierunków, dyżurów). Zero wydźwięku reklamy.
9. **Nie wymyślaj danych ani źródeł.** Podając liczby, wskaż źródło i rok. Zweryfikowane statystyki do Z1 są w README — korzystaj z nich. Jeśli czegoś nie wiesz — powiedz to wprost i wskaż, gdzie zweryfikować.
10. **Materiały mają być gotowe do użycia na zajęciach bez dalszej edycji**: kompletny, działający kod; komentarze w kodzie po polsku; brak placeholderów typu „tutaj uzupełnij”.

## Struktura repozytorium i konwencje

```text
spotkania/     # scenariusze bazowe (z01–z04, l01–l05) — nie zmieniaj bez potrzeby
prezentacje/   # outline'y prezentacji: {id}-prezentacja.md (np. z02-prezentacja.md)
cwiczenia/     # materiały dla uczniów: {id}-{temat}/… (kod bez polskich znaków w nazwach plików)
rozwiazania/   # lustrzane odbicie cwiczenia/ z kluczami i rozwiązaniami
```

- Nazwy plików i katalogów: **kebab-case, bez spacji i polskich znaków** (np. `z02-fanpage`, `formularz-kontaktowy.html`).
- Dokumenty w Markdown; kod w blokach z oznaczeniem języka (`html`, `css`, `js`).
- Pliki uczniowskie (`cwiczenia/`) nie zawierają rozwiązań — te trafiają wyłącznie do `rozwiazania/`.
- Daty, grupy (A/B) i numery wersji spotkań wpisuj w nagłówek dokumentu, gdy je znasz; w przeciwnym razie zostaw pole do uzupełnienia.

## Praca z meta promptami

Każdy plik w `spotkania/` ma sekcję **Meta prompt**. Dwa sposoby użycia:

- **Człowiek:** kopiuje meta prompt do dowolnego asystenta AI (instrukcja w README).
- **Ty (agent w tym repo):** gdy prowadzący pop o przygotowanie materiałów na spotkanie — zrealizuj meta prompt z odpowiedniego pliku wprost, tworząc pliki wg konwencji powyżej (prezentacja → `prezentacje/`, ćwiczenia → `cwiczenia/`, rozwiązania → `rozwiazania/`).

Gdy polecenie użytkownika jest sprzeczne z meta promptem lub twardymi zasadami — zasady tego pliku mają pierwszeństwo, a rozbieżność wyjaśnij w odpowiedzi.

## Checklista jakości (przejdź przed oddaniem każdej partii materiałów)

- [ ] Suma czasów zgadza się z 135 min (kartkówka 10 + 50 + 15 + 60; Z1: 60 + 15 + 60).
- [ ] Kartkówka: zakres z poprzedniego spotkania, min. 2 pytania zamknięte INF.03, klucz + punktacja.
- [ ] Kod: domknięte znaczniki, poprawne selektory, składnia JS bez literówek — przetestuj mentalnie każdą linię.
- [ ] Ćwiczenia w wariantach A/B/C, każde z pełnym rozwiązaniem; rozwiązania poza materiałami uczniowskimi.
- [ ] Nawiązanie do INF.03 + 5 pytań egzaminacyjnych z kluczem na koniec.
- [ ] Jeden subtelny akcent Akademii Tarnowskiej.
- [ ] Zadanie domowe (30–45 min pracy ucznia) + podany zakres kartkówki na następne spotkanie.
- [ ] Statystyki/twierdzenia poparte źródłem i rokiem — albo jawnie oznaczone „do weryfikacji”.
