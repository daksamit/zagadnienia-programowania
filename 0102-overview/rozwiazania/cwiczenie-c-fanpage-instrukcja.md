# 0102 · Wariant C — instrukcja oczekiwanego efektu (zakotwiczenia + audyt Tabem)

Materiał dla prowadzącego. Wariant C nie ma jednego „pliku rozwiązania" — produktem ucznia jest **poprawiona własna strona** (menu wewnętrzne + strona dająca się przejść Tabem) i krótkie zestawienie znalezionych problemów. Poniżej: wzorcowy przebieg, oczekiwany efekt, typowe problemy.

## Wzorcowy przebieg (uczniowie znają go z instrukcji w `cwiczenia/`)

1. **Menu wewnętrzne** — każda sekcja ma `id`, `nav` linkuje do każdej z nich; na końcu każdej sekcji link „↑ wróć na górę":

```html
<!-- w nav: link do zakotwiczenia -->
<li><a href="#galeria">Galeria</a></li>

<!-- sekcja o tym samym id -->
<section id="galeria"> ... </section>

<!-- koniec sekcji: powrót na górę (id="gora" siedzi na headerze) -->
<p><a href="#gora">↑ wróć na górę</a></p>

<header id="gora"> ... </header>
```

2. **Audyt Tabem** — uczeń klika pasek adresu, odkłada mysz i przechodzi całą stronę samym Tabem: nav → linki sekcji → linki w treści → pola formularza → przycisk. Odhacza: dotrzę wszędzie? kolejność logiczna? widać fokusz?
3. **Poprawa znalezionych problemów** — najczęściej: niejednoznaczne teksty linków, brak fokusu na jakimś elemencie interaktywnym, label przed checkboxem zamiast po.
4. **Bonus „dla bohaterów"** — skip-link na samej górze strony:

```html
<!-- pierwszy element w body: link niewidoczny dopóki nie dostanie fokusu (styl dodamy na 0103) -->
<a href="#tresc">Przejdź do treści</a>

<main id="tresc"> ... </main>
```

## Oczekiwany efekt

- klik w każdą pozycję `nav` przewija do właściwej sekcji (a „wróć na górę" — do nagłówka),
- przejście Tabem od góry do przycisku formularza działa **bez myszy** i w logicznej kolejności,
- uczeń potrafi wskazać co najmniej jedno **znalezione i naprawione** utrudnienie (np. zmienione „tutaj" na „koncert w Krakowie — bilety"),
- bonus: skip-link obecny w kodzie na początku `body`.

Najważniejsze jest zdanie kontrolne: **„po co to komu?"** — oczekiwana odpowiedź: dla osoby, która nie używa myszy (nawigacja klawiaturą, czytniki ekranu); skip-link oszczędza nasłuchiwanie całego menu przy każdej podstronie.

## Typowe problemy i reakcja prowadzącego

| Objaw | Przyczyna | Pomoc |
|---|---|---|
| Klik w menu nic nie robi | literówka: `href="#Galeria"` vs `id="galeria"` — zakotwiczenia są **czułe na wielkość liter** | pokaż w DevTools, że element nie ma szukanego `id` |
| „Wróć na górę" przewija tylko trochę | `id="gora"` nadane elementowi w połowie strony | `id` musi być na `header` (lub pierwszym elemencie) |
| Tab przeskakuje jakieś pole | `label` niepowiązany z polem (brak `for`/`id`) — sam label nie jest wtedy klikalny | dopasuj `for` z `id` |
| Nie widać, co jest zaznaczone | przeglądarka domyślnie pokazuje obwódkę — jeśli jej nie ma, ktoś (strona) ją usuwa | u nas nie wystąpi — czysty HTML; zapowiedz, że na 0103 pilnujemy `:focus-visible` |
| Tab wchodzi w `iframe` | YouTube „połyka" fokus | to znane utrudnienie; wystarczy, że uczeń je **zaobserwuje** i zanotuje |

## Punktacja (propozycja, jeśli chcesz ocenić gwiazdkę)

- zakotwiczenia działają w obie strony + strona daje się przejść Tabem od góry do formularza: zaliczone,
- jedno znalezione i nazwane problematyczne miejsce + poprawka: pełna wartość ćwiczenia,
- skip-link: ponad program — pochwała na forum (i materiał na 0103, gdy wrócimy do a11y przy kontraście).
