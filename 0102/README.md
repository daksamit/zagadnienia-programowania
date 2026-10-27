# 0102 · Materiały dla ucznia - „HTML5: fundamenty i semantyka + dostępność (a11y)"

Technologie webowe · ZST w Tarnowie × Akademia Tarnowska

Ten pakiet to wszystko, czego potrzebujesz na dzisiejszych zajęciach: ta instrukcja oraz start do live codingu - plik [index.html](index.html) („ściana divów"). Rozpiska prowadzącego, kartkówka i rozwiązania zostają u niego.

Dziś budujesz **własny fanpage**: ulubiony zespół, gracz, gra albo youtuber - wybierz temat, o którym umiesz napisać trzy zdania bez zaglądania do internetu. Fanpage będzie Twoim projektem na kolejne spotkania: na **0103 ostylujesz go w CSS3**, żeby wyglądał jak prawdziwa strona. Dziś tylko szkielet i treść - i to dobrze: najpierw fundamenty, potem wygląd.

## Plan spotkania - 3 bloki

| Blok | Czas | Co się dzieje |
|---|---|---|
| 1 | 0:00–0:45 | kartkówka z 0101 (10 min) · „ściana divów" → **szkielet semantyczny** · tekst i listy · linki i zakotwiczenia · obrazy: `img`, `src`, `alt` |
| 2 | 0:45–1:30 | obrazy cd.: formaty i `figure` · **dostępność (a11y)** i 4 zasady WCAG · *przerwa 15 min* · tabele danych · multimedia: `video`, `audio`, `iframe` |
| 3 | 1:30–2:15 | **formularz z walidacją HTML5** (live coding krok po kroku) · **Twój fanpage** - warianty A/B/C · mini-quiz, podsumowanie, zapowiedź 0103 |

Prowadzący pokazuje każdy element na żywo - **Ty piszesz razem z nim** we własnym projekcie, a potem robisz fanpage samodzielnie. Mieć otwarte od początku zajęć: VS Code z Live Server i przeglądarkę.

## Jak o tym myśleć - zanim zaczniesz pisać znaczniki

Cały dzisiejszy dzień sprowadza się do czterech modeli myślowych. Są ważniejsze niż zapamiętanie listy znaczników - działają też przy elementach, których jeszcze nie znasz.

### Semantyka: HTML opisuje znaczenie, nie wygląd

Stronę czytają dwaj czytelnicy: **człowiek** (widzi układ i obrazy) i **maszyna** (czytnik ekranu, robot wyszukiwarki, przeglądarka). Wygląd załatwia CSS - na 0103. HTML odpowiada na jedno pytanie: **czym ta treść jest?**

Zadawaj je kaskadowo, dla każdego kawałka strony:

1. **Jaka to część strony?** - nagłówek strony (`header`), nawigacja (`nav`), główna treść (`main`), treść poboczna (`aside`), stopka (`footer`).
2. **Jeśli to treść: czym ona jest?** - samodzielna całość, która ma sens nawet wyrwana z kontekstu (`article`)? sekcja z własnym nagłówkiem (`section`)? zwykły akapit (`p`)?
3. **Jeśli fragment wewnątrz zdania: niesie znaczenie?** - waga (`strong`), akcent (`em`), cytat (`blockquote`) - czy tylko grupuje bez znaczenia (`span`)?

`div` nie jest zły - to uczciwe pudełko bez znaczenia, do grupowania. Problem zaczyna się, gdy `div` stoi tam, gdzie znaczenie istnieje: „ściana divów" wygląda identycznie dla człowieka, ale dla maszyny to pusta kartka.

Obszary semantyki, które dziś ćwiczysz - i w każdym obowiązuje to samo pytanie „czym to jest?": **struktura dokumentu** (szkielet strony), **semantyka tekstu** (`strong`, `em`, listy, cytaty), **media** (`alt`, `figure`), **dane** (`table`), **interakcja** (formularze).

### a11y: nie dodatek, tylko funkcja HTML

Dlaczego w ogóle o tym mówimy - trzy powody, każdy innego rodzaju:

- **ludzki**: 1 na 6 ludzi na świecie żyje z niepełnosprawnością (WHO, 2023) - to realni użytkownicy Twoich stron,
- **prawny**: unijne wymogi dostępności usług online (European Accessibility Act) obowiązują od 28 czerwca 2025,
- **praktyczny**: dostępność jest punktowana w arkuszach INF.03, a strona dostępna jest po prostu lepsza dla wszystkich - `alt` czyta też wyszukiwarka obrazów, a porządek nagłówków pomaga każdemu, kto skanuje stronę wzrokiem.

### a11y w praktyce: trzy filtry zamiast regułek

Nie ucz się zasad na pamięć - przepuść stronę przez trzy pytania kontrolne:

1. **Co usłyszę zamiast zobaczyć?** Czytnik ekranu czyta `alt` zamiast obrazu, po nagłówkach nawiguje jak po spisie treści, a przy polu formularza odczytuje jego `label`. Stąd: `alt` opisujący treść, dokładnie jeden `h1` i nagłówki po kolei, `label` przy każdym polu, `lang="pl"`.
2. **Czy strona działa bez myszy?** Nie każdy używa myszy. Sprawdź: całą stronę da się przejść Tabem, widać obwódkę fokusu, link mówi, dokąd prowadzi (bo bez myszy nie „celujesz wzrokiem").
3. **Co z tego zrozumie robot?** W uproszczeniu: to samo, co czytnik ekranu. Strona bez semantyki to dla robota ściana tekstu - dlatego semantyka i a11y to jedna bajka, nie dwa osobne tematy.

Cała checklista a11y (niżej w tym pliku) to właśnie te trzy filtry, wypisane punkt po punkcie.

### Formularze: rozmowa, którą pilnuje przeglądarka

Formularz to rozmowa z użytkownikiem, nie zbiór pudełek. Każde pole zaprojektuj czterema krokami:

1. **Jakie dane zbieram?** - e-mail, liczba, data, jedna opcja z wielu, zgoda…
2. **Który typ to opisze?** - `email`, `number`, `date`, `radio`, `checkbox`… typ to nie ozdoba: przeglądarka daje za darmo właściwą klawiaturę na telefonie (np. `@` pod palcem przy e-mailu) i sprawdzanie formatu. `text` do wszystkiego marnuje te prezenty - ściąga z typami jest niżej.
3. **Jak pole się nazywa?** - `label` powiązany `for`/`id`: klik w etykietę fokusuje pole, czytnik ekranu odczyta nazwę. Pole bez etykiety to pytanie, którego nie słychać.
4. **Kto pilnuje reguł?** - `required`, `min`/`max`, `minlength`, `pattern` (+ `title` z podpowiedzią). Walidacja HTML5 działa bez ani linijki JavaScriptu - JS przyjdzie na 0104.

I koperta na koniec: `form` z `action` (adresat rozmowy) i `method` (sposób wysyłki). Co serwer robi z wysłanymi danymi - to backend, patrz mapa „poza zakresem" niżej.

## Zanim zaczniesz - projekt i obrazy

1. Utwórz katalog projektu, np. `fanpage`, otwórz w VS Code, utwórz w nim `index.html`.
2. Jeśli nie skończyłeś/aś live codingu - dokończ go najpierw: „ściana divów" czeka w [index.html](index.html) obok tej instrukcji (skopiuj go do swojego katalogu zajęć i pracuj dalej), a finalną wersję prześle prowadzący.
3. **Obrazy do galerii** - przygotuj 3–5 plików w katalogu `obrazy/` obok `index.html`; wtedy w `src` wpisujesz **ścieżkę względną**, np. `obrazy/koncert.jpg`. Skąd wziąć zdjęcia? Po kolei:
   - **własne albo z oficjalnych profili Twojego tematu** - najlepsze, bo autorskie,
   - [unsplash.com](https://unsplash.com) - darmowe zdjęcia dobrej jakości: wpisz temat fanpage'a w wyszukiwarkę („concert", „esports", „guitar"…), pobierz 2–3 pliki, ściśnij je w [TinyPNG](https://tinypng.com/) i wrzuć do `obrazy/`. Zrób to **szybko** (max 5 minut) - doskonałe zdjęcia dopiejesz na 0103, dziś liczy się szkielet. Licencja Unsplash pozwala używać zdjęć za darmo, nawet komercyjnie, bez podawania autora,
   - nie chcesz pobierać? obrazki poglądowe: `https://placehold.co/600x400?text=Opis` albo `https://picsum.photos/seed/twoj-temat/600/400` - spójrz, co się wyświetliło, i **właśnie to opisz w `alt`**.

Podgląd: prawy przycisk na `index.html` → **Open with Live Server**; po każdej zmianie Ctrl+S (Cmd+S).

## Ściąga: typy pola `<input>` - które do czego

| Typ | Co robi / kiedy użyć | Co sam pilnuje przeglądarka |
|---|---|---|
| `text` | krótki tekst: imię, nazwa | nic - sam dodajesz `required`, `minlength` |
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

## Wariant A (podstawowy) - szkielet fanpage'u

Zbuduj kompletną stronę (sam szkielet - bez CSS, wygląd przyjdzie na 0103):

- [ ] szkielet dokumentu z 0101: `<!DOCTYPE html>`, `html lang="pl"`, `head` z `meta charset`, `viewport` i `title`,
- [ ] **`header`**: `h1` z nazwą tematu + jedno zdanie-hasło w `p`,
- [ ] **`nav`**: lista `ul` z 3–5 linkami do sekcji strony (`href="#id"` - sekcje muszą mieć te `id`),
- [ ] **`main`** z co najmniej **dwoma sekcjami**: „O …" (2–3 akapity `p` + lista `ul` lub `ol`) i **galeria**,
- [ ] galeria: **minimum 3 obrazy** `img`, każdy z `alt` opisującym, co widać, i z `width`/`height` (podpisane obrazy? bonus: `figure` + `figcaption`),
- [ ] **`footer`**: info, że to fanpage szkolny + link zewnętrzny do oficjalnej strony tematu (`target="_blank"` + `rel="noopener"`),
- [ ] **formularz zapisu** w osobnej sekcji: imię (`type="text"`, `required`), e-mail (`type="email"`, `required`), zgoda (`checkbox`, `required`), przycisk `button` - każde pole z `label` powiązanym `for`/`id`.

Sprawdź przed oddaniem: linki w `nav` skaczą do sekcji; wszystkie obrazy się wyświetlają; wysłanie pustego formularza blokuje przeglądarka.

## Wariant B (rozszerzający) - dla tych, którzy skończyli A

- [ ] **tabela danych** związana z tematem (np. dyskografia, wyniki/statystyki gracza, wymagania gry): `table` + `caption` + `thead` z `th` + `tbody` z `td`, minimum 3 wiersze danych,
- [ ] rozszerz formularz: **`select`** (np. „skąd znasz…") i **`radio` w `fieldset` z `legend`** (np. wybór jednej opcji) + po jednym polu `number` (z `min`/`max`) i `date`,
- [ ] **multimedia**: wstaw `iframe` z filmem powiązanym z tematem (pamiętaj o `title` ramki!) albo `audio`/`video` z `controls`.

Sprawdź przed oddaniem: tabela ma nagłówki `th` i tytuł `caption`; radio pozwala wybrać tylko jedną opcję; walidacja pól `number`/`date` działa.

## Wariant C ⭐ (gwiazdka, dla najszybszych) - fanpage bez myszy

1. Dokoncz/porządkuj **menu wewnętrzne**: każda sekcja ma `id`, `nav` linkuje do każdej z nich; na końcu każdej sekcji dodaj link „↑ wróć na górę" prowadzący do `#` nagłówka strony.
2. **Odłóż mysz.** Kliknij pasek adresu, a potem przechodź całą stronę samym **Tabem**: link po linku, pole po polu, aż do przycisku formularza. Odhaczaj: czy da się dotrzeć wszędzie? Czy kolejność ma sens? Czy widać, co jest zaznaczone (obwódka fokusu)?
3. Napraw znalezione problemy (np. link „czytaj dalej" - czy poza kontekstem wiadomo, dokąd prowadzi?).
4. **Dla bohaterów:** dodaj na samej górze strony link „Przejdź do treści" prowadzący do `main` (`id="tresc"`) - pierwszy prawdziwy trik dostępności, zanim w ogóle poznasz ARIA.

## Checklista dostępności (a11y) - samokontrola fanpage'a

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

1. **Dokończ fanpage** (wariant A; jeśli zdążyłeś/aś - dopracuj B) i przelicz go przez checklistę a11y wyżej - każdą odhaczoną pozycję zostaw w kodzie świadomie.
2. **Detektyw dostępności**: znajdź w internecie stronę z oczywistym błędem dostępności (brak `alt` przy obrazkach, „ściana divów", nagłówki pomieszane). Zapisz **adres strony** i **co jest nie tak** - pierwsze znaleziska omówimy na 0103.
3. **Przygotuj się do kartkówki** - zakres niżej.

**Nie kasuj projektu!** Na 0103 twój fanpage dostanie kolory, fonty i układ (flexbox), a na 0104 go opublikujemy. Trzymaj katalog `fanpage/` z obrazami w jednym kawałku.

## Kartkówka na 0103 - dokładny zakres

Na następnym spotkaniu (**0103 - CSS3: stylowanie i responsywność**) zajęcia zaczną się **10-minutową kartkówką** z dzisiejszego materiału:

- **semantyka**: czym się różni `article` od `section`, po co `nav`/`header`/`footer`, kiedy `div` wystarczy,
- **typy `input`**: dobierz typ do danych (e-mail, liczba, data, jedna opcja z wielu, zgoda),
- **formularze i walidacja HTML5**: `label` + `for`/`id`, `required`, `pattern`, `min`/`max`,
- **tabele**: `th` vs `td`, `caption`, `thead`/`tbody`,
- **a11y**: `alt`, kolejność nagłówków, nawigacja Tabem.

Będą pytania zamknięte (A–D, jak na egzaminie INF.03) i krótkie otwarte - podobnie jak dzisiaj.

## Zakres w pigułce: musisz umieć · warto wiedzieć · poza zakresem

Nie wszystko z dzisiejszych zajęć jest równie wymagające - i dobrze, że to wiesz. Ta mapa mówi wprost, co jest fundamentem (sprawdzi Cię kartkówka na 0103, sprawdzian semestralny i egzamin INF.03), co wystarczy **rozumieć i umieć nazwać**, a co dziś świadomie pomijamy. Zasada kursu: **wiedzieć, czego się jeszcze nie wie, to połowa drogi**.

### Musisz umieć - sam, bez podglądu

- **Semantyczny szkielet**: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer` - umieć dobrać właściwy znacznik i obronić wybór („dlaczego tu `article`, a nie `div`?"),
- **tekst i listy**: dokładnie jeden `h1` i nagłówki po kolei; `strong` vs `em`; `ul`/`ol`/`dl` - kiedy które (`ol` = kolejność ma znaczenie),
- **linki**: ścieżki względne vs bezwzględne; `target="_blank"` zawsze z `rel="noopener"`; zakotwiczenia `#id`; `mailto:`,
- **obrazy**: `img` z `alt` opisującym treść + `width`/`height`; dobór formatu prostą regułą: zdjęcie - JPG/WebP, przeźroczystość - PNG, logo/ikona - SVG,
- **tabela danych**: `table` + `caption` + `thead` z `th` + `tbody` z `td`,
- **formularz z walidacją HTML5**: każde pole z `label` powiązanym `for`/`id`; typy z ściągi wyżej; walidacja: `required`, `min`/`max`, `minlength`, `pattern`,
- **a11y w praktyce**: wszystkie 8 punktów checklisty wyżej - w tym `iframe` z `title` i przejście strony Tabem.

Kartkówka na 0103 sięgnie do środka tej listy (dokładny zakres - sekcja wyżej), a obrazy i linki sprawdzą Twój fanpage oraz sprawdzian semestralny (0104).

### Warto wiedzieć - umieć nazwać i wiedzieć, po co istnieje

- **WCAG**: 4 zasady - spostrzegalna, funkcjonalna, zrozumiała, solidna. Tyle wystarczy; kryteria sukcesu i poziomy A/AA/AAA zostawiamy na później,
- **ARIA**: zasada jest jedna - najpierw semantyczny HTML, ARIA tylko tam, gdzie HTML nie wystarcza,
- **czytniki ekranu**: VoiceOver (Mac) i NVDA (Windows) „czytają" strony na głos - dlatego kolejność nagłówków naprawdę robi robotę,
- **liczby, które uzasadniają a11y** (nie uczysz się ich na pamięć - odpowiadają na pytanie „po co?"): 1 na 6 ludzi na świecie, ok. 1,3 mld, żyje z niepełnosprawnością (WHO, 2023); unijne wymogi dostępności usług online (European Accessibility Act) obowiązują od 28 czerwca 2025; badanie WebAIM Million znajduje błędy dostępności na 95,9% z miliona sprawdzonych stron głównych,
- **tabnabbing**: atak przez kartę otwartą w `target="_blank"` - dlatego `rel="noopener"` wpisujemy zawsze; szczegóły ataku nie są Ci dziś potrzebne,
- **`type="color"` i `type="range"`**: 30 sekund zabawy - przetestuj sam w wariancie B,
- **`figure` + `figcaption`**: bonus do galerii, gdy chcesz podpisać obrazy,
- **link „Przejdź do treści"**: pierwszy prawdziwy trik dostępności, zanim w ogóle poznasz ARIA (wariant C),
- **`meta viewport`**: wpisujesz już teraz w każdym projekcie, dokładnie zrozumiesz go na 0103.

### Poza zakresem - mapa „wiem, czego nie wiem"

O tym dziś tylko wspominamy albo świadomie pomijamy - z planem, kiedy wróci:

- **CSS i responsywność** - całe stylowanie Twojego fanpage'a: **0103** (psst: w `index.html` z live codingu czeka na to jedna zakomentowana linijka),
- **JavaScript** - pierwszy skrypt, który „ożywi" stronę: **0104**,
- **backend formularza** - co dzieje się z danymi po kliknięciu „Wyślij": `action` i `method` tylko wskazują cel, dane przyjmuje i przetwarza serwer; osobny blok zajęć backendowych, a na INF.03 część praktyczna bywa z PHP + SQL,
- **publikacja i hosting** - jak sprawić, że strona dostanie prawdziwy adres w internecie: **0104**,
- **szczegóły WCAG i ARIA** - ponad dziś poznaną świadomość nie wracają (wyjątek: kontrast - zmierzysz go na 0103 w Lighthouse),
- **mechanika formatów graficznych** (kompresja stratna vs bezstratna, dlaczego WebP jest lżejszy) - wystarcza reguła doboru z listy „musisz umieć".

## Przydatne linki

- [MDN Web Docs - HTML po polsku](https://developer.mozilla.org/pl/docs/Web/HTML) - encyklopedia znaczników od ludzi pilnujących webowych standardów; tu sprawdzisz każdy element z dzisiejszych zajęć. Pełna lista wszystkich znaczników (po angielsku): [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).
- [HTML5 Periodic Table](https://madebymike.github.io/html5-periodic-table/) - wszystkie elementy HTML ułożone jak tablica Mendelejewa, pogrupowane według roli (sekcje, semantyka tekstu, media, formularze…). Kliknięcie „atomu" pokazuje krótki opis i link do MDN - dobra ściąga, gdy zastanawiasz się, jakie znaczniki semantyczne w ogóle istnieją.
- [Walidator W3C](https://validator.w3.org/) - wklej adres swojej strony (albo wgraj plik) i dostaniesz listę błędów HTML. Przepuść nim fanpage przed oddaniem.
- [WAVE - audyt dostępności](https://wave.webaim.org/) - pokazuje, gdzie brakuje `alt`, `label` albo porządku w nagłówkach. Fanpage na Live Serverze to localhost, więc zainstaluj [rozszerzenie WAVE do Chrome](https://wave.webaim.org/extension/) - działa też na stronach lokalnych.
- [web.dev - Learn HTML](https://web.dev/learn/html/) - darmowy kurs HTML od zespołu Google; po angielsku, ale prostym - idealny, gdy chcesz pójść dalej niż materiały z zajęć.
- [MDN - formularze krok po kroku](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms) - samouczek o `form`, typach `input` i walidacji (po angielsku; ściąga z typami pól jest wyżej w tym pliku).
- [regex101](https://regex101.com/) - do testowania wzorców do `pattern` (przyda się w wariancie B): piszesz wyrażenie i od razu widzisz, co łapie, a co nie.
- [TinyPNG](https://tinypng.com/) - kompresja JPG/PNG/WebP w przeglądarce, bez konta (do 20 plików naraz). Zdjęcie z Unsplash potrafi ważyć kilka MB - po TinyPNG to zwykle kilkaset KB, a galeria ładuje się natychmiast.
- [SVGOMG](https://jakearchibald.github.io/svgomg/) - czyści i odchudza pliki SVG (usuwa zbędne metadane, zaokrągla współrzędne); przyda się, gdy do fanpage'a wstawisz ikonę lub logotyp SVG.

---

> Zgubiłeś/aś pliki albo pracujesz na innym komputerze? Pakiet zawsze pobierzesz ze strony [daksamit.pl/zp/0102](https://daksamit.pl/zp/0102).

Masz pytania albo coś nie działa? Pytaj na bieżąco - na zajęciach lub mailowo. A jeśli wolisz najpierw spróbować samodzielnie: poproś AI z ściągi 0101 (ELI5: „wyjaśnij różnicę między article i section, jakbym miał 15 lat") i sprawdź odpowiedź w [MDN](https://developer.mozilla.org/pl/docs/Web/HTML).
