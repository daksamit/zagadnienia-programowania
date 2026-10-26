# 0102 · Klucz kartkówki nr 1 — zakres: 0101 „Dlaczego web?"

Materiał **wyłącznie dla prowadzącego**. Arkusz dla ucznia: [../kartkowka.md](../kartkowka.md). Czas pisania: 8 min (+1 min rozdanie, +1 min zbiór).

## Klucz odpowiedzi

| Pytanie | Odpowiedź | Punkty |
|---|---|---|
| 1 (zamknięte, DNS) | **B** | 1 |
| 2 (zamknięte, `title`) | **B** | 1 |
| 3 (zamknięte, HTTPS) | **A** | 1 |
| 4 (otwarte, szkielet) | kompletny szkielet — kryterium poniżej | 1 |
| 5 (otwarte, DevTools + F5) | istota: zmiany są lokalne, F5 pobiera pliki ponownie z serwera | 1 |

**Razem: 0–5 pkt.**

### Pytanie 4 — wzór i kryterium (1 pkt za komplet)

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Kartkówka</title>
</head>
<body>
</body>
</html>
```

1 pkt — wszystkie elementy obecne i we właściwych miejscach: `<!DOCTYPE html>`, `<html lang="pl">`, `head` z `meta charset="UTF-8"` i `title`, pusty `body`. Brak `lang="pl"` **lub** brak `meta charset` = 0 pkt (to dwa akcenty 0101, o które pytały ćwiczenia). `meta viewport` nie jest wymagany (bonus, nie odejmujemy). Drobne literówki w znacznikach (np. `</hed>`) = 0 pkt — przeglądarka by ich nie zrozumiała.

### Pytanie 5 — przykładowa pełna odpowiedź

„Zmiana zniknie, bo była zapisana tylko lokalnie, w pamięci mojej przeglądarki; F5 pobiera pliki strony ponownie z serwera, więc wraca oryginał." 1 pkt za obie składowe: (a) zmiany tylko lokalne, (b) odświeżenie pobiera oryginał z serwera.

## Propozycja skali ocen

| Punkty | Ocena |
|---|---|
| 5 | 5 (bardzo dobra) |
| 4 | 4 (dobra) |
| 3 | 3 (dostateczna) |
| 2 | 2 (dopuszczająca) |
| 0–1 | 1 (niedostateczna) |

Skala jest propozycją — w razie potrzeby stosuj pół punktu za pytania otwarte (np. 0,5 pkt za szkielet z jednym brakiem). Kartkówka jest **oceną cząstkową** i wchodzi do oceny na koniec roku.

## Po zbiórce: omówienie (2 min na początku Sekcji 1)

1. Pytanie 2 — najczęstszy błąd: `h1` zamiast `title`. Powiedz: „`h1` to nagłówek **na stronie**, `title` to napis **na karcie** — to nie to samo i na INF.03 lubią to mieszać."
2. Pytanie 5 — upewnij się, że wszyscy rozumieją: DevTools edytuje **kopię strony w pamięci**, nie pliki na serwerze.
3. Wyniki wrócić uczniom na 0103 (przed kartkówką z 0102).
