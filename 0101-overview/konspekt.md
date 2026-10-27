# 0101 · Konspekt zajęć - „Dlaczego web? Wstęp, przeglądarki i DevTools"

| | |
|---|---|
| **Semestr** | zimowy 2026 - spotkanie 1 z 9 |
| **Realizacja** | 07 X 2026 (grupa B) · 21 X 2026 (grupa A) |
| **Czas** | 135 min = **ankieta zapoznawcza 10 (nieoceniana)** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 |
| **Prowadzący** | mgr inż. Dominik Aksamit - Akademia Tarnowska |
| **Wersja materiałów** | 1.0 |
| **Scenariusz bazowy** | [scenariusz.md](scenariusz.md) |
| **Następne spotkanie** | 0102 · HTML5 - fundamenty i semantyka; **zaczyna się kartkówką z 0101** |

**Materiały towarzyszące:**

- prezentacja: [prezentacja.md](prezentacja.md) (20 slajdów),
- pakiet dla ucznia: [0101/](../0101/README.md) - instrukcja ćwiczeń z planem spotkania (3 bloki), ściąga i poradnik,
- rozwiązania i klucze: [rozwiazania/](rozwiazania/README.md),
- ankieta zapoznawcza (rozdrukka, 1/uczniów, nieoceniana): [ankieta-zapoznawcza.md](ankieta-zapoznawcza.md),
- mini-ściąga „AI jako tutor" (rozdrukka, 1/uczniów): [ai-jako-tutor-sciega.md](../0101/ai-jako-tutor-sciega.md).

## Cele zajęć - po spotkaniu uczeń:

- wie, jak wyglądają zajęcia: 135 min, kartkówki od 0102 (oceny cząstkowe → ocena na koniec roku), sprawdzian semestralny na 0104 zamiast kartkówki,
- rozumie na zweryfikowanych liczbach, dlaczego technologie webowe warto znać,
- potrafi wyjaśnić w pigułce: klient–serwer, DNS, HTTP(S), URL, renderowanie strony,
- otwiera Chrome DevTools, edytuje HTML/CSS na żywo i wie, że zmiany są lokalne,
- ma przygotowany warsztat: VS Code + Live Server + katalog projektu z `index.html` (alternatywnie edytor online: StackBlitz lub CodeSandbox),
- zna sposoby uczciwej nauki z AI i dostaje mini-ścięgę z gotowymi promptami,
- napisał (razem z prowadzącym) swoją pierwszą stronę HTML5 i zaczął ćwiczenie „Kim jestem".

## Przygotowanie przed zajęciami

- [ ] Na komputerach uczniowskich i na maszynie prowadzącego: **Chrome** oraz **VS Code z rozszerzeniem Live Server**.
- [ ] Projektor sprawny, rozdzielczość czytelna z ostatniej ławki (powiększ czcionkę w VS Code i Chrome).
- [ ] Internet działa; przetestuj wcześniej: `https://www.zst.tarnow.pl`, `https://www.photopea.com`, `http://info.cern.ch/hypertext/WWW/TheProject.html`, `https://picsum.photos/600/400`, `https://stackblitz.com` (lub `https://codesandbox.io`).
- [ ] Rozdrukki mini-ściągi „AI jako tutor" - po 1 egzemplarzu na ucznia.
- [ ] Rozdrukki ankiety zapoznawczej - po 1 egzemplarzu na ucznia (nieoceniana).
- [ ] Otwarte karty na start: prezentacja, strona szkoły, photopea.com.
- [ ] Plan B bez internetu: obrazek do live codingu położony lokalnie (`obrazek.jpg` w katalogu projektu); demo PWA i info.cern.ch zamienione na zrzuty ekranu.

Oznaczenia w przebiegu: **[DEMO NA ŻYWO]** - pokazuje prowadzący, uczniowie patrzą; **[LIVE CODING]** - uczniowie piszą razem z prowadzącym u siebie; **[PRACA SAMODZIELNA]** - uczniowie pracują samodzielnie, prowadzący pomaga indywidualnie.

---

## Ankieta zapoznawcza (0:00–0:10, 10') - na starcie, przed Sekcją 1

**[PRACA SAMODZIELNA]** Rozdaj arkusze ankiety ([ankieta-zapoznawcza.md](ankieta-zapoznawcza.md)) - **nieoceniana**, pisemna, trzy pytania otwarte:

