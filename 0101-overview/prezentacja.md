# 0101 · Prezentacja - „Dlaczego web? Wstęp, przeglądarki i DevTools"

| | |
|---|---|
| **Spotkanie** | 0101 · semestr zimowy 2026 (realizacja: 07 X - grupa B, 21 X - grupa A) |
| **Slajdów** | 25 |
| **Czas prezentacji** | ok. 45 min łącznie z omówieniem i demami (slajdy 18–21 towarzyszą ćwiczeniom) |

Konwencja: przy slajdzie znacznik **[NA ŻYWO]** = przełącz się na przeglądarkę/VS Code i pokaż demo. Wszystkie statystyki występują wyłącznie ze źródłem i rokiem - nie doklejaj do nich żadnych innych liczb.

---

## Slajd 1 · Tytułowy

- **Technologie webowe - HTML5 · CSS3 · JavaScript**
- 0101: Dlaczego web? Wstęp, przeglądarki i DevTools
- mgr inż. Dominik Aksamit · Akademia Tarnowska × ZST w Tarnowie

## Slajd 2 · Ankieta na start

- **Weź kartkę z ankiety i odpowiedz pisemnie - 3 pytania:**
- 1. Czym dla Ciebie jest AI?
- 2. Jakie znasz sposoby na korzystanie z AI?
- 3. Wymień pojęcia, które kojarzą Ci się z AI
- to **nie test**: nie ma złych odpowiedzi, ankieta **nie jest oceniana**
- chcę tylko wiedzieć, od czego zaczynamy - wrócimy do tego w bloku o AI

## Slajd 3 · Zasady gry

- 135 minut: ankieta na start 10' + sekcja 50' + przerwa 15' + sekcja 35' + sekcja 25'
- od 0102 każde spotkanie zaczyna **kartkówką** (10 min, zakres: poprzednie spotkanie) - **z kartkówek zbierasz oceny cząstkowe, z nich wystawiam ocenę na koniec roku**
- 0104: **sprawdzian semestralny zamiast kartkówki** - pisemny, zakres 0101–0104, kartka i długopis
- pytania zadawaj w każdej chwili - im wcześniej, tym lepiej dla Ciebie
- dziś: pokazy, DevTools i Twoja pierwsza strona

## Slajd 4 · Mikro-historia WWW (5 minut, nie dłużej!)

- 1989 - Tim Berners-Lee proponuje WWW w CERN
- 1991 - pierwsza strona internetowa
- 1995 - powstaje JavaScript
- dziś - ponad 1,2 mld stron internetowych (Internet Live Stats, stan 2026)

**[NA ŻYWO]** Otwórz `http://info.cern.ch/hypertext/WWW/TheProject.html` - pierwsza strona w historii nadal działa.

## Slajd 5 · Pierwsza strona w historii - z czego była zbudowana

- pierwsza strona (1991) to **czysty HTML**: sam tekst i linki - zero CSS, zero grafiki, zero JavaScriptu
- HTML powstał, żeby naukowcy w CERN mogli **łączyć dokumenty linkami** - stąd „hypertext"
- kilkanaście prostych znaczników - a strona **nadal działa po ponad 30 latach**: to siła otwartych standardów
- dokładnie ten sam fundament (nagłówki, akapity, linki) użyjesz dziś przy swojej pierwszej stronie

**[NA ŻYWO]** Pokaż źródło pierwszej strony (Ctrl+U lub DevTools) - policzcie razem, ile różnych znaczników ma ta strona.

## Slajd 6 · Historia HTML - od znaczników do HTML5

- **1991** - pierwsza wersja HTML (Tim Berners-Lee, CERN): kilkanaście znaczników
- **1995** - HTML 2.0: pierwszy wspólny standard dla przeglądarek
- **1997** - HTML 4.01: standard na całe lata - większość jego znaczników poznasz w tym kursie
- **2014** - **HTML5** jako rekomendacja W3C (prace od 2004 r. w grupie WHATWG)
- HTML5 wnosi: znaczniki semantyczne (`header`, `nav`, `footer`), audio i wideo bez wtyczek, formularze z walidacją, `canvas`
- „5" w HTML5 to wersja języka - jak poziom w grze: fundamenty bez zmian, nowe możliwości na górze

