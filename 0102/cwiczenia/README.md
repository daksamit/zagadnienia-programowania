# 0102 · Ćwiczenia — „HTML5: fundamenty i semantyka + dostępność (a11y)"

Materiały dla ucznia · Technologie webowe · ZST w Tarnowie × Akademia Tarnowska

Dziś budujesz **własny fanpage**: ulubiony zespół, gracz, gra albo youtuber — wybierz temat, o którym umiesz napisać trzy zdania bez zaglądania do internetu. Fanpage będzie Twoim projektem na kolejne spotkania: na **0103 ostylujesz go w CSS3**, żeby wyglądał jak prawdziwa strona. Dziś tylko szkielet i treść — i to dobrze: najpierw fundamenty, potem wygląd.

## Zanim zaczniesz — projekt i obrazy

1. Utwórz katalog projektu, np. `fanpage`, otwórz w VS Code, utwórz w nim `index.html`.
2. Jeśli nie skończyłeś/aś live codingu — dokończ go najpierw: plik startowy („ściana divów") to [live-coding-start.html](live-coding-start.html), a finalną wersję prześle prowadzący.
3. **Obrazy do galerii** — przygotuj 3–5 plików (najlepiej własne, np. pobrane z oficjalnych profili Twojego tematu) i włóż je do katalogu `obrazy/` obok `index.html`. Wtedy w `src` wpisujesz **ścieżkę względną**, np. `obrazy/koncert.jpg`. Nie masz plików? Użyj obrazków poglądowych: `https://placehold.co/600x400?text=Opis` albo `https://picsum.photos/seed/twoj-temat/600/400` — spójrz, co się wyświetliło, i **właśnie to opisz w `alt`**.

Podgląd: prawy przycisk na `index.html` → **Open with Live Server**; po każdej zmianie Ctrl+S (Cmd+S).

## Ściąga: typy pola `<input>` — które do czego

| Typ | Co robi / kiedy użyć | Co sam pilnuje przeglądarka |
|---|---|---|
| `text` | krótki tekst: imię, nazwa | nic — sam dodajesz `required`, `minlength` |
| `email` | adres e-mail | format adresu (`@`, domena) |
| `number` | liczba: wiek, ilość | cyfry + zakres z `min`/`max` |
| `date` | data | kalendarz do kliknięcia |
| `password` | hasło | znaki zamaskowane kropkami |
| `radio` | wybór **jednej** opcji z pary/kilku (ta sama nazwa `name`!) | zaznaczenie max. 1 z grupy |
| `checkbox` | zgody, tak/nie | przełącznik |
| `file` | wybór pliku z dysku | okno wyboru pliku |
| `color` | wybór koloru | próbnik kolorów |
| `range` | suwak (np. skala 1–10) | suwak z `min`/`max` |

Do dłuższego tekstu: `<textarea>`; wybór z listy: `<select>` + `<option>`.

## Wariant A (podstawowy) — szkielet fanpage'u

Zbuduj kompletną stronę (sam szkielet — bez CSS, wygląd przyjdzie na 0103):

- [ ] szkielet dokumentu z 0101: `<!DOCTYPE html>`, `html lang="pl"`, `head` z `meta charset`, `viewport` i `title`,
- [ ] **`header`**: `h1` z nazwą tematu + jedno zdanie-hasło w `p`,
- [ ] **`nav`**: lista `ul` z 3–5 linkami do sekcji strony (`href="#id"` — sekcje muszą mieć te `id`),
- [ ] **`main`** z co najmniej **dwoma sekcjami**: „O …" (2–3 akapity `p` + lista `ul` lub `ol`) i **galeria**,
- [ ] galeria: **minimum 3 obrazy** `img`, każdy z `alt` opisującym, co widać, i z `width`/`height` (podpisane obrazy? bonus: `figure` + `figcaption`),
- [ ] **`footer`**: info, że to fanpage szkolny + link zewnętrzny do oficjalnej strony tematu (`target="_blank"` + `rel="noopener"`),
- [ ] **formularz zapisu** w osobnej sekcji: imię (`type="text"`, `required`), e-mail (`type="email"`, `required`), zgoda (`checkbox`, `required`), przycisk `button` — każde pole z `label` powiązanym `for`/`id`.

Sprawdź przed oddaniem: linki w `nav` skaczą do sekcji; wszystkie obrazy się wyświetlają; wysłanie pustego formularza blokuje przeglądarka.

## Wariant B (rozszerzający) — dla tych, którzy skończyli A

- [ ] **tabela danych** związana z tematem (np. dyskografia, wyniki/statystyki gracza, wymagania gry): `table` + `caption` + `thead` z `th` + `tbody` z `td`, minimum 3 wiersze danych,
- [ ] rozszerz formularz: **`select`** (np. „skąd znasz…") i **`radio` w `fieldset` z `legend`** (np. wybór jednej opcji) + po jednym polu `number` (z `min`/`max`) i `date`,
- [ ] **multimedia**: wstaw `iframe` z filmem powiązanym z tematem (pamiętaj o `title` ramki!) albo `audio`/`video` z `controls`.

Sprawdź przed oddaniem: tabela ma nagłówki `th` i tytuł `caption`; radio pozwala wybrać tylko jedną opcję; walidacja pól `number`/`date` działa.

## Wariant C ⭐ (gwiazdka, dla najszybszych) — fanpage bez myszy

1. Dokoncz/porządkuj **menu wewnętrzne**: każda sekcja ma `id`, `nav` linkuje do każdej z nich; na końcu każdej sekcji dodaj link „↑ wróć na górę" prowadzący do `#` nagłówka strony.
2. **Odłóż mysz.** Kliknij pasek adresu, a potem przechodź całą stronę samym **Tabem**: link po linku, pole po polu, aż do przycisku formularza. Odhaczaj: czy da się dotrzeć wszędzie? Czy kolejność ma sens? Czy widać, co jest zaznaczone (obwódka fokusu)?
3. Napraw znalezione problemy (np. link „czytaj dalej" — czy poza kontekstem wiadomo, dokąd prowadzi?).
4. **Dla bohaterów:** dodaj na samej górze strony link „Przejdź do treści" prowadzący do `main` (`id="tresc"`) — pierwszy prawdziwy trik dostępności, zanim w ogóle poznasz ARIA.

## Checklista dostępności (a11y) — samokontrola fanpage'a

Przejdź przed oddaniem; to samo będzie na liście kontrolnej arkusza praktycznego:

- [ ] każdy `img` ma `alt`, który **opisuje treść** (nie „obrazek", nie „foto"),
- [ ] `html lang="pl"` jest ustawiony,
- [ ] dokładnie **jeden `h1`**, a dalej nagłówki **po kolei** (`h2` → `h3`, bez przeskoku h2 → h5),
- [ ] każde pole formularza ma `label` powiązany `for`/`id`,
- [ ] całą stronę da się przejść **samym Tabem** (mysz pod biurko!),
- [ ] teksty linków mówią, dokąd prowadzą (unikaj samego „tutaj"),
- [ ] `iframe` ma `title`,
- [ ] tabela danych ma `caption` i `th` w nagłówkach.

## Zadanie domowe (30–45 min)

1. **Dokończ fanpage** (wariant A; jeśli zdążyłeś/aś — dopracuj B) i przelicz go przez checklistę a11y wyżej — każdą odhaczoną pozycję zostaw w kodzie świadomie.
2. **Detektyw dostępności**: znajdź w internecie stronę z oczywistym błędem dostępności (brak `alt` przy obrazkach, „ściana divów", nagłówki pomieszane). Zapisz **adres strony** i **co jest nie tak** — pierwsze znaleziska omówimy na 0103.
3. **Przygotuj się do kartkówki** — zakres niżej.

**Nie kasuj projektu!** Na 0103 twój fanpage dostanie kolory, fonty i układ (flexbox), a na 0104 go opublikujemy. Trzymaj katalog `fanpage/` z obrazami w jednym kawałku.

## Kartkówka na 0103 — dokładny zakres

Na następnym spotkaniu (**0103 — CSS3: stylowanie i responsywność**) zajęcia zaczną się **10-minutową kartkówką** z dzisiejszego materiału:

- **semantyka**: czym się różni `article` od `section`, po co `nav`/`header`/`footer`, kiedy `div` wystarczy,
- **typy `input`**: dobierz typ do danych (e-mail, liczba, data, jedna opcja z wielu, zgoda),
- **formularze i walidacja HTML5**: `label` + `for`/`id`, `required`, `pattern`, `min`/`max`,
- **tabele**: `th` vs `td`, `caption`, `thead`/`tbody`,
- **a11y**: `alt`, kolejność nagłówków, nawigacja Tabem.

Będą pytania zamknięte (A–D, jak na egzaminie INF.03) i krótkie otwarte — podobnie jak dzisiaj.

---

Masz pytania albo coś nie działa? Pytaj na bieżąco — na zajęciach lub mailowo. A jeśli wolisz najpierw spróbować samodzielnie: poproś AI z ściągi 0101 (ELI5: „wyjaśnij różnicę między article i section, jakbym miał 15 lat") i sprawdź odpowiedź w [MDN](https://developer.mozilla.org/pl/docs/Web/HTML).