1. Czym dla Ciebie jest AI?
2. Jakie znasz sposoby na korzystanie z AI?
3. Wymień pojęcia, które kojarzą Ci się z AI.

Przebieg: rozdanie (1') → samodzielne odpowiedzi (7') → zbiór arkuszy (2'). Powiedz uczniom wprost: „to nie test - nie ma złych odpowiedzi i ankieta nie jest oceniana; chcę tylko wiedzieć, od czego zaczynamy". W trakcie przerwy przejrzyj odpowiedzi - skalibruj nimi głębokość bloku „AI jako tutor" w Sekcji 2 (grupa znająca pojęcia idzie szybciej, grupa od zera dostaje więcej podstaw).

## Sekcja 1 (0:10–1:00, 50 min) - start kursu, liczby, kontekst

### 0:10–0:15 (5') · Przedstawienie się i zasady zajęć

Budujemy relację, nie wykład. W punktach:

1. **Kim jestem** - mgr inż. Dominik Aksamit; ścieżka: studia → praca w IT → Akademia Tarnowska; po bloku frontendowym prowadzi też mgr inż. Tomasz Gądek (backend, inne materiały).
2. **Jak wyglądają zajęcia** - 135 min w trzech sekcjach z 15-minutową przerwą w środku; środa raz na 2 tygodnie wg harmonogramu (daty w README).
3. **Forma sprawdzania i ocenianie** - od 0102 każde spotkanie zaczyna się **kartkówką (10 min)** z zakresu poprzedniego; na **0104 pisemny sprawdzian semestralny zamiast kartkówki** (zakres 0101–0104, 30 pytań zamkniętych A–D + pytania otwarte, kartka i długopis, bez komputerów). **Z kartkówek i sprawdzianu wystawiam oceny cząstkowe, z których powstaje ocena na koniec roku** - powiedz to wyraźnie, mają usłyszeć zapowiedź już dziś (dzisiejsza ankieta jest wyjątkiem: nieoceniana).
4. **Kultura zajęć** - pytania w każdej chwili, „nie ma głupich pytań"; komputer służy do ćwiczeń, nie do własnych spraw w trakcie sekcji.

### 0:15–0:20 (5') · Mikro-historia WWW - maksymalnie 5 minut!

Ciekawostka, nie program zajęć. Na slajdzie 4 daty:

- **1989** - Tim Berners-Lee pisze w CERN propozycję systemu hipertekstowego (urodziło się WWW),
- **1991** - pierwsza strona internetowa,
- **1995** - powstaje JavaScript (ciekawostka: pierwszy prototyp powstał w ok. 10 dni),
- **dziś** - ponad **1,2 mld stron** (Internet Live Stats).

**[DEMO NA ŻYWO]** Otwórz `http://info.cern.ch/hypertext/WWW/TheProject.html` - pierwsza strona w historii nadal działa. Puenta: „strona ma ponad 30 lat i nadal działa - bo web był projektowany jako trwały, otwarty standard".

### 0:20–0:30 (10') · Dlaczego warto: web w liczbach

Slajd „Web w liczbach" - **każda liczba ze źródłem i rokiem**. Omawiasz po kolei, do każdej jedno zdanie „co to znaczy dla Ciebie":

| Liczba | Źródło | Co to znaczy dla ucznia |
|---|---|---|
| JavaScript - najczęściej używany język programistów **13. rok z rzędu**, ~66% respondentów (49 000+ odpowiedzi) | Stack Overflow Developer Survey **2025** | uczysz się języka nr 1 na świecie, nie niszy |
| JavaScript działa po stronie klienta na **98,9% stron** | W3Techs, **2026** | znajomość JS otwiera praktycznie cały web |
| ponad **1,2 mld stron** (w 2000 r. tylko 17 mln) | Internet Live Stats (stan 2026) | rynek rośnie od 30 lat i nie zwalnia |
| **Chrome ~70–72%** udziału w rynku przeglądarek | StatCounter, **2025** | dlatego warsztat budujemy na Chrome + DevTools |
| **84% programistów** używa lub planuje używać narzędzi AI | Stack Overflow Developer Survey **2025** | AI to narzędzie pracy - nauczymy się z niego korzystać uczciwie |

Zakończ kierunkowskazem zawodowym (jakościowo, bez wymyślonych liczb): HTML + CSS + JS to trzon pracy frontend developera; fullstack = frontend + backend; te trzy języki poznasz tu od zera, a każde zajęcie trenuje Cię do INF.03.

### 0:30–0:35 (5') · PWA - strona może być „natywna"

Trzy zdania teorii maksymalnie:

- PWA (Progressive Web App) = strona, która potrafi działać jak aplikacja: **instalacja z przeglądarki** (bez sklepu z aplikacjami), **offline**, **powiadomienia**,
- przykład: **Photopea** (`photopea.com`) - pełny edytor graficzny w stylu Photoshopa, który działa w przeglądarce i instaluje się jak aplikacja; inne znane PWA: **Starbucks**, **Twitter/X Lite** (powstały, by działać tanio i szybko na słabych łączach).

**[DEMO NA ŻYWO]** Otwórz `https://www.photopea.com` → zwróć uwagę, że to „Photoshop w przeglądarce" bez instalowania czegokolwiek → w pasku adresu kliknij ikonę instalacji → „Zainstaluj" → uruchom aplikację z pulpitu menu Start / Docka. Puenta: „to nadal zwykła strona - zrobiona z tych samych technologii, których będziemy się uczyć".

### 0:35–0:45 (10') · Jak działa internet w pigułce

Analogie z życia, zero głębi protokołów:

1. **Klient–serwer** - restauracja: ty (klient/przeglądarka) składasz zamówienie, kelner (HTTP) nosi zamówienia, kuchnia (serwer) przygotowuje danie (pliki HTML/CSS/JS). Strona nie „jest" w przeglądarce - przeglądarka ją **pobiera i renderuje** na Twoim ekranie.
2. **DNS** - „książka telefoniczna internetu": zapamiętujesz nazwę `zst.tarnow.pl`, DNS podaje numer (adres IP) serwera.
3. **HTTP(S)** - język żądań i odpowiedzi; **S** = szyfrowanie (kłódka przy adresie).
4. **URL** - rozłóż na części: `https://` (schemat) + `www.przyklad.pl` (host) + `/oferta/cennik.html` (ścieżka do pliku na serwerze).
5. **CDN** (bonus) - Content Delivery Network: sieć serwerów z kopiami plików strony rozsianych po świecie; pliki lecą z najbliższego węzła, więc strona ładuje się szybciej (Netflix, duże sklepy).
6. **Renderowanie** - przeglądarka czyta HTML (szkielet i treść), pobiera CSS (wygląd) i JS (zachowanie), po czym maluje stronę piksel po pikselu.

**[DEMO NA ŻYWO]** Na stronie szkoły pokaż w pasku adresu: kłódkę HTTPS, nazwę hosta. Opcjonalnie (dla dociekliwych): F12 → Network → F5 - widać listę pobieranych plików.

### 0:45–0:50 (5') · Przeglądarki i silniki

Krótki blok - szczegóły wracają na 0102, dziś tylko mapa świata przeglądarek:

- Udziały rynkowe: **Chrome ~70–72%** (StatCounter, 2025), dalej Safari, Edge, Firefox.
- Silniki renderujące: **Blink** (Chrome, Edge) · **WebKit** (Safari) · **Gecko** (Firefox).
- Dlaczego testujemy na kilku przeglądarkach: różne silniki mogą trochę inaczej zinterpretować ten sam kod - „u mnie działa" to za mało. DevTools masz w każdej; u nas standard: Chrome.

### 0:50–1:00 (10') · Mapa semestru + INF.03 + akcent Akademii Tarnowskiej

Slajd „Mapa semestru". Przeczytaj plan konkretnie:

- **0102 - HTML5**: semantyka, formularze, dostępność (a11y); zaczyna się kartkówką z dzisiejszego spotkania,
- **0103 - CSS3**: stylowanie, flexbox, responsywność,
- **0104 - Frontend w praktyce**: publikacja strony w internecie, dodatek „jak w branży" o Tailwind CSS, **pierwszy JavaScript** (wstęp do interaktywnych stron) - i **sprawdzian semestralny zamiast kartkówki** (pisemny: 30 pytań zamkniętych A–D + pytania otwarte, kartka i długopis, zakres 0101–0104),
- **semestr letni**: JavaScript na poważnie → DOM i zdarzenia → dane i API → projekt zespołowy → trening INF.03,
- **INF.03 w skrócie**: część pisemna - test 40 zadań zamkniętych (60 min, 40 pkt); część praktyczna - witryna HTML/CSS/JS + baza danych SQL (240 min, 100 pkt); próg 50% z każdej części. Szczegóły i trening na ostatnim spotkaniu semestru letniego.

**Akcent Akademii Tarnowskiej** (jedno zdanie, pierwsza osoba, bez reklamy):
„To samo, co będziecie robić na zajęciach, nasi studenci na Akademii Tarnowskiej robią na projektach i praktykach - na końcu semestru pokażę wam, jak to wygląda od kuchni."

---

## Przerwa (15 min) · 1:00–1:15

---

## Sekcja 2 (35 min) - warsztat: DevTools, narzędzia, AI jako tutor

### 1:15–1:20 (5') · Chrome DevTools - wprowadzenie **[DEMO NA ŻYWO]**

- Jak otworzyć: **F12** lub **Ctrl+Shift+I** (macOS: **Cmd+Option+I**) albo menu → Więcej narzędzi → Narzędzia deweloperskie.
- Pokaż panel **Elements**: kliknij ikonę strzałki/wskaźnika, najedź na nagłówek strony szkoły - podświetlenie na stronie ↔ węzeł w drzewie HTML.
- Na żywo zmień tekst nagłówka (dwuklik w Elements) i kolor tekstu (w panelu Styles dopisz np. `color: crimson;`) - efekt natychmiastowy.
- Kluczowe zdanie sekcji: **zmiany są tylko lokalne, w pamięci Twojej przeglądarki - F5 przywraca oryginał**. Nikt tego nie widzi, nic nie psujesz.

### 1:20–1:35 (15') · DevTools w praktyce **[PRACA SAMODZIELNA]**

Każdy uczeń na swoim komputerze, na dowolnej stronie (np. ulubiony serwis, sklep, strona szkoły):

1. Otwórz DevTools, znajdź w Elements główny nagłówek - zmień jego tekst (np. dodaj swoje imię).
2. W panelu Styles zmień kolor tekstu i tło wybranego elementu.
3. Ukryj wybrany element (w Elements: klawisz **H** na węźle lub odznacz wizualizację; alternatywnie dopisz `display: none;`).
4. Włącz **device toolbar** (Ctrl+Shift+M) - zobacz stronę jak na telefonie; przeciągnij szerokość.
5. W **Console** wpisz `2 + 2`, potem `document.title` - Console to miejsce, gdzie strona „mówi" (pełną naukę Console odkładamy na semestr letni).
6. Odśwież stronę (F5) i obejrzyj efekt „magii": wszystko wróciło do oryginału.

Prowadzący krąży, pomaga; szybcy niech pomogą sąsiadowi. Po ~12 minutach zbierz 2–3 wrażenia.

### 1:35–1:40 (5') · Warsztat: VS Code + Live Server **[DEMO NA ŻYWO - uczniowie powtarzają równolegle]**

Jeśli sala gotowa wcześniej, skróć do 2 minut. Kroki (każdy wykonuje u siebie):

1. Utwórz na dysku katalog projektu, np. `moja-strona`.
2. Otwórz go w VS Code (Plik → Otwórz folder).
3. Utwórz plik **`index.html`** - specjalna nazwa: strona startowa katalogu. Zapisz.
4. **Adres nr 1 - statycznie:** otwórz plik dwuklikiem w Eksploratorze/Finderze → pokaż uczniom adres `file:///…` → „przeglądarka czyta plik prosto z dysku: żadnego serwera, żadnego HTTP".
5. **Adres nr 2 - serwer deweloperski:** wróć do VS Code, prawy przycisk na pliku → **Open with Live Server** → pokaż adres `http://127.0.0.1:5500` → „to prawdziwy serwer HTTP; `127.0.0.1` (localhost) to specjalny adres oznaczający »ten komputer« - model klient–serwer z Sekcji 1 dzieje się na Twoim biurku: laptop jest jednocześnie klientem i serwerem". Pokaż auto-odświeżanie: dopisz cokolwiek w pliku, zapisz (Ctrl+S) - przeglądarka sama się odświeża.
6. **Adres nr 3 - serwer produkcyjny:** „to samo, co przed przerwą na photopea.com - tylko serwer stoi gdzie indziej; swoją stronę na prawdziwy serwer wrzucimy na 0104".
7. **Alternatywa bez instalowania czegokolwiek - edytor w przeglądarce:** pokaż krótko **StackBlitz** (`stackblitz.com`) lub **CodeSandbox** (`codesandbox.io`) - wystarczy kliknąć „New project" / „Create sandbox" → HTML+CSS+JS i kodzimy w przeglądarce, z podglądem i auto-odświeżaniem obok kodu. „To samo, co VS Code + Live Server, tylko w chmurze - użyteczne, gdy pracujesz na cudzym komputerze albo nie chcesz nic instalować".

Ściągawka dla prowadzącego - trzy adresy, jedna strona:

| Adres w pasku | Kto podaje pliki | Kiedy używamy |
|---|---|---|
| `file:///…` (dwuklik na pliku) | nikt - przeglądarka czyta plik prosto z dysku | awaryjnie; działa tylko dla prostych stron |
| `http://127.0.0.1:5500` (Live Server) | serwer HTTP na Twoim komputerze (localhost) | codzienna praca przy budowie strony - tak robimy na zajęciach |
| `https://…` (np. zst.tarnow.pl) | serwer produkcyjny w internecie | strona opublikowana dla świata (0104) |

Dlaczego od razu uczymy się Live Server, skoro dwuklik też działa: przez `file://` przeglądarka stosuje dodatkowe ograniczenia bezpieczeństwa - między innymi późniejsze pobieranie danych (`fetch`) nie zadziała. Dokładnie poznamy to na 0203; na dziś wystarczy świadomość różnicy.

Plan B: jeśli Live Server niedostępny, pracuj przez dwuklik (adres `file://…`) i odświeżaj ręcznie F5 - powiedz wówczas uczniom wprost, czym ten tryb różni się od serwera (tabela wyżej): dzisiejsza strona zadziała w obu trybach, ale to serwer deweloperski jest „prawdziwym internetem w miniaturze".

### 1:40–1:50 (10') · AI jako Twój tutor - prezentacja + dyskusja

Trzy podpunkty (slajdy „AI jako tutor"):

**(a) Dlaczego fundamenty czynią AI użytecznym** - porównanie promptów na slajdzie:

- prompt „na lenia": *„utwórz mi stronę internetową wizytówkę i daj linka"* → dostajesz przypadkowy, generyczny wynik,
- prompt ekspercki: *„zaprojektuj stronę-wizytówkę zgodnie ze standardami, z a11y, SEO, systemem kontroli wersji Git, deploymentem na Netlify oraz najnowszym Astro.js"* → dostajesz dokładnie to, co zamawiasz.

Puenta: **jakość wyniku zależy od precyzji zamówienia** - a tak zamówić możesz tylko wtedy, gdy znasz fundamenty (a11y, SEO, Git, deployment to słowa, które poznasz w tym kursie). Zacytuj: 84% programistów używa lub planuje używać narzędzi AI (Stack Overflow 2025) - AI to standard wyposażenia, nie oszukiwanie.

**(b) Jak się uczyć z AI** - wymień metody: ELI5 („wyjaśnij, jakbym miał 5 lat"), rozwinięcie tematu, dopytywanie o niezrozumiałe fragmenty, pytania kontrolne z oceną, „znajdź błąd w moim kodzie".

**(c) Zasady uczciwego użycia** - AI się myli (każdy fakt i kod zweryfikuj: MDN, dokumentacja, prowadzący); kartkówki, sprawdziany i egzamin piszemy **bez AI**; używaj do zrozumienia, nie do kopiowania.

**Rozdaj mini-ścięgę „AI jako tutor"** - 6 gotowych promptów do skopiowania; będzie użyta w zadaniu domowym.

---

## Sekcja 3 (25 min) - pierwsza strona: live coding i praca samodzielna

### 1:50–2:05 (15') · Live coding: pierwsza strona HTML **[LIVE CODING - uczniowie piszą razem z prowadzącym]**

Prowadzący pisze w VS Code, projektor działa, uczniowie powtarzają każdy krok u siebie; Live Server odświeża stronę po każdym zapisie. Skrypt krok po kroku - patrz sekcja **„Live coding - scenariusz krok po kroku"** poniżej. Etapy: szkielet → nagłówek i akapity → lista → link → obrazek.

Kompletne pliki: krok po kroku poniżej; finalny plik referencyjny: [rozwiazania/live-coding/index.html](rozwiazania/live-coding/index.html) (do wysłania uczniom, którzy nie nadążyli).

### 2:05–2:12 (7') · Ćwiczenie samodzielne „Kim jestem" **[PRACA SAMODZIELNA]**

Uczniowie zaczynają ćwiczenie A (strona „Kim jestem": nagłówek, akapity, lista, link), szybcy przechodzą do wariantu B (obrazek + sekcja „Moje cele") i C (modyfikacja ulubionej strony w DevTools, zrzut przed/po). Instrukcja: [0101/README.md](../0101/README.md). Prowadzący pomaga indywidualnie.

### 2:12–2:15 (3') · Domknięcie dnia

- Podsumowanie runda: „wymień jedną rzecz, którą dziś nauczyłeś/aś" - 3–4 ochotników.
- **Zadanie domowe** (30–40 min): dokończ „Kim jestem" · podejrzyj 2–3 ulubione strony w DevTools · wypróbuj 2 prompty ze ściągi AI (np. ELI5 na temat „jak działa DNS").
- **Zapowiedź 0102**: HTML5 - semantyka, formularze, dostępność (a11y). **Zakres kartkówki na 0102: historia WWW · klient–serwer (DNS, HTTP(S), URL, 127.0.0.1/localhost) · Chrome DevTools · szkielet HTML.**
- Przypomnienie mapy: 0103 - CSS3; **0104 - pierwszy JavaScript i sprawdzian semestralny zamiast kartkówki** (papierowy, zakres 0101–0104).

---

## Live coding - scenariusz krok po kroku

Każdy etap: powiedz → napisz → zapisz (Ctrl+S) → wszyscy patrzą na odświeżoną stronę w Live Server.

### Etap 1 - szkielet dokumentu (podstawa, zawsze od tego zaczynamy)

```html
<!DOCTYPE html>
<!-- lang="pl" mówi przeglądarce i czytnikom ekranu, w jakim języku jest strona -->
<html lang="pl">
<head>
  <!-- kodowanie znaków - bez tego polskie znaki mogą się wykrzaczyć -->
  <meta charset="UTF-8">
  <!-- viewport: strona dobrze wygląda też na telefonie -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- tytuł karty w przeglądarce (to nie jest nagłówek na stronie!) -->
  <title>Dlaczego web? - moja pierwsza strona</title>
</head>
<body>
  <!-- tu wpisujemy całą widoczną treść -->
</body>
</html>
```

Po zapisie: pusta strona, ale **tytuł karty** już się zmienił. Skomentuj: `head` = informacje O stronie, `body` = treść DLA użytkownika.

### Etap 2 - nagłówek główny i akapity (dopisz w `body`)

```html
<h1>Dlaczego web?</h1>

<p>
  Cześć! To pierwsza strona, którą napisałem samodzielnie na zajęciach
  „Zagadnienia programowania”. Powstaje w VS Code, a przeglądarkę mam
  obok dzięki rozszerzeniu Live Server.
</p>

<p>
  Dziś sprawdziliśmy, że JavaScript jest najczęściej używanym językiem
  programistycznym - po raz trzynasty z rzędu (Stack Overflow 2025).
  A strona internetowa to w sumie zwykły plik tekstowy.
</p>
```

Zwróć uwagę: enter w akapicie nie łamie linii - przeglądarka zbija białe znaki.

### Etap 3 - podsekcja z listą (dopisz niżej w `body`)

```html
<!-- h2 = nagłówek sekcji podrzędnej względem h1 -->
<h2>Czego nauczyłem się na 0101</h2>

<!-- lista nieuporządkowana: ul = kontener, li = element -->
<ul>
  <li>jak działa internet: klient, serwer, DNS, HTTP(S)</li>
  <li>jak podejrzeć i pozmieniać każdą stronę w Chrome DevTools</li>
  <li>jak napisać szkielet strony w HTML5</li>
</ul>
```

### Etap 4 - link (dopisz niżej w `body`)

```html
<h2>Link dnia</h2>

<p>
  <!-- href = dokąd prowadzi; target="_blank" otwiera w nowej karcie -->
  <a href="http://info.cern.ch/hypertext/WWW/TheProject.html" target="_blank" rel="noopener">
    Pierwsza strona w historii WWW (1991)
  </a>
  - nadal działa.
</p>
```

### Etap 5 - obrazek (dopisz na końcu `body`)

```html
<h2>Obrazek</h2>

<!-- src = skąd pobrać obrazek; alt = opis dla osób niewidomych i gdy obrazek się nie wczyta;
     width/height zapobiegają „skakaniu” strony przy wczytywaniu -->
<img
  src="https://picsum.photos/600/400"
  alt="Przykładowe zdjęcie wczytywane z zewnętrznego serwisu picsum.photos"
  width="600"
  height="400"
>
```

Jeśli brak internetu: użyj lokalnego pliku, np. `src="obrazek.jpg"` (plik w tym samym katalogu). Kliknij link z etapu 4 - działa.

Po etapie 5: 30 sekundy swobodnych modyfikacji (każdy zmienia teksty na swoje) - to już wstęp do ćwiczenia A.

---

## Notatki prowadzącego

- **Akcent Akademii Tarnowskiej** - dokładnie jedno zdanie w Sekcji 1 (skrypt wyżej). Zero tonu reklamy.
- **Przekaz o narzędziach** (jedno zdanie w bloku „AI jako tutor", 1:40–1:50 - najlepiej po pokazie porównania promptów): „W dzisiejszych czasach nie jest ważne, jak umiecie budować, ale szybko potraficie korzystać z narzędzi, które za nas pracę wykonują."
- **Statystyki** - używaj wyłącznie liczb z tabeli w Sekcji 1, zawsze ze źródłem i rokiem. Przed zajęciami odśwież dane u źródła (linki w [README.md](../README.md), sekcja „Technologie webowe w liczbach").
- **Tempo Sekcji 1** - historia WWW to ciekawostka na 5 minut, nie wykład; jeśli ściskasz czas, tnij opowieści, nie ćwiczenia.
- **DevTools na macOS** - skrót Cmd+Option+I; device toolbar: Cmd+Shift+M.
- **Uczniowie bez VS Code** - dwie drogi: (1) na dziś wystarczy Notatnik/dowolny edytor + otwieranie pliku w Chrome; wyjaśnij im wprost różnicę `file://` vs `http://127.0.0.1` (tabela w bloku warsztatu 1:35–1:40), (2) **StackBlitz** (`stackblitz.com`) lub **CodeSandbox** (`codesandbox.io`) - pełny edytor z podglądem w przeglądarce, zero instalacji, wystarczy konto Google/GitHub.
- **5 pytań w stylu INF.03** z tego spotkania (baza kartkówki na 0102): [rozwiazania/pytania-inf03-z-kluczem.md](rozwiazania/pytania-inf03-z-kluczem.md). Nie pokazuj ich uczniom na zajęciach.

## Checklista jakości (AGENTS.md)

- [x] Suma czasów = 135 min (ankieta 10 + 50 + 15 + 35 + 25), rozpiska co 5–10 min z oznaczonymi momentami live coding i pracy samodzielnej.
- [x] Ankieta zapoznawcza na starcie: nieoceniana, bez klucza (arkusz: [ankieta-zapoznawcza.md](ankieta-zapoznawcza.md)); podano zakres kartkówki na 0102.
- [x] Kod: domknięte znaczniki, poprawna struktura dokumentu, komentarze po polsku.
- [x] Ćwiczenia w wariantach A/B/C, każde z pełnym rozwiązaniem - rozwiązania wyłącznie w `rozwiazania/`.
- [x] Nawiązanie do INF.03 (mapa semestru) + 5 pytań egzaminacyjnych z kluczem w materiałach prowadzącego.
- [x] Jeden subtelny akcent Akademii Tarnowskiej (Sekcja 1, skrypt dosłowny).
- [x] Zadanie domowe (30–40 min) + zakres kartkówki na następne spotkanie.
- [x] Statystyki wyłącznie zweryfikowane, każda ze źródłem i rokiem.
