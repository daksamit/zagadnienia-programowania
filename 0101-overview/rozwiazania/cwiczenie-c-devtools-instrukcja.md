# 0101 · Wariant C - instrukcja oczekiwanego efektu (DevTools)

Materiał dla prowadzącego. Wariant C nie ma „pliku rozwiązania" - produktem ucznia są dwa zrzuty ekranu (`przed.png`, `po.png`). Poniżej: wzorcowy przebieg, oczekiwany efekt i typowe problemy.

## Wzorcowy przebieg (uczniowie znają go z instrukcji w `0101/`)

1. Uczeń otwiera w Chrome dowolną ulubioną stronę (do demonstracji polecaj `https://www.zst.tarnow.pl` - znana wszystkim i ma czytelną strukturę).
2. Zrzut ekranu „przed" - na obrazie ma być widoczny oryginalny nagłówek strony.
3. F12 → panel **Elements** → ikona wskaźnika (lub Ctrl+Shift+C) → kliknięcie głównego nagłówka → dwuklik na tekst węzła w drzewie → wpisanie własnego tekstu → Enter.
4. Panel **Styles** przy zaznaczonym elemencie → dopisanie deklaracji, np. `color: crimson;` i `background-color: gold;` - natychmiastowy efekt na stronie.
5. Zrzut ekranu „po" - ma pokazywać zmieniony nagłówek i zmienione kolory.
6. F5 → strona wraca do oryginału.

## Oczekiwany efekt

- `przed.png`: nienaruszona oryginalna strona,
- `po.png`: ta sama kategoria elementu z widocznie zmienioną treścią nagłówka oraz kolorem tekstu/tła,
- uczeń potrafi jednym zdaniem wyjaśnić, dlaczego po F5 zmiany zniknęły: **edycja była lokalna, w pamięci przeglądarki; odświeżenie pobiera pliki ponownie z serwera** - to główny cel dydaktyczny wariantu, ważniejszy niż efektowność przeróbki.

## Typowe problemy i reakcja prowadzącego

| Objaw | Przyczyna | Pomoc |
|---|---|---|
| Nie widzą podświetlenia elementu | klikają w stronę bez włączonego trybu wskaźnika | Ctrl+Shift+C, potem klik w nagłówek |
| Dwuklik otwiera edycję, ale Enter ją przerywa bez zmian | edytowali tag zamiast treści tekstowej | dwuklik dokładnie na tekście wewnątrz znacznika |
| Zmiany w Styles „znikają" od razu | literówka w deklaracji CSS (np. `colour:`) lub brak średnika | pokaż czerwoną ikonę ostrzeżenia przy błędnej linii |
| Strona wygląda „rozjechanie" po wyczyszczeniu stylów | usunęli za dużo w drzewie HTML | F5 - i przypomnij: nic trwałego się nie stało, wszystkie zmiany są odwracalne odświeżeniem |
| Screenshot po F5 zamiast przed | zmiany zniknęły przed zrobieniem zrzutu | zrobią ponownie - ćwiczenie trwa 2 minuty |

## Punktacja (propozycja, jeśli chcesz ocenić gwiazdkę)

- zrzut „przed" + „po" widocznie różne (nagłówek + kolor): zaliczone,
- poprawne wyjaśnienie znikania zmian po F5 (pytanie ustne): pełna wartość ćwiczenia - bez tego zrzuty to tylko zabawa.