## Slajd 7 · Historia CSS - od szarego internetu do CSS3

- **1994** - Håkon Wium Lie proponuje CSS: **oddzielenie treści (HTML) od wyglądu (CSS)**
- **1996** - CSS 1 (kolory, czcionki, marginesy) · **1998** - CSS 2 (pozycjonowanie)
- **CSS3** (rozwijany modułowo od ok. 1999 r.) - nie jedna wersja, tylko zestaw niezależnych modułów dodawanych do przeglądarek na bieżąco
- z CSS3 pochodzą: cienie i zaokrąglenia, **flexbox i grid**, animacje, media queries (responsywność)
- przed CSS wygląd „wklejano" w HTML - dziś nikt tak nie robi; na 0103 zobaczysz, jak sama zmiana CSS przemienia stronę

## Slajd 8 · Wayback Machine - wehikuł czasu internetu

- **Wayback Machine** (`web.archive.org`) - darmowe archiwum stron prowadzone przez Internet Archive od **1996** r.
- wpisujesz adres → oglądasz, jak strona wyglądała lata temu
- ponad **800 mld zapisanych zrzutów stron** (Internet Archive, stan 2024)
- użyteczne także „na poważnie": sprawdzenie, co faktycznie było na stronie w konkretnej dacie

**[NA ŻYWO]** Wpisz w Wayback Machine adres strony szkoły i otwórz najstarszy zapis - porównajcie z obecną wersją: tyle zmienił CSS3 (i mody).

## Slajd 9 · Web w liczbach

- JavaScript: najczęściej używany język wśród programistów **13. rok z rzędu** - ~66% respondentów, 49 000+ odpowiedzi (Stack Overflow Developer Survey **2025**)
- JavaScript działa po stronie klienta na **98,9% stron internetowych** (W3Techs, **2026**)
- ponad **1,2 mld stron** na świecie - w 2000 r. tylko 17 mln (Internet Live Stats, stan 2026)
- **Chrome ~70–72%** udziału w rynku przeglądarek (StatCounter, **2025**)
- **84% programistów** używa lub planuje używać narzędzi AI (Stack Overflow **2025**)

## Slajd 10 · Co z tego wynika dla Ciebie

- HTML + CSS + JavaScript = trzon pracy frontend developera
- fullstack developer = frontend + backend
- te trzy języki poznasz tu od zera: od pierwszej strony do interaktywnej aplikacji
- skupiamy się na fundamentach - zaawansowane aspekty frontendu (frameworki, build-tooly) pomijamy
- każde zajęcie trenuje Cię do egzaminu zawodowego INF.03

## Slajd 11 · PWA - strona może być „natywna"

- PWA (Progressive Web App) = strona internetowa z supermocami aplikacji
- instalujesz ją **z paska adresu przeglądarki** - bez sklepu z aplikacjami
- działa **offline** i potrafi wysyłać **powiadomienia**
- przykład: **Photopea** - „Photoshop" działający w całości w przeglądarce
- inne znane PWA: **Starbucks**, **Twitter/X Lite** (zaprojektowane też pod słabe łącza)

**[NA ŻYWO]** Otwórz `https://www.photopea.com`, kliknij ikonę instalacji w pasku adresu i uruchom PWA z systemu.

## Slajd 12 · Jak działa internet: klient i serwer

- klient = Twoja przeglądarka · serwer = komputer, który trzyma stronę
- jak w restauracji: Ty zamawiasz (klient), kelner nosi zamówienia (HTTP), kuchnia gotuje (serwer)
- przeglądarka wysyła żądanie → serwer odsyła pliki: HTML, CSS, JS, obrazki
- strona nie „jest" w Twoim komputerze - przeglądarka ją pobiera i **renderuje** na ekranie

**[NA ŻYWO]** Wejdź na `https://www.zst.tarnow.pl` i pokaż na pasku adresu: nazwę hosta i kłódkę HTTPS.

