# Poradnik 0101 · Dlaczego web? Wstęp, przeglądarki i DevTools

0101 · Technologie webowe · ZST w Tarnowie × Akademia Tarnowska · kompletny przewodnik po pierwszym spotkaniu

To rozbudowana wersja materiałów z zajęć 0101: wszystko wyjaśnione od podstaw, z pełnym słowniczkiem pojęć na końcu. Szybka powtórka przed kartkówką? Sięgnij po [ściągę](0101-cheatsheet.md).

**Spis treści**

1. [Historia WWW i wersji HTML/CSS](#1-historia-www-i-wersji-htmlcss)
2. [Web w liczbach](#2-web-w-liczbach)
3. [Jak działa internet](#3-jak-działa-internet)
4. [Przeglądarki i silniki renderujące](#4-przeglądarki-i-silniki-renderujące)
5. [PWA - strona może być „natywna"](#5-pwa--strona-może-być-natywna)
6. [Chrome DevTools](#6-chrome-devtools)
7. [Warsztat: VS Code, Live Server, localhost](#7-warsztat-vs-code-live-server-localhost)
8. [AI jako Twój tutor](#8-ai-jako-twój-tutor)
9. [Twoja pierwsza strona HTML](#9-twoja-pierwsza-strona-html)
10. [Słowniczek pojęć A–Z](#10-słowniczek-pojęć-a--z)
11. [Powtórka przed kartkówką](#11-powtórka-przed-kartkówką)

---

## 1. Historia WWW i wersji HTML/CSS

### Skąd się wzięło WWW

W **1989 roku** brytyjski fizyk **Tim Berners-Lee**, pracujący w europejskim ośrodku badawczym **CERN** (koło Genewy), zaproponował system łączenia dokumentów naukowych linkami - tak żeby naukowcy mogli przeskakiwać między publikacjami jednym kliknięciem. Ten system nazwał **WWW** (World Wide Web, „sieć ogólnoświatowa"). Dlatego mówi się o „hypertekście": strona to tekst z **hiperłączami** - linkami do innych stron.

W **1991 roku** powstała **pierwsza strona internetowa** w historii. Zadziwiające: **nadal działa** - otwórz `http://info.cern.ch/hypertext/WWW/TheProject.html`. Zbudowana była z czystego HTML: sam tekst i linki, **zero CSS, zero grafiki, zero JavaScriptu**. Kilka prostych znaczników, a strona działa bez przerwy ponad 30 lat - to siła otwartych standardów. Dokładnie ten sam fundament (nagłówki, akapity, linki) użyłeś na zajęciach przy swojej pierwszej stronie.

### Wersje HTML - poziomy w tej samej grze

| Rok | Wersja | Dlaczego ważna |
|---|---|---|
| 1991 | pierwsza wersja HTML | kilkanaście znaczników, autor: Tim Berners-Lee |
| 1995 | HTML 2.0 | pierwszy wspólny standard dla przeglądarek |
| 1997 | HTML 4.01 | standard na całe lata - większość jego znaczników poznasz w kursie |
| 2014 | **HTML5** | rekomendacja W3C (prace od 2004 r. w grupie WHATWG) |

**HTML5** (rok 2014) nie wywrócił fundamentów - dodał nowe możliwości na górze, jak nowy poziom w grze:

- **znaczniki semantyczne**: `header`, `nav`, `footer` i inne, które mówią przeglądarce (i wyszukiwarkom), *co znaczy* dany fragment strony - poznasz je na 0102,
- **audio i wideo bez wtyczek** (kiedyś potrzebny był Flash - dziś nie),
- **formularze z wbudowaną walidacją**,
- **`canvas`** - „płótno" do rysowania i animacji w JavaScripcie.

### Wersje CSS - od szarego internetu do CSS3

W **1994 roku** Håkon Wium Lie zaproponował **CSS** - pomysł kluczowy dla całego webu: **oddzielenie treści (HTML) od wyglądu (CSS)**. Przed CSS wygląd „wklejano" w sam HTML - dziś nikt tak nie robi.

- **1996 - CSS 1**: kolory, czcionki, marginesy.
- **1998 - CSS 2**: pozycjonowanie elementów.
- **CSS3** (rozwijany modułowo od ok. 1999 r.): to **nie jedna wersja, lecz zestaw niezależnych modułów**, dodawanych do przeglądarek na bieżąco. Stąd pochodzą cienie i zaokrąglenia, **flexbox i grid**, animacje oraz **media queries** (responsywność - strona dopasowuje się do telefonu). Zobaczysz to na 0103.

### Wehikuł czasu: Wayback Machine

**Wayback Machine** (`web.archive.org`) to darmowe archiwum stron prowadzone przez Internet Archive od **1996 roku**. Wpisujesz adres - oglądasz, jak strona wyglądała lata temu. Ponad **800 mld zapisanych zrzutów stron** (Internet Archive, 2024). Spróbuj: wpisz adres strony szkoły i otwórz najstarszy zapis. Różnica między nim a dzisiejszą wersją to w dużej mierze zasługa CSS3 (i mody).

## 2. Web w liczbach

Każda z tych liczb ma źródło i rok - tak zawsze podawaj dane, a nigdy nie powołuj się na „gdzieś słyszałem".

| Liczba | Co oznacza | Źródło |
|---|---|---|
| JavaScript - najczęściej używany język **13. rok z rzędu** (~66% respondentów; 49 000+ odpowiedzi ze 177 krajów) | technologia, której się uczysz, jest nr 1 na świecie | Stack Overflow Developer Survey 2025 |
| JS działa po stronie klienta na **98,9% stron internetowych** | prawie cały interaktywny web stoi na JS | W3Techs, 2026 |
| ponad **1,2 mld stron** (w 2000 r. tylko 17 mln; aktywnych ok. 15%) | rynek ogromny i wciąż rośnie | Internet Live Stats, 2026 |
| **Chrome ~70–72%** udziału w rynku przeglądarek | testuj przede wszystkim tam, gdzie są użytkownicy | StatCounter, 2025 |
| **84% programistów** używa lub planuje używać narzędzi AI do kodowania | AI to standardowe narzędzie pracy, nie sztuczka | Stack Overflow Developer Survey 2025 |

**Co z tego wynika dla Ciebie:** HTML + CSS + JavaScript to **trzon pracy frontend developera** (ten, kto buduje to, co widać w przeglądarce). Dodaj backend (serwery, bazy danych) i masz **fullstack developera**. Na kursie poznasz te trzy języki od zera - bez frameworków i build-toolów, bo najpierw fundamenty (dokładnie tak samo zaczynają nasi studenci na Akademii Tarnowskiej - i wracają do nich nawet na ostatnim semestrze).

## 3. Jak działa internet

### Klient i serwer - restauracja w trzech rolach

- **klient** = Twoja przeglądarka (Chrome, Firefox, Safari…),
- **serwer** = komputer gdzieś na świecie, który **trzyma pliki strony** (HTML, CSS, JS, obrazki) i rozsyła je na zamówienie,
- **HTTP** = język, w którym klient i serwer się dogadują.

Analogia restauracji: **Ty zamawiasz (klient) → kelner nosi zamówienia (HTTP) → kuchnia gotuje (serwer)**. Kiedy wpisujesz adres w przeglądarce:

1. przeglądarka pyta DNS o adres serwera,
2. wysyła do serwera **żądanie HTTP** („poproszę stronę `index.html`"),
3. serwer odsyła **odpowiedź**: pliki HTML, CSS, JS i obrazki,
4. przeglądarka **renderuje** z nich stronę - maluje ją piksel po pikselu na ekranie.

Ważne: strona **nie „jest" w Twoim komputerze** - przeglądarka ją pobiera i rysuje za każdym razem, gdy wchodzisz na adres.

### DNS - książka telefoniczna internetu

Ludzie pamiętają nazwy (`zst.tarnow.pl`), komputery - numery (adresy IP, np. `93.184.216.34`). **DNS** (Domain Name System) tłumaczy jedne na drugie: pytasz DNS, jaki IP ma `zst.tarnow.pl`, dostajesz odpowiedź i dopiero wtedy przeglądarka łączy się z serwerem.

### HTTP i HTTPS - język żądań i odpowiedzi

**HTTP** (HyperText Transfer Protocol) to zestaw zasad rozmowy klient–serwer: żądanie → odpowiedź. **HTTPS** to ta sama rozmowa, ale **szyfrowana** - nikt po drodze (np. operator sieci Wi-Fi) nie odczyta, co przesyłasz. Stąd **kłódka** przy adresie. Strony bez kłódki przeglądarka dziś oznacza jako „niezabezpieczone".

### URL - adres rozbity na części

URL (Uniform Resource Locator) to adres strony, np.:

```text
https://www.przyklad.pl/oferta/cennik.html
└─┬─┘   └──────┬──────┘ └───────┬──────┘
schemat       host             ścieżka
```

- **schemat** - `https://`: jaką „ustalonym językiem" rozmawiamy,
- **host** - nazwa serwera (przed DNS-em to tylko etykieta; DNS zamieni ją na IP),
- **ścieżka** - konkretny plik/katalog na serwerze.

### CDN i renderowanie

- **CDN** (Content Delivery Network) - sieć serwerów z kopiami plików strony rozsianych po świecie; pliki lecą do Ciebie **z najbliższego węzła**, więc strona ładuje się szybciej.
- **renderowanie** - przeglądarka czyta HTML (szkielet i treść), CSS (wygląd) i JS (zachowanie) i maluje stronę na ekranie. Różne przeglądarki mogą ten sam kod renderować odrobinę inaczej (o tym niżej).

## 4. Przeglądarki i silniki renderujące

**Przeglądarka** to program, który pobiera pliki strony i renderuje ją na ekranie. Udziały rynkowe: **Chrome ~70–72%** (rekord w historii pomiarów; StatCounter, 2025), dalej Safari, Edge i Firefox - daleko w tyle.

Pod maską każdą przeglądarkę napędza **silnik renderujący** - część, która zamienia kod w to, co widzisz:

| Silnik | Przeglądarki |
|---|---|
| **Blink** | Chrome, Edge |
| **WebKit** | Safari |
| **Gecko** | Firefox |

Różny silnik może oznaczać, że ta sama strona **wygląda lub działa trochę inaczej** w innej przeglądarce - jak dwa drukarki drukujący ten sam plik odrobinę inaczej. Dlatego w branży testuje się stronę na kilku przeglądarkach: **„u mnie działa" to za mało**. DevTools masz w każdej z nich; na zajęciach pracujemy na Chrome.

## 5. PWA - strona może być „natywna"

**PWA** (Progressive Web App) to zwykła strona internetowa z „supermocami" aplikacji:

- **instalujesz ją z paska adresu przeglądarki** - bez sklepu z aplikacjami,
- działa **offline** (o tym więcej na 0203),
- potrafi wysyłać **powiadomienia**.

Przykłady: **Photopea** (`photopea.com`) - „Photoshop" działający w całości w przeglądarce; **Starbucks** i **Twitter/X Lite** - PWA zaprojektowane też pod słabe łącza i tanie telefony. Wniosek: granica między „stroną" a „aplikacją" praktycznie zniknęła - a Ty piszesz w technologiach, które stoją za jedną i drugą.

## 6. Chrome DevTools

**Chrome DevTools** to wbudowany, darmowy zestaw narzędzi webdevelopera. Otwierasz go na **dowolnej stronie, także cudzej** - i możesz ją modyfikować. Nic nie instalujesz, nic nie psujesz: **zmiany żyją tylko w Twojej przeglądarce**.

Otwarcie: **F12** lub **Ctrl+Shift+I** (macOS: **Cmd+Option+I**), albo menu ⋮ → Więcej narzędzi → Narzędzia deweloperskie.

### Elements - podejrz i edytuj każdą stronę

1. Otwórz DevTools (F12) na wybranej stronie.
2. Kliknij ikonę strzałki w kwadracie (lub **Ctrl+Shift+C**) i wskaż dowolny element na stronie - podświetli się w drzewie HTML.
3. Kliknij dwukrotnie tekst w panelu → edytujesz go **na żywo**.
4. W zakładce **Styles** po prawej zmień np. `color: red` - efekt widać natychmiast.
5. **F5 (odświeżenie) przywraca oryginał** - dlatego jest to bezpieczne.

To najlepszy sposób nauki: widzisz, z czego zbudowane są strony, które lubisz.

### Console - miejsce, gdzie strona „mówi"

Console pokazuje komunikaty strony i **przyjmuje Twoje polecenia**. Spróbuj po kolei:

```js
2 + 2
document.title          // przeglądarka pokaże tytuł strony
document.title = "Zajęcia 0101"   // a teraz go zmień - spójrz na kartę przeglądarki
```

Na kolejnych zajęciach Console stanie się Twoim podstawowym narzędziem debugowania.

### Device toolbar - telefon bez telefonu

**Ctrl+Shift+M** włącza podgląd strony w wymiarach telefonu lub tabletu. Przeciągaj krawędź i patrz, jak strona się przestawia (o ile jest responsywna). Szybki test bez sięgania po komórkę.

## 7. Warsztat: VS Code, Live Server, localhost

- **VS Code** - darmowy edytor kodu od Microsoftu, standard w branży (i narzędzie, na którym pracują nasi studenci na Akademii Tarnowskiej).
- **Live Server** - rozszerzenie VS Code: mały **serwer HTTP działający na Twoim komputerze**. Po każdym zapisie pliku (Ctrl+S) strona odświeża się w przeglądarce **sama**.
- Struktura projektu: katalog (np. `moja-strona`) + plik **`index.html`** - to strona startowa, którą serwer podaje pod samym adresem katalogu.

### Trzy adresy, które musisz rozumieć

| Adres | Co to |
|---|---|
| `file:///Users/jan/moja-strona/index.html` | plik otwarty **bez serwera** (dwuklik) - dziś zadziała, ale ma ograniczenia (np. niektóre rzeczy JS nie działają) |
| `http://127.0.0.1:5500` | strona serwowana przez **Live Server**; `127.0.0.1` = **localhost** = „ten komputer" - Twój laptop jest jednocześnie klientem i serwerem |
| `https://www.przyklad.pl` | prawdziwy serwer w internecie |

Bez instalacji cokolwiek: **StackBlitz** (`stackblitz.com`) lub **CodeSandbox** (`codesandbox.io`) - edytor z podglądem strony prosto w przeglądarce.

## 8. AI jako Twój tutor

AI (np. asystent w przeglądarce) świetnie sprawdza się jako **korepetytor dostępny 24/7** - ale dostajesz to, co konkretnie zamówisz, jak u dobrego wykonawcy:

- prompt „na lenia": *„utwórz mi stronę internetową wizytówkę i daj linka"* - wynik losowy,
- prompt ekspercki: *„zaprojektuj stronę-wizytówkę zgodnie ze standardami, z a11y, SEO, systemem kontroli wersji Git, deploymentem na Netlify oraz najnowszym Astro.js"* - wynik konkretny.

Żeby tak zamawiać, musisz znać fundamenty - a11y, SEO, Git i deployment poznasz właśnie w tym kursie. Techniki nauki z AI: **ELI5** („wyjaśnij, jakbym miał 5 lat"), rozwinięcie tematu, wyjaśnianie kodu linia po linii, pytania kontrolne z oceną, „znajdź błąd - bez gotowca". Gotowe prompty do skopiowania są w [mini-śnie AI jako tutor](ai-jako-tutor-sciega.md).

**Trzy zasady uczciwego użycia:**

1. **AI się myli** - każdy fakt i kod zweryfikuj (dokumentacja, np. MDN Web Docs; prowadzący).
2. **Kartkówki, sprawdziany i egzamin piszemy bez AI** - bez wyjątków.
3. **Używaj do zrozumienia, nie do kopiowania** - wklejając gotowiec, którego nie rozumiesz, nie uczysz się niczego.

## 9. Twoja pierwsza strona HTML

Szkielet HTML5 znak po znaku (dokładnie ten sam powstaje w live codingu; finalną wersję pliku prześle prowadzący):

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kim jestem</title>
</head>
<body>
  <h1>Cześć, jestem Jan</h1>
  <p>Uczę się w 4. klasie technikum ZST w Tarnowie.</p>
  <ul>
    <li>piłka nożna</li>
    <li>gry komputerowe</li>
    <li>programowanie</li>
  </ul>
  <a href="https://akademia.tarnowska.pl">Strona, którą polecam</a>
  <img src="ja.jpg" alt="Moje zdjęcie">
</body>
</html>
```

Co robi każdy element:

- **`<!DOCTYPE html>`** - deklaracja: „ten dokument to HTML5". Bez niej przeglądarka przełącza się w stary tryb renderowania.
- **`<html lang="pl">`** - korzeń całej strony; `lang="pl"` mówi przeglądarce, że treść jest po polsku (ważne m.in. dla czytników ekranu).
- **`<head>`** - informacje *o* stronie (niewidoczne na ekranie):
  - **`<meta charset="UTF-8">`** - kodowanie polskich znaków (bez tego „ą" zamienia się w „Ä„"),
  - **`<meta name="viewport" …>`** - informacja dla przeglądarki, jak skalować stronę na telefonie,
  - **`<title>`** - tekst na karcie przeglądarki (i wyniku Google).
- **`<body>`** - wszystko, co widać na stronie:
  - **`<h1>`** - nagłówek najwyższego poziomu (na stronie powinien być jeden),
  - **`<p>`** - akapit tekstu,
  - **`<ul>`** - lista nieuporządkowana; każdy punkt to **`<li>`**,
  - **`<a href="…">`** - link (ang. *anchor*); `href` to adres docelowy,
  - **`<img src="…" alt="…">`** - obrazek; `src` to ścieżka do pliku, `alt` - opis dla osób, które obrazka nie widzą (kluczowy dla dostępności, o czym na 0102).

Zapis pliku (Ctrl+S) → Live Server sam odświeża stronę. Sprawdź w praktyce: zmień tekst w `<h1>` i zapisz.

## 10. Słowniczek pojęć A–Z

- **a11y** - skrót od „accessibility" (dostępność; 11 liter między „a" i „y"). Strona dostępna da się używać też np. samą klawiaturą czy czytnikiem ekranu. Temat na 0102.
- **backend** - część aplikacji działająca na serwerze (logika, bazy danych); blok kolegi Gądka.
- **CDN** (Content Delivery Network) - sieć serwerów z kopiami plików strony po całym świecie; pliki lecą z najbliższego węzła, więc strona ładuje się szybciej.
- **CMS** - (poza zakresem 0101) system zarządzania treścią strony.
- **CSS** (Cascading Style Sheets) - język **wyglądu** strony: kolory, czcionki, układ. Propozycja: Håkon Wium Lie, 1994.
- **DevTools** - narzędzia deweloperskie wbudowane w przeglądarkę: Elements, Console, device toolbar i inne.
- **DNS** (Domain Name System) - „książka telefoniczna internetu": tłumaczy nazwy domen na adresy IP serwerów.
- **DOCTYPE** - pierwsza linia dokumentu HTML (`<!DOCTYPE html>`): deklaracja wersji HTML5.
- **DOM** - reprezentacja strony w pamięci przeglądarki jako drzewo elementów; temat na 0202.
- **frontend** - część strony działająca w przeglądarce użytkownika: HTML, CSS, JS.
- **fullstack** - developer łączący frontend i backend.
- **host** - nazwa serwera w adresie URL, np. `www.przyklad.pl`.
- **HTML** (HyperText Markup Language) - język **szkieletu i treści** strony; znaczniki opisują, co jest nagłówkiem, akapitem, listą, linkiem.
- **HTML5** - aktualna wersja HTML (rekomendacja W3C, 2014): znaczniki semantyczne, audio/wideo, walidacja formularzy, `canvas`.
- **HTTP / HTTPS** - protokół (język) żądań i odpowiedzi między klientem a serwerem; HTTPS = wersja szyfrowana (kłódka).
- **`index.html`** - nazwa pliku, który serwer podaje jako stronę startową katalogu.
- **IP (adres)** - numeryczny adres komputera w sieci, np. `93.184.216.34`.
- **JavaScript (JS)** - język **zachowania** strony: reakcje na kliknięcia, zmiany treści, pobieranie danych. Powstał w 1995 r.; działa na 98,9% stron (W3Techs, 2026).
- **klient** - program, który zamawia stronę; w praktyce: Twoja przeglądarka.
- **localhost / `127.0.0.1`** - „ten komputer": adres, pod którym Twój laptop jest jednocześnie klientem i serwerem (tak działa Live Server).
- **Live Server** - rozszerzenie VS Code: serwer HTTP na Twoim komputerze, strona odświeża się sama po zapisie.
- **MDN Web Docs** (`developer.mozilla.org`) - najlepsza darmowa dokumentacja HTML/CSS/JS; tam weryfikujesz odpowiedzi AI.
- **PWA** (Progressive Web App) - strona z możliwościami aplikacji: instalacja z przeglądarki, offline, powiadomienia (np. Photopea).
- **prompt** - polecenie wysyłane do AI; im precyzyjniejszy, tym lepsza odpowiedź.
- **ELI5** - „Explain Like I'm 5" - prośba do AI o wyjaśnienie, jakbym miał 5 lat.
- **renderowanie** - proces, w którym przeglądarka zamienia kod HTML/CSS/JS na stronę widoczną na ekranie.
- **serwer** - komputer (i działający na nim program), który trzyma pliki strony i odpowiada na żądania.
- **silnik renderujący** - część przeglądarki zamieniająca kod w obraz: Blink (Chrome, Edge), WebKit (Safari), Gecko (Firefox).
- **StackBlitz / CodeSandbox** - edytory kodu działające w przeglądarce (podgląd strony bez instalowania czegokolwiek).
- **URL** (Uniform Resource Locator) - adres zasobu w internecie: schemat + host + ścieżka.
- **viewport** - widoczny obszar strony na ekranie (meta viewport: instrukcja skalowania na telefonach).
- **VS Code** - darmowy edytor kodu od Microsoftu, standard w branży.
- **WWW** (World Wide Web) - system stron połączonych linkami; zaproponował Tim Berners-Lee (CERN, 1989).
- **W3C / WHATWG** - organizacje standaryzujące web: W3C wydaje rekomendacje (np. HTML5), WHATWG rozwija na co dzień standard HTML.

## 11. Powtórka przed kartkówką

**Zakres kartkówki na 0102 (z 0101):** historia WWW i wersji HTML/CSS · klient–serwer (DNS, HTTP(S), URL, `127.0.0.1`/localhost) · DevTools · szkielet HTML.

Sprawdź się - jeśli któreś pytanie sprawia trudność, wróć do odpowiedniego rozdziału (odpowiedzi znajdziesz w tym poradniku):

1. W którym roku i gdzie Tim Berners-Lee zaproponował WWW? Z czego była zbudowana pierwsza strona internetowa?
2. Czym różni się HTTP od HTTPS? Jaką rolę pełni DNS i dlaczego nazwano go „książką telefoniczną internetu"?
3. Rozbierz na części URL `https://www.zst.tarnow.pl/oferta/cennik.html` - jak nazywają się te trzy części?
4. Co oznacza adres `127.0.0.1`? Czym różni się otwarcie strony przez Live Server od dwukrotnego kliknięcia pliku?
5. Jak otworzyć DevTools i co robi panel Elements? Dlaczego zmiany zrobione w Elements znikają po odświeżeniu strony?
6. Napisz z pamięci (lub sprawdź i wyjaśnij) szkielet HTML5: `<!DOCTYPE html>`, `<html lang="pl">`, `<head>` z meta charset, viewport i title, `<body>` z nagłówkiem, akapitem i listą.

Kartkówka będzie zawierać min. 2 pytania zamknięte (jednokrotny wybór A–D) w formacie egzaminu INF.03 - poćwicz z [ściągi](0101-cheatsheet.md).

---

Następne spotkanie: **0102 - HTML5: semantyka, formularze, dostępność (a11y)**. Zaczyna się kartkówką z zakresu powyżej.
