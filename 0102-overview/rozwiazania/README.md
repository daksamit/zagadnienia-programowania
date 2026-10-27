# 0102 · Rozwiązania i klucze - „HTML5: fundamenty i semantyka + a11y"

Materiały **wyłącznie dla prowadzącego** - nie przekazuj uczniom. Dotyczą ćwiczeń z pakietu ucznia: [0102/](../../0102/README.md).

| Plik | Zawartość |
|---|---|
| [kartkowka-klucz.md](kartkowka-klucz.md) | klucz kartkówki nr 1 (zakres 0101), punktacja 0–5, skala ocen, scenariusz omówienia |
| [live-coding/index.html](live-coding/index.html) | finalny plik z live codingu (etapy 1–14 z konspektu) - do wysłania uczniom, którzy nie nadążyli; start („ściana divów") uczniowie mają w [0102/index.html](../../0102/index.html) |
| [cwiczenie-a/index.html](cwiczenie-a/index.html) | pełne rozwiązanie wariantu A (przykład: fanpage gry „Orbita: Ostatnia Stacja") |
| [cwiczenie-b/index.html](cwiczenie-b/index.html) | pełne rozwiązanie wariantu B (A + tabela + `select`/`radio` w `fieldset` + multimedia) |
| [cwiczenie-c-fanpage-instrukcja.md](cwiczenie-c-fanpage-instrukcja.md) | wariant C: wzorcowy przebieg (zakotwiczenia + audyt Tabem), oczekiwany efekt, typowe problemy |
| [bonus-cyber-phishing-klucz.md](bonus-cyber-phishing-klucz.md) | klucz bonusu ⭐ „detektyw phishingu" (8 czerwonych flag, eksperyment GET vs POST, scenariusz omówienia) - dobrowolny, bez oceny |
| [pytania-inf03-z-kluczem.md](pytania-inf03-z-kluczem.md) | 5 pytań w stylu INF.03 (+2 zamienne) z kluczem i uzasadnieniami - **baza kartkówki na 0103** |

## Ocena ćwiczeń - minimum, o które pytamy

**Wariant A** - uczeń rozumie (a nie tylko przepisał): różnicę `header`/`nav`/`main`/`footer`, że nav linkuje do `id` sekcji, że `alt` opisuje treść obrazu, a nie jest wypełniaczem. Pytanie kontrolne: „co się stanie po kliknięciu pozycji w menu?" (skok do sekcji o danym `id`) albo „co usłyszy osoba niewidoma przy Twoim obrazku?".

**Wariant B** - dopilnuj: tabela ma `caption` i `th` w `thead` (nie „ładny szablon" z samymi `td`); radio w `fieldset` z `legend` i wspólnym `name`; po jednym pytaniu o `min`/`max` („co się stanie przy 99 latach stażu?").

**Wariant C** - kluczowa jest obserwacja z audytu Tabem, nie liczba poprawek. Pytanie kontrolne: „po co komu strona obsługiwana samą klawiaturą?" (osoby nie używające myszy, czytniki ekranu, dyskomfort ruchowy).

## Częste błędy uczniów na tym spotkaniu - na co patrzeć przy sprawdzaniu

- `label` bez `for` albo `for` niepasujące do `id` (klik w etykietę nie uaktywnia pola),
- `h1` w każdej sekcji zamiast jednego `h1` i `h2`/`h3` w sekcjach; przeskoki h2 → h5,
- `alt="obrazek"` / `alt="foto"` - technicznie obecny, bezużyteczny dla a11y,
- tabela bez `caption`, nagłówki wpisane jako `td` zamiast `th`,
- radio z różnymi `name` - da się zaznaczyć wszystkie naraz (klasyczny błąd, warty pokazania całej klasie).