## Slajd 13 · DNS, HTTP(S) i URL - słowniczek

- **DNS** - „książka telefoniczna internetu": `zst.tarnow.pl` → adres IP serwera
- **HTTP** - język żądań i odpowiedzi; **HTTPS** = szyfrowana wersja (stąd kłódka)
- **URL** = adres złożony ze schematu, hosta i ścieżki: `https://` + `www.przyklad.pl` + `/oferta/cennik.html`
- **CDN** - sieć serwerów z kopiami plików strony po całym świecie; pliki lecą z najbliższego węzła, więc strona ładuje się szybciej

**[NA ŻYWO]** Rozbierz na części URL strony szkoły na forum klasy (schemat / host / ścieżka).

## Slajd 14 · Jak przeglądarka renderuje stronę

- **HTML** - szkielet i treść: co jest na stronie
- **CSS** - wygląd: jak strona wygląda
- **JavaScript** - zachowanie: co strona robi
- przeglądarka czyta pliki i maluje stronę piksel po pikselu
- różne przeglądarki mogą renderować ten sam kod odrobinę inaczej

## Slajd 15 · Przeglądarki i silniki

- Chrome **~70–72%** rynku (StatCounter, 2025); dalej Safari, Edge, Firefox
- silniki renderujące: **Blink** (Chrome, Edge) · **WebKit** (Safari) · **Gecko** (Firefox)
- różny silnik = ta sama strona może wyglądać lub działać trochę inaczej
- dlatego w branży testuje się na kilku przeglądarkach - „u mnie działa" to za mało
- DevTools masz w każdej z nich; my pracujemy na Chrome

## Slajd 16 · Mapa semestru - zimowy

- **0102 - HTML5**: semantyka, formularze, dostępność (a11y) · start kartkówką z 0101
- **0103 - CSS3**: stylowanie, flexbox, responsywność
- **0104 - Frontend w praktyce**: publikacja strony w internecie + dodatek o Tailwind CSS + **pierwszy JavaScript** - wstęp do interaktywnych stron
- **0104 zamyka semestr: sprawdzian semestralny zamiast kartkówki - zakres 0101–0104** (30 pytań zamkniętych A–D + pytania otwarte, kartka i długopis)
- te same technologie nasi studenci na Akademii Tarnowskiej wykorzystują na projektach - na końcu semestru pokażę, jak to wygląda od kuchni

## Slajd 17 · Chrome DevTools - supermoce w przeglądarce

- Chrome DevTools = wbudowany, darmowy zestaw narzędzi webdevelopera
- otwarcie: **F12** lub **Ctrl+Shift+I** (macOS: **Cmd+Option+I**) albo menu → Więcej narzędzi
- działa na każdej stronie - także na cudzej
- nic nie instalujesz, nic nie psujesz - zmiany są tylko lokalne

**[NA ŻYWO]** Otwórz DevTools na stronie szkoły i pokaż panel Elements.

## Slajd 18 · Elements - podejrzyj i edytuj każdą stronę

- widzisz dokładny kod HTML i CSS strony, którą oglądasz
- klikasz element na stronie → podświetla się w drzewie HTML
- edytujesz tekst i style **na żywo** - efekt widać natychmiast
- **F5 przywraca oryginał** - zmiany żyją tylko w Twojej przeglądarce

**[NA ŻYWO]** Zmień tekst nagłówka i kolor tekstu na zst.tarnow.pl, potem odśwież stronę.

## Slajd 19 · Console i device toolbar

- **Console** - miejsce, gdzie strona „mówi"; Ty też możesz w niej pisać (spróbuj: `2 + 2`)
- **device toolbar** - podgląd strony na telefonie lub tablecie bez telefonu
- przeciągnij szerokość i patrz, jak strona się przestawia
- idealne narzędzie do szybkiego testowania

**[NA ŻYWO]** Wpisz w Console `document.title` → potem `document.title = "Zajęcia 0101"`; włącz device toolbar (Ctrl+Shift+M).

