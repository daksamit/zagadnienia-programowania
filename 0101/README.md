# 0101 · Materiały dla ucznia - „Dlaczego web? Wstęp, przeglądarki i DevTools"

Technologie webowe · ZST w Tarnowie × Akademia Tarnowska

Ten pakiet to wszystko, czego potrzebujesz na pierwszych zajęciach: ta instrukcja, [ściąga](0101-cheatsheet.md) i [poradnik](0101-materialy-dydaktyczne.md) do powtórki oraz mini-ściąga [„AI jako tutor"](ai-jako-tutor-sciega.md). Rozpiska prowadzącego, ankieta i rozwiązania zostają u niego.

Dziś napiszesz swoją pierwszą stronę internetową. Potrzebujesz: VS Code z rozszerzeniem Live Server, przeglądarkę Chrome i ~35 minut pracy na zajęciach (resztę dokończysz w domu).

## Plan spotkania - 3 bloki

| Blok | Czas | Co się dzieje |
|---|---|---|
| 1 | 0:00–0:45 | ankieta zapoznawcza na start (nieoceniana) · zasady zajęć i oceniania · historia WWW · web w liczbach · jak działa internet: klient–serwer, DNS, HTTP(S), URL |
| 2 | 0:45–1:30 | przeglądarki i silniki · mapa semestru i egzamin INF.03 · *przerwa 15 min* · **Chrome DevTools w praktyce**: edycja strony na żywo i dlaczego F5 przywraca oryginał |
| 3 | 1:30–2:15 | warsztat **VS Code + Live Server** · AI jako tutor (dostaniesz ścięgę z promptami) · **live coding: Twoja pierwsza strona HTML** · ćwiczenie „Kim jestem" (warianty A/B/C) |

Prowadzący pokazuje każdy element na żywo - **Ty piszesz razem z nim** we własnym projekcie, a potem robisz ćwiczenie samodzielnie. Mieć otwarte od początku zajęć: VS Code z Live Server i przeglądarkę Chrome.

Nie masz VS Code pod ręką? Żaden problem - zamiast instalować cokolwiek, możesz kodować w przeglądarce: otwórz **StackBlitz** (`stackblitz.com`) lub **CodeSandbox** (`codesandbox.io`), utwórz nowy projekt HTML i działaj tam. Efekt będzie ten sam: kod z jednej strony, podgląd strony z drugiej.

## Zanim zaczniesz - szkielet do skopiowania

Utwórz katalog projektu (np. `kim-jestem`), otwórz go w VS Code, utwórz w nim plik **`index.html`** i wklej poniższy szkielet. To jest dokładnie ten szkielet, który pisaliśmy razem na zajęciach:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kim jestem</title>
</head>
<body>
  <!-- tutaj pisz treść swojej strony -->
</body>
</html>
```

Podgląd: kliknij plik prawym przyciskiem → **Open with Live Server**. Po każdej zmianie zapisz (Ctrl+S / Cmd+S) - strona odświeży się sama.

> **Trzy adresy, jedna strona.** Tę samą stronę możesz otworzyć na trzy sposoby - zawsze zerkaj na początek adresu w pasku przeglądarki:
>
> - `file:///…` - dwuklik na pliku: przeglądarka czyta go **prosto z dysku, bez serwera i bez HTTP** (tryb awaryjny - przy prostych stronach wystarczy, ale ma ograniczenia),
> - `http://127.0.0.1:5500` - Live Server: **prawdziwy serwer HTTP działający na Twoim komputerze**. Adres `127.0.0.1` to tzw. **localhost** - „ten komputer": Twój laptop jest jednocześnie klientem i serwerem. Tak pracujemy na zajęciach.
> - `https://…` - serwer **produkcyjny** w internecie (np. `zst.tarnow.pl`). Swoją stronę opublikujemy tak na 0104.

## Wariant A (podstawowy) - strona „Kim jestem"

Napisz prostą stronę o sobie. Wymagania:

- [ ] nagłówek główny `h1` z Twoim imieniem (lub ksywką),
- [ ] co najmniej **2 akapity** (`p`) o Tobie: kim jesteś, czym się zajmujesz, co Cię kręci,
- [ ] sekcja „Moje zainteresowania": nagłówek `h2` + **lista nieuporządkowana** (`ul`) z co najmniej 4 pozycjami (`li`),
- [ ] **link** (`a`) do strony, którą lubisz odwiedzać - z atrybutem `href`,
- [ ] strona zapisana jako `index.html`, tytuł karty (`title`) ustawiony na „Imię Nazwisko - kim jestem".

Sprawdź przed oddaniem: polskie znaki wyświetlają się poprawnie, link działa po kliknięciu, lista ma znaczniki (kropki).

## Wariant B (rozszerzający) - dla tych, którzy skończyli A

Rozbuduj stronę z wariantu A:

- [ ] dodaj **obrazek** (`img`): własne zdjęcie/grafikę położoną w katalogu strony (np. `zdjecie.jpg`) albo przykładowy z adresu `https://picsum.photos/600/400`,
- [ ] obrazek musi mieć wypełniony atrybut **`alt`** (opis: co widać na obrazku) oraz atrybuty `width` i `height`,
- [ ] dodaj sekcję **„Moje cele na ten rok"**: nagłówek `h2` + **lista uporządkowana** (`ol`) z co najmniej 3 celami (numerowana - kolejność ma znaczenie!).

Sprawdź przed oddaniem: obrazek się wyświetla (a jeśli nie - widać tekst z `alt`), cele są ponumerowane.

## Wariant C ⭐ (gwiazdka, dla najszybszych) - przeróbka cudzej strony w DevTools

Uwaga: zrób **zrzuty ekranu przed odświeżeniem strony** - po F5 wszystkie zmiany znikną!

1. Otwórz w Chrome swoją ulubioną stronę.
2. Zrób **zrzut ekranu „przed"** (np. Cmd+Shift+4 na macOS, Win+Shift+S na Windows).
3. Otwórz DevTools (F12), w panelu **Elements** znajdź główny nagłówek strony i zmień jego tekst na dowolny (pamiętaj o dobrych manierach 😉).
4. W panelu **Styles** zmień kolor tekstu (`color:`) i tło (`background-color:`) wybranego elementu.
5. Zrób **zrzut ekranu „po"**.
6. Wciśnij F5 i pokaż, że strona wróciła do oryginału - zrozum, dlaczego.

Zapisz oba zrzuty jako `przed.png` i `po.png` - pokażesz je na następnych zajęciach.

## Zadanie domowe (30–40 min)

1. **Dokończ stronę „Kim jestem"** (wariant A; jeśli zdążyłeś/aś - dopracuj B).
2. **Detektyw stron**: znajdź 2–3 strony, które Ci się podobają, podejrzyj je w DevTools (panel Elements) i zastanów się, z jakich elementów są zbudowane (nagłówki, listy, obrazki, linki).
3. **AI jako tutor**: wypróbuj 2 prompty z mini-ściągi [ai-jako-tutor-sciega.md](ai-jako-tutor-sciega.md) - np. ELI5 na temat „jak działa DNS".
4. **Przygotuj się do kartkówki** - zakres: historia WWW · klient–serwer (DNS, HTTP(S), URL) · Chrome DevTools · szkielet HTML.

## Kartkówka na 0102 - dokładny zakres

Na następnym spotkaniu (0102 - HTML5: semantyka, formularze, dostępność) zajęcia zaczną się **10-minutową kartkówką** z dzisiejszego materiału:

- **historia WWW**: 1989 Tim Berners-Lee (CERN), 1991 pierwsza strona, 1995 JavaScript,
- **klient–serwer**: kto jest kim, co robi DNS, czym różni się HTTP od HTTPS, z czego składa się URL, co oznacza adres 127.0.0.1 (localhost),
- **DevTools**: jak otworzyć, co robi panel Elements, dlaczego zmiany znikają po odświeżeniu,
- **szkielet HTML**: `<!DOCTYPE html>`, `html lang="pl"`, `head` (meta charset, viewport, title) i `body`.

Będą pytania zamknięte (A–D, jak na egzaminie INF.03) i krótkie otwarte.

---

## Materiały do powtórki

- [Ściąga 0101](0101-cheatsheet.md) - wszystko z zajęć na jednej stronie: historia, klient–serwer, DevTools, szkielet HTML.
- [Poradnik 0101](0101-materialy-dydaktyczne.md) - wersja rozszerzona: kompletne wyjaśnienia wszystkich terminów i pojęć oraz słowniczek A–Z.

## Przydatne linki

- [MDN Web Docs - HTML po polsku](https://developer.mozilla.org/pl/docs/Web/HTML) - encyklopedia webowych technologii od ludzi pilnujących standardów; pierwsze miejsce, gdzie sprawdzisz każdy znacznik (będzie służyć też na kolejnych spotkaniach).
- [Dokumentacja Chrome DevTools po polsku](https://developer.chrome.com/docs/devtools?hl=pl) - oficjalny przewodnik Google po panelach, które poznałeś/aś dziś (Elements, Console); uwaga: tłumaczenie automatyczne, ale zrozumiałe.
- [web.dev - Learn HTML](https://web.dev/learn/html/) - darmowy kurs HTML od zespołu Google (po angielsku, ale prostym); świetne uzupełnienie dzisiejszego live codingu.
- [StackBlitz](https://stackblitz.com) i [CodeSandbox](https://codesandbox.io) - edytory kodu w przeglądarce: zero instalacji, ratunek, gdy pracujesz na cudzym komputerze.
- [Internet Live Stats](https://www.internetlivestats.com/total-number-of-websites/) - licznik stron internetowych na żywo; stąd pochodzi liczba „ponad 1,2 mld stron" z dzisiejszych slajdów.

---

Masz pytania albo coś nie działa? Pierwsza zasada z dzisiejszych zajęć: **pytaj na bieżąco** - na zajęciach lub mailowo. A jak wolisz najpierw spróbować samodzielnie - sięgnij po mini-ścięgę AI.
