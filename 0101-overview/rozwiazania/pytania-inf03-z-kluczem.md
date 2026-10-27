# 0101 · 5 pytań w stylu INF.03 — z kluczem odpowiedzi

Materiał dla prowadzącego · zakres: spotkanie 0101 · format: jednokrotny wybór A–D, jak w części pisemnej egzaminu INF.03.

**Punktacja:** 1 pkt za pytanie; kartkówka na 0102 to 4–5 pytań z tej puli (pytanie 6. jest zamienne — włączaj je zamiast jednego z powyższych, np. pytania 5).

**Rola tego pliku:** pula bazowa kartkówki na 0102 (razem z 1–2 pytaniami otwartymi, zgodnie z zasadami kursu). Przed 0102 przebuduj kolejność odpowiedzi, żeby klucz nie był ten sam.

---

## Pytanie 1

W którym roku Tim Berners-Lee przedstawił w organizacji CERN propozycję systemu World Wide Web?

- A. 1985
- B. 1987
- C. 1989
- D. 1991

**Odpowiedź: C** — propozycję hipertekstowego systemu zarządzania informacją Berners-Lee napisał w CERN w 1989 r.; rok 1991 to publikacja pierwszej strony WWW.

## Pytanie 2

Który zapis, umieszczony w pierwszej linii pliku, informuje przeglądarkę, że dokument jest napisany w HTML5?

- A. `<!DOCTYPE html>`
- B. `<html5>`
- C. `<meta name="wersja" content="5">`
- D. `<header>`

**Odpowiedź: A** — `<!DOCTYPE html>` to standardowa, skrócona deklaracja typu dokumentu w HTML5; znacznik `<html5>` nie istnieje, a `<header>` to znacznik treści.

## Pytanie 3

Jaką rolę w działaniu internetu pełni system DNS (Domain Name System)?

- A. szyfruje ruch sieciowy między klientem a serwerem
- B. tłumaczy nazwy domen na adresy IP serwerów
- C. przechowuje pliki, z których zbudowana jest strona internetowa
- D. kompresuje obrazki wysyłane do przeglądarki

**Odpowiedź: B** — DNS działa jak „książka telefoniczna internetu": zamienia zapamiętywalne nazwy (np. `zst.tarnow.pl`) na liczbowe adresy IP; szyfrowaniem ruchu zajmuje się HTTPS, a pliki stron trzyma serwer.

## Pytanie 4

W panelu Elements narzędzi Chrome DevTools zmieniono kolor nagłówka obcej strony internetowej. Co stanie się z tą zmianą po kliknięciu przycisku odświeżania (F5)?

- A. zostanie zapisana na serwerze, z którego pochodzi strona
- B. pozostanie w przeglądarce do końca bieżącej sesji
- C. zobaczą ją wszyscy użytkownicy odwiedzający stronę
- D. zniknie — przeglądarka pobierze oryginalne pliki z serwera

**Odpowiedź: D** — zmiany wprowadzone w DevTools są wyłącznie lokalne, w pamięci przeglądarki; odświeżenie pobiera pliki strony ponownie z serwera, więc powraca stan oryginalny.

## Pytanie 5

Silnik renderujący (layout engine) wykorzystywany przez przeglądarkę Google Chrome to:

- A. Blink
- B. WebKit
- C. Gecko
- D. Trident

**Odpowiedź: A** — Chrome (i Edge) używają silnika Blink, wywodzącego się z WebKit; WebKit napędza Safari, Gecko — Firefoksa, a Trident to historyczny silnik Internet Explorera.

## Pytanie 6 (zamienne — z bloku „trzy adresy, jedna strona")

Adres IP 127.0.0.1, zwany także **localhost**, oznacza:

- A. adres własnego komputera — ruch wysłany tam wraca do tej samej maszyny
- B. adres głównego serwera Google
- C. zarezerwowany adres stron szkolnych
- D. adres szkolnej sieci WiFi

**Odpowiedź: A** — 127.0.0.1 to pętla lokalna (loopback): wszystko wysłane na ten adres zostaje na Twoim komputerze; dlatego serwer deweloperski (np. Live Server) działa nawet bez internetu — klient i serwer to ta sama maszyna.

---

## Klucz w skrócie

| Pytanie | 1 | 2 | 3 | 4 | 5 | 6 (zamienne) |
|---|---|---|---|---|---|---|
| Odpowiedź | C | A | B | D | A | A |

## Zgodność z zakresem kartkówki na 0102

| Obszar zakresu | Pokryte pytaniem |
|---|---|
| historia WWW | 1 |
| klient–serwer (DNS, HTTP(S), URL) | 3 |
| klient–serwer — serwer lokalny (Live Server, 127.0.0.1/localhost) | 6 (zamienne) |
| Chrome DevTools | 4 |
| szkielet HTML | 2 |
| dodatkowo: przeglądarki i silniki | 5 |

Do kartkówki na 0102 (10 min) weź 4–5 z powyższych (przetasowane) + 1–2 pytania otwarte, np.: „Wymień trzy elementy szkieletu dokumentu HTML5, które mieszczą się w sekcji `head`, i napisz, do czego służy każdy z nich." albo „Wyjaśnij jednym zdaniem, czym różni się HTTP od HTTPS.".
