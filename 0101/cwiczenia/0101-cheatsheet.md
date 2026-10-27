# Ściąga 0101 · Dlaczego web? Przeglądarki i DevTools

0101 · Technologie webowe · ZST w Tarnowie × Akademia Tarnowska · do powtórki przed kartkówką na 0102

**Zakres kartkówki z 0101:** historia WWW i wersji HTML/CSS · klient–serwer (DNS, HTTP(S), URL, 127.0.0.1/localhost) · DevTools · szkielet HTML.

---

## 1. Historia w jednej tabeli

| Rok | Co się stało |
|---|---|
| **1989** | Tim Berners-Lee proponuje WWW w CERN |
| **1991** | pierwsza strona internetowa (działa do dziś: `http://info.cern.ch`) - czysty HTML, zero CSS i JS |
| **1994** | Håkon Wium Lie proponuje CSS - oddzielenie treści (HTML) od wyglądu (CSS) |
| **1995** | powstaje JavaScript; pierwszy wspólny standard HTML - HTML 2.0 |
| **1997** | HTML 4.01 - standard na lata, większość jego znaczników poznasz na kursie |
| **2014** | **HTML5** jako rekomendacja W3C (prace od 2004 w WHATWG) |

- **HTML5** wnosi: znaczniki semantyczne (`header`, `nav`, `footer`), audio/wideo bez wtyczek, walidację formularzy, `canvas`.
- **CSS3** to nie jedna wersja, tylko **zestaw niezależnych modułów** dodawanych do przeglądarek na bieżąco (flexbox, grid, animacje, media queries).

## 2. Jak działa internet w 6 hasłach

| Pojęcie | W jednym zdaniu |
|---|---|
| **klient** | Twoja przeglądarka - zamawia stronę |
| **serwer** | komputer, który trzyma stronę - „kuchnia" odsyłająca pliki |
| **DNS** | „książka telefoniczna internetu": `zst.tarnow.pl` → adres IP serwera |
| **HTTP / HTTPS** | język żądań i odpowiedzi; **S** = szyfrowanie (stąd kłódka) |
| **URL** | `https://` (schemat) + `www.przyklad.pl` (host) + `/oferta/cennik.html` (ścieżka) |
| **renderowanie** | przeglądarka pobiera HTML/CSS/JS i maluje stronę na ekranie |

Analogia restauracji: **Ty zamawiasz (klient) → kelner nosi zamówienia (HTTP) → kuchnia gotuje (serwer)**.

Rola trzech języków: **HTML = szkielet i treść · CSS = wygląd · JavaScript = zachowanie**.

## 3. Przeglądarki i silniki

- **Chrome ~70–72%** rynku (StatCounter, 2025); dalej Safari, Edge, Firefox.
- Silniki renderujące: **Blink** (Chrome, Edge) · **WebKit** (Safari) · **Gecko** (Firefox).
- Różny silnik = ta sama strona może wyglądać lub działać trochę inaczej → dlatego testuje się na kilku przeglądarkach. „U mnie działa" to za mało.

## 4. DevTools w 4 skrótach

Otwarcie: **F12** lub **Ctrl+Shift+I** (macOS: **Cmd+Option+I**) albo menu → Więcej narzędzi.

| Panel | Co robi |
|---|---|
| **Elements** | podgląd i **edycja HTML/CSS na żywo** (klik element → podświetla się w drzewie); **F5 przywraca oryginał** - zmiany żyją tylko u Ciebie |
| **Console** | miejsce, gdzie strona „mówi"; Ty też możesz pisać (np. `2 + 2`, `document.title = "Zajęcia"`) |
| **device toolbar** | podgląd strony na telefonie/tablecie (**Ctrl+Shift+M**) - bez telefonu |

## 5. Warsztat

- **VS Code** - darmowy edytor kodu, standard w branży; **Live Server** - mały serwer HTTP na Twoim komputerze, strona odświeża się sama po zapisie (Ctrl+S).
- **`http://127.0.0.1:5500`** = `localhost` = „ten komputer" - Twój laptop jest jednocześnie klientem i serwerem.
- **`file://`** (dwuklik na pliku) = bez serwera - dziś zadziała, ale ma ograniczenia.
- Struktura projektu: katalog (np. `moja-strona`) + plik **`index.html`** - strona startowa katalogu.
- Bez instalacji: **StackBlitz** (`stackblitz.com`) lub **CodeSandbox** (`codesandbox.io`).

## 6. Szkielet HTML5 - do skopiowania

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kim jestem</title>
</head>
<body>
  <h1>Jan Kowalski</h1>
  <p>Kilka słów o mnie.</p>
  <ul>
    <li>piłka nożna</li>
    <li>gry</li>
  </ul>
  <a href="https://akademia.tarnowska.pl">Moja ulubiona strona</a>
  <img src="ja.jpg" alt="Moje zdjęcie">
</body>
</html>
```

Znaczniki z tej planszy: `h1` (nagłówek), `p` (akapit), `ul`/`li` (lista), `a` (link), `img` (obrazek).

## 7. Liczby, które warto pamiętać (ze źródłami)

| Liczba | Źródło |
|---|---|
| JavaScript - najczęściej używany język **13. rok z rzędu** (~66% respondentów) | Stack Overflow Developer Survey 2025 |
| JS działa po stronie klienta na **98,9% stron** | W3Techs, 2026 |
| ponad **1,2 mld stron** (w 2000 r. tylko 17 mln) | Internet Live Stats, 2026 |
| **Chrome ~70–72%** rynku przeglądarek | StatCounter, 2025 |
| **84% programistów** używa lub planuje używać narzędzi AI | Stack Overflow 2025 |

---

Więcej wyjaśnień znajdziesz w [poradniku 0101](poradnik-0101.md), prompty do nauki z AI - w [mini-śnie AI jako tutor](ai-jako-tutor-sciega.md).