## Slajd 20 · Warsztat: VS Code + Live Server

- **VS Code** - darmowy edytor kodu, standard w branży
- **Live Server** = mały **serwer HTTP na Twoim komputerze** - strona odświeża się sama po każdym zapisie
- **alternatywa bez instalacji: StackBlitz** (`stackblitz.com`) **lub CodeSandbox** (`codesandbox.io`) - edytor z podglądem strony w przeglądarce
- **`file://` (dwuklik na pliku) = bez serwera** - dziś też zadziała, ale ma ograniczenia
- **`127.0.0.1` = localhost = „ten komputer"** - Twój laptop jest jednocześnie klientem i serwerem
- struktura projektu: katalog (np. `moja-strona`) + plik **`index.html`** - strona startowa katalogu

**[NA ŻYWO]** Utwórz katalog `moja-strona` i plik `index.html`; pokaż oba adresy - najpierw dwuklik na pliku (`file:///…`), potem „Open with Live Server" (`http://127.0.0.1:5500`); zwróć uwagę klasy na początek adresu w pasku.

## Slajd 21 · AI jako Twój tutor - porównanie promptów

- prompt „na lenia": *„utwórz mi stronę internetową wizytówkę i daj linka"*
- prompt ekspercki: *„zaprojektuj stronę-wizytówkę zgodnie ze standardami, z a11y, SEO, systemem kontroli wersji Git, deploymentem na Netlify oraz najnowszym Astro.js"*
- różnica: **dostajesz to, co konkretnie zamówisz** - jak u dobrego wykonawcy
- żeby tak zamawiać, musisz znać fundamenty - a11y, SEO, Git i deployment poznasz w tym kursie
- 84% programistów używa lub planuje używać narzędzi AI (Stack Overflow 2025) - AI to standardowe narzędzie pracy

## Slajd 22 · Jak uczyć się z AI - i zasady uczciwości

- metody: **ELI5** („wyjaśnij, jakbym miał 5 lat") · rozwinięcie tematu · „wyjaśnij ten kod linia po linii" · pytania kontrolne z oceną · „znajdź błąd w moim kodzie"
- dostajesz dziś **mini-ścięgę z 6 gotowymi promptami** do skopiowania
- zasada 1: **AI się myli** - każdy fakt i kod zweryfikuj (dokumentacja, MDN, prowadzący)
- zasada 2: **kartkówki, sprawdziany i egzamin bez AI**
- zasada 3: używaj AI **do zrozumienia, nie do kopiowania**

## Slajd 23 · Twoja pierwsza strona - piszemy razem

- szkielet HTML5: `<!DOCTYPE html>` → `<html lang="pl">` → `<head>` (meta charset, viewport, title) → `<body>`
- treść: nagłówek `h1`, akapity `p`, lista `ul`/`li`, link `a`, obrazek `img`
- prowadzący pisze na projektorze - **Ty piszesz u siebie**, krok w krok
- każdy zapis (Ctrl+S) = strona odświeża się sama w Live Server

**[NA ŻYWO - LIVE CODING]** Przejdź do VS Code i prowadź live coding według konspektu (etapy 1–5).

## Slajd 24 · Podsumowanie i zadanie domowe

- dziś wiesz: po co web, jak działa internet, co to DevTools, jak uczyć się z AI - i masz swoją pierwszą stronę
- zadanie domowe (30–40 min): dokończ stronę „Kim jestem" · podejrzyj w DevTools 2–3 ulubione strony · wypróbuj 2 prompty ze ściągi AI
- następne spotkanie: **0102 - HTML5: semantyka, formularze, dostępność (a11y)**
- **0102 zaczyna się kartkówką** - zakres: historia WWW i wersji HTML/CSS · klient–serwer (DNS, HTTP(S), URL, 127.0.0.1/localhost) · DevTools · szkielet HTML
- pamiętaj o mapie: 0103 - CSS3, 0104 - pierwszy JavaScript i **sprawdzian semestralny zamiast kartkówki** (zakres 0101–0104)
