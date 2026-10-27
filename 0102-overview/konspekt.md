# 0102 · Konspekt zajęć - „HTML5: fundamenty i semantyka + dostępność (a11y)"

| | |
|---|---|
| **Semestr** | zimowy 2026 - spotkanie 2 z 9 |
| **Realizacja** | 28 X 2026 (grupa B) · 04 XI 2026 (grupa A) |
| **Czas** | 135 min = **kartkówka 10** + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25 |
| **Prowadzący** | mgr inż. Dominik Aksamit - Akademia Tarnowska |
| **Wersja materiałów** | 1.0 |
| **Scenariusz bazowy** | [scenariusz.md](scenariusz.md) |
| **Następne spotkanie** | 0103 · CSS3 - stylowanie i responsywność; **zaczyna się kartkówką z 0102** |

**Materiały towarzyszące:**

- prezentacja: [prezentacja.md](prezentacja.md) (18 slajdów),
- kartkówka (rozdrukka, 1/uczeń): [kartkowka.md](kartkowka.md),
- pakiet dla ucznia: [0102/](../0102/README.md) - instrukcja ćwiczeń z planem spotkania (3 bloki) + start live codingu: plik [index.html](../0102/index.html) („ściana divów"); do pobrania: [daksamit.pl/zp/0102](https://daksamit.pl/zp/0102),
- rozwiązania i klucze: [rozwiazania/](rozwiazania/README.md) - **tylko dla prowadzącego**.

## Cele zajęć - po spotkaniu uczeń:

- buduje **semantyczny szkielet strony** (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`) i uzasadnia, dlaczego nie „ściana divów" (czytniki ekranu, SEO, czytelność - i punkty w kryteriach INF.03),
- poprawnie strukturuje tekst: **kolejność nagłówków `h1`–`h6`**, akapity, wyróżnienia, listy `ul`/`ol`/`dl`, cytaty,
- robi **linki**: ścieżki względne i bezwzględne, `target="_blank"` + `rel="noopener"`, zakotwiczenia `#id`,
- wstawia **obrazy** z sensownym `alt`, zna formaty JPG/PNG/WebP/SVG i wie, kiedy który,
- tworzy **tabelę danych** z `caption`, `thead`/`th` i `tbody`/`td` - i wie, że tabela to nie layout,
- wstawia multimedia: `audio`/`video` z `controls`, `iframe` z `title`,
- buduje **formularz z walidacją HTML5**: doboru typu pola do danych, `label` powiązany `for`/`id`, `required`, `pattern`, `min`/`max`,
- rozumie **dostępność (a11y)**: po co (liczby WHO, European Accessibility Act), co robić w HTML (alt, `lang`, nagłówki po kolei, `label`, obsługa klawiaturą) i że WCAG streszcza się do zasad: spostrzegalne, funkcjonalne, zrozumiałe, solidne,
- zaczął **własny fanpage** (zespół/gracz/gra) - szkielet pod ostylowanie na 0103.

## Przygotowanie przed zajęciami

- [ ] Na komputerach uczniowskich i na maszynie prowadzącego: **Chrome** oraz **VS Code z rozszerzeniem Live Server** (jak na 0101).
- [ ] **Pakiet ucznia opublikowany**: [daksamit.pl/zp/0102](https://daksamit.pl/zp/0102) - wrzuć zip katalogu [../0102/](../0102/README.md) i sprawdź, że link pobiera plik (uczniowie pobierają na start zajęć).
- [ ] Projektor czytelny z ostatniej ławki (powiększ czcionkę w VS Code i Chrome).
- [ ] Internet działa; przetestuj wcześniej: `https://unsplash.com` (uczniowie pobierają stamtąd zdjęcia do `obrazy/`; uwaga: usługa hotlinkowania `source.unsplash.com` jest **wyłączona** - zwraca błąd, nie używaj jej w demo), `https://placehold.co/600x400?text=test`, `https://picsum.photos/seed/test/600/400`, `https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3`, film testowy `https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4`, `https://www.youtube.com/embed/dQw4w9WgXcQ`.
- [ ] Rozdrukki kartkówki - po 1 egzemplarzu na ucznia ([kartkowka.md](kartkowka.md), drukuj bez klucza).
- [ ] Otwarte karty na start: prezentacja, [MDN Web Docs](https://developer.mozilla.org/pl/docs/Web/HTML) (element reference).
- [ ] **Plan B bez internetu:** przygotuj katalog `obrazy/` z 3–4 lokalnymi plikami jpg/png przygotowanymi na uczniowskie maszyny; demo iframe zamień na zrzut ekranu; formularz i walidacja działają w pełni offline.

Oznaczenia w przebiegu: **[DEMO NA ŻYWO]** - pokazuje prowadzący, uczniowie patrzą; **[LIVE CODING]** - uczniowie piszą razem z prowadzącym u siebie; **[PRACA SAMODZIELNA]** - uczniowie pracują samodzielnie, prowadzący pomaga indywidualnie.

---

## Kartkówka nr 1 (0:00–0:10, 10') - zakres: 0101

**[PRACA SAMODZIELNA]** Rozdaj arkusze ([kartkowka.md](kartkowka.md)): 3 pytania zamknięte (A–D) + 2 otwarte (szkielet HTML + DevTools/F5), max 5 pkt, ocena cząstkowa. Przebieg: rozdanie (1') → pisanie (8') → zbiór (1'). Przypomnij zasady: jedna odpowiedź w pytaniach zamkniętych, pisać czytelnie.

Klucz, punktacja, skala ocen i scenariusz omówienia: [rozwiazania/kartkowka-klucz.md](rozwiazania/kartkowka-klucz.md). Wyniki oddaj na 0103.

## Sekcja 1 (0:10–1:00, 50 min) - szkielet strony i treść

### 0:10–0:12 (2') · Omówienie kartkówki na skróty

Bez odczytywania odpowiedzi. Dwie pułapki z klucza: `h1` vs `title` (nagłówek na stronie vs tytuł karty) oraz „dlaczego zmiany z DevTools znikają po F5" (edycja lokalna, odświeżenie pobiera pliki z serwera). Zapowiedz: wyniki wrócą na 0103.

### 0:12–0:22 (10') · Semantyczny szkielet - ściana divów **[LIVE CODING - etap 1]**

Wprowadzenie (2', slajdy 4–5): strona z samych `div`-ów działa i wygląda - ale kod nic nie znaczy: czytnik ekranu nie ma struktury, wyszukiwarka nie rozpoznaje nawigacji, programista się gubi. Semantyka = znaczniki, które **mówią, czym jest treść**, nie jak wygląda.

Uczniowie kopiują `index.html` z pakietu ([daksamit.pl/zp/0102](https://daksamit.pl/zp/0102) - kto nie pobrał na start zajęć, niech pobierze teraz) do swojego katalogu zajęć (nazwa już właściwa - „ściana divów"; Live Server pokaże stronę od razu) i przekształcają razem z prowadzącym (skrypt: etap 1 poniżej): `div.naglowek` → `header` (+ `h1`), `div.menu` → `nav` z listą, `div.glowna` → `main`, `div.czesc` → `section` z `h2`, `div.wiadomosc` → `article` z `h3`, `div.bok` → `aside`, `div.stopka` → `footer`. Po zapisie: strona wygląda prawie tak samo - **a kod zaczął znaczyć**; pokaż różnicę w DevTools (Elements: widać nazwy sekcji).

### 0:22–0:31 (9') · Tekst i listy **[LIVE CODING - etap 2]**

Krótko (slajdy 6–7): nagłówki `h1`–`h6` - **kolejność bez przeskoków** (h1 → h2 → h3), dokładnie jeden `h1`; `p` akapit; `strong` (ważność) vs `em` (nacisk); `br` nowa linia, `hr` przerwa tematyczna; `blockquote` cytat; `ul`/`ol`/`dl` - kiedy które. Pułapka egzaminacyjna: `ol` = kolejność ma znaczenie.

Uczniowie dopisują w sekcji „O zespole": listę składu (`ul`), historię (`ol`), mini-słowniczek (`dl`), wzmiankę z `strong`/`em`, cytat z recenzji (`blockquote`), a między sekcjami jedno `hr` (skrypt: etap 2).

### 0:31–0:40 (9') · Linki i ścieżki **[LIVE CODING - etap 3]**

Wprowadzenie (slajd 8): `a href`; **ścieżka względna** (`obrazy/koncert.jpg` - plik w naszym projekcie) vs **bezwzględna** (`https://…` - pełny adres); `target="_blank"` zawsze z `rel="noopener"`; zakotwiczenie `#id` - skok do sekcji; `mailto:`. Pułapka INF.03: rozpoznać ścieżkę względną i bezwzględną w kodzie.

Uczniowie: pozycje `nav` zamieniają w linki do sekcji (`#o-zespole`, `#aktualnosci`…), sekcje dostają `id`; w stopce link zewnętrzny (MDN) z `target="_blank" rel="noopener"` i kontakt `mailto:` (skrypt: etap 3). Test: klik w menu skacze do sekcji.

### 0:40–0:50 (10') · Obrazy **[LIVE CODING - etap 4]**

Wprowadzenie (slajdy 9–10): `img` z `src`, **`alt` opisuje treść obrazu** (nie „obrazek"!), `width`/`height` rezerwują miejsce (strona nie skacze); `figure` + `figcaption` - obraz z podpisem; formaty: **JPG** - zdjęcia, **PNG** - zrzuty/przezroczystość, **WebP** - jak JPG/PNG, ale ~25–35% lżejszy (dokumentacja Google WebP), **SVG** - ikony/logotypy, skaluje się bez utraty jakości.

Uczniowie tworzą sekcję „Galeria": 2–3 obrazy w `figure` z podpisami - z plików lokalnych `obrazy/…` lub poglądowych `placehold.co` (skrypt: etap 4).

### 0:50–1:00 (10') · Dostępność (a11y) - fundament **[DEMO NA ŻYWO + krótki audyt - etap 5]**

Slajd 11 (liczby, zawsze ze źródłem i rokiem):

- **1 na 6 ludzi na świecie** (ok. 1,3 mld, 16% populacji) żyje z istotną niepełnosprawnością - WHO, 2023,
- **European Accessibility Act** (dyrektywa UE 2019/882) obowiązuje **od 28 czerwca 2025** - m.in. e-commerce i usługi konsumenckie w UE muszą być dostępne,
- **95,9% z miliona badanych stron głównych** ma wykrywalne błędy dostępności - WebAIM Million, 2026; czyli: przeciętna strona jest **niedostępna** - Wasze mogą być lepsze.

Slajd 12 (praktyka): `alt`, `lang="pl"`, nagłówki po kolei, `label` powiązany z polem, strona obsługiwana **Tabem**, ARIA - **tylko gdy HTML nie wystarczy**; WCAG w pigułce - 4 zasady: **spostrzegalna, funkcjonalna, zrozumiała, solidna**.

**[DEMO NA ŻYWO]** Odłóż mysz: kliknij pasek adresu i przechodź stronę live codingu samym **Tabem** - widać obwódkę fokusu, kolejność logiczna (menu → treść). Następnie szybki audyt własnej strony z uczniami: czy jest `lang="pl"`? jeden `h1`? nagłówki bez przeskoków? wszystkie obrazy z `alt`? (formularz jeszcze bez `label` - to naprawimy po przerwie; ta celowa dziura motywuje blok formularzy). Opcjonalnie 1–2 min: czytnik ekranu (VoiceOver: Cmd+F5 / NVDA) czyta nagłówki strony.

---

## Przerwa (15 min) · 1:00–1:15

Przy okazji: zapisz na tablicy wzór zakotwiczenia (`href="#id"` + `id` na sekcji) i cztery zasady WCAG - niech wiszą do końca zajęć.

---

## Sekcja 2 (1:15–1:50, 35 min) - tabele, multimedia, formularze, start fanpage'a

### 1:15–1:25 (10') · Tabele **[LIVE CODING - etap 6]**

Wprowadzenie (slajd 13): tabela służy **do danych**, nie do układania strony (przestarzały trik z lat 90.); struktura: `table` + `caption` (tytuł) + `thead` z `th` + `tbody` z `td`; `scope="col"`/`"row"` mówi czytnikom ekranu, co opisuje nagłówek. INF.03 lubi zestawienia danych - tabela wraca w każdej pracy praktycznej.

Uczniowie dodają sekcję „Koncerty" z tabelą trasy (3 wiersze danych, skrypt: etap 6). Kontrola: nagłówki w `th`, tytuł w `caption`.

### 1:25–1:30 (5') · Multimedia **[LIVE CODING - etap 7]**

Slajd 14 + wpisujemy razem (etap 7): `video` z `controls` (film testowy), `iframe` z YouTube **z atrybutem `title`** (czytnik ekranu musi wiedzieć, co jest w ramce), `audio` z `controls` (utwór przykładowy). Uwaga praktyczna: filmy z YouTube wstawiamy przez `iframe` (embed), nie przez `video`.

### 1:30–1:45 (15') · Formularze + walidacja HTML5, krok po kroku **[LIVE CODING - etapy 8–14]**

Wprowadzenie (2', slajdy 15–16): `form` (`action`, `method`), każde pole z `label` powiązanym `for`/`id` (klik w etykietę uaktywnia pole - i a11y), dobór typu do danych, walidacja **za darmo w przeglądarce**: `required`, `pattern`, `min`/`max`. Niemal każda praca praktyczna INF.03 ma formularz - dziś budujemy go dokładnie w egzaminacyjnym stylu.

Uczniowie piszą razem formularz „Klub Fana" w sekcji „Zapisz się" (skrypt: etapy 8–14): szkielet i `label`/`for`/`id` → imię (`required`, `minlength`) → e-mail (`type="email"`) → data (`type="date"` - kalendarz!) → liczba biletów (`min`/`max`) → kod promocyjny (`pattern` + `title`) → `select` + `textarea` → zgoda (`checkbox` + `required`) i przycisk. Finał: **klik „Wyślij" przy pustym formularzu** - przeglądarka sama blokuje i komunikuje po polsku.

**Akcent Akademii Tarnowskiej** (jedno zdanie, w trakcie pisania formularza): „Dokładnie takie formularze studenci Akademii Tarnowskiej robią na zaliczeniowe projekty aplikacji - niedługo będziecie mieli przewagę na starcie."

### 1:45–1:50 (5') · Start ćwiczenia głównego: fanpage **[PRACA SAMODZIELNA]**

Uczniowie zakładają katalog `fanpage/`, plik `index.html` i wybierają temat (zespół/gracz/gra). Pierwszy krok: szkielet semantyczny z nagłówkami - na wzorze strony z live codingu. Instrukcja i checklista: [0102/README.md](../0102/README.md). Prowadzący krąży - pomaga w doborze tematów.

---

## Sekcja 3 (1:50–2:15, 25 min) - domknięcie: fanpage, INF.03, podsumowanie

### 1:50–2:10 (20') · Ćwiczenie główne: fanpage (cd.) **[PRACA SAMODZIELNA]**

Kolejność pracy (tablica): wariant A - szkielet + 2 sekcje + galeria z `alt` + formularz (imię, e-mail); wariant B - + tabela danych + `select`/`radio` w `fieldset` + multimedia; wariant C ⭐ - menu wewnętrzne + audyt Tabem + poprawki. Każdy wariant A kończy **checklistą a11y** (8 punktów w [0102/README.md](../0102/README.md)): `alt`, `lang`, jeden `h1`, nagłówki po kolei, `label` przy każdym polu, przejście Tabem, sensowne teksty linków, `title` na `iframe`.

Prowadzący pomaga indywidualnie; szybcy łapią B, najszybsi C. 2 minuty przed końcem bloku: „odłóżcie myszy i przejdźcie swoje strony Tabem" - mini-audyt na własnym materiale.

### 2:10–2:15 (5') · Domknięcie dnia

1. **Mini-quiz ustny** (2–3 pytania, nie z puli kartkówkowej): „Dlaczego `article`, a nie `div`, dla newsa?" · „Który format na logo: JPG czy SVG - i dlaczego?" · „Co robi atrybut `for` w `label`?"
2. **Podsumowanie rundą**: „wymień jedną rzecz, którą dziś odkryłeś/aś" - 3–4 ochotników.
3. **Zadanie domowe** (30–45 min): dokończ fanpage z checklistą a11y · **detektyw dostępności**: znajdź stronę z oczywistym błędem (brak `alt`, ściana divów) i zapisz adres + co jest nie tak - omówimy na 0103 · przygotuj się do kartkówki.
4. **Zapowiedź 0103 (CSS3)**: „Dziś zbudowaliście dom - na 0103 przyjdzie wyposażenie i farba: kolory, fonty, flexbox i wersja mobilna. **Fanpage koniecznie zachowajcie** - ostylujemy właśnie jego."
5. **Zakres kartkówki na 0103**: semantyczne znaczniki (`article` vs `div`, `nav`/`header`/`footer`) · typy `input` i dobór do danych · `label` + a11y · tabele (`th`/`td`, `caption`) · walidacja HTML5 (`required`, `pattern`, `min`/`max`).

---

## Live coding - scenariusz krok po kroku

Każdy etap: powiedz → napisz → zapisz (Ctrl+S) → wszyscy patrzą na odświeżoną stronę w Live Server. Start: uczniowie kopiują `index.html` z pakietu ucznia do swojego katalogu zajęć - nazwa już jest właściwa („ściana divów"). Finalny plik (do wysłania niedoświetlnym): [rozwiazania/live-coding/index.html](rozwiazania/live-coding/index.html). Temat przykładowy: zespół **„Bity z Podwórka"** - kod można wklejać bez edycji, komentarze po polsku są w plikach.

### Etap 1 - ściana divów → szkielet semantyczny (0:12–0:22)

Zamiany (treść zostaje, zmieniają się opakowania):

```html
<!-- div.naglowek → header; div.tytul → h1; div.podtytul → p -->
<header>
  <h1>Bity z Podwórka</h1>
  <p>Fanpage zespołu - prowadzony przez fanów, z miłości do bitów.</p>
</header>

<!-- div.menu → nav; pozycje menu → lista ul/li (linki dodamy w etapie 3) -->
<nav>
  <ul>
    <li>O zespole</li>
    <li>Aktualności</li>
    <li>Galeria</li>
    <li>Koncerty</li>
    <li>Zapisz się</li>
  </ul>
</nav>

<!-- div.glowna → main -->
<main>
  <!-- div.czesc → section; div.naglowek-czesci → h2 -->
  <section>
    <h2>O zespole</h2>
    <!-- div.akapit → p (bez zmian treści) -->
  </section>

  <!-- div.wiadomosc → article; div.tytul-wiadomosci → h3 -->
  <section>
    <h2>Aktualności</h2>
    <article>
      <h3>Wychodzi singiel „Kuchnia"</h3>
      <p><!-- treść bez zmian --></p>
    </article>
    <article>
      <h3>Konkurs na okładkę albumu</h3>
      <p><!-- treść bez zmian --></p>
    </article>
  </section>

  <!-- kolejne section: Koncerty i Zapisz się wg tego samego wzorca -->

  <!-- div.bok → aside -->
  <aside>
    <h2>Ciekawostka</h2>
    <p><!-- treść bez zmian --></p>
  </aside>
</main>

<!-- div.stopka → footer -->
<footer>
  <p><!-- treść bez zmian --></p>
</footer>
```

Puenta po zapisie: strona wygląda prawie identycznie - **a czytnik ekranu i Google już wiedzą, co jest menu, a co treścią**. W DevTools (Elements) widać czytelne nazwy sekcji.

### Etap 2 - tekst i listy (0:22–0:31)

Dopisz w sekcji „O zespole":

```html
<!-- strong = ważność, em = nacisk (czytnik zmienia intonację) -->
<p>
  Nazwa wzięła się z miejsca pierwszych prób: <strong>podwórko</strong>
  przy ulicy Miodowej, <em>pralka</em> jako perkusja i sąsiadka Grażyna
  jako pierwszy recenzent.
</p>

<h3>Skład</h3>
<!-- ul = kolejność nieistotna -->
<ul>
  <li>Kuba - wokal i teksty</li>
  <li>Zosia - klawisze i bity</li>
  <li>Igor - perkusja (i garnek w „Kuchni")</li>
</ul>

<h3>Jak do tego doszło</h3>
<!-- ol = kolejność ma znaczenie -->
<ol>
  <li>2022 - pierwszy koncert na szkolnym festynie</li>
  <li>2024 - wygrana w przeglądzie kapel podwórkowych Małopolski</li>
  <li>2026 - album „Mgła i Bit" i ten fanpage</li>
</ol>

<h3>Mini-słowniczek fana</h3>
<!-- dl = termin + opis -->
<dl>
  <dt>Bit</dt>
  <dd>Powtarzalny szkic rytmiczny, na którym stoi utwór.</dd>
  <dt>Podwórko</dt>
  <dd>Miejsce pierwszych prób - i stan ducha zespołu.</dd>
</dl>

<!-- blockquote = dłuższy cytat z podaniem autora -->
<blockquote>
  <p>„Mgła i Bit" brzmi, jakby Daft Punk wynajął mieszkanie przy Miodowej - i to działa.</p>
  <footer>- fragment przykładowej recenzji portalu „Brzmienia"</footer>
</blockquote>
```

Oraz jedno `hr` między sekcją „O zespole" a „Aktualności" (przerwa tematyczna - rzadko potrzebna).

### Etap 3 - linki i zakotwiczenia (0:31–0:40)

```html
<!-- sekcje dostają id; nav linkuje do nich przez #id -->
<section id="o-zespole"> ... </section>

<nav>
  <ul>
    <li><a href="#o-zespole">O zespole</a></li>
    <li><a href="#aktualnosci">Aktualności</a></li>
    <li><a href="#galeria">Galeria</a></li>
    <li><a href="#koncerty">Koncerty</a></li>
    <li><a href="#zapis">Zapisz się</a></li>
  </ul>
</nav>
```

W stopce - link bezwzględny w nowej karcie (z `rel="noopener"`!) i `mailto:`:

```html
<p>
  Dokładnie te znaczniki opisuje
  <a href="https://developer.mozilla.org/pl/docs/Web/HTML" target="_blank" rel="noopener">
    MDN Web Docs
  </a>
  - darmowa encyklopedia HTML.
</p>
<p>
  Pytania o fanpage?<br>
  Napisz: <a href="mailto:klubfana@bity-z-podworka.example">klubfana@bity-z-podworka.example</a>
</p>
```

Zwróć uwagę: `mailto:` w `href` otwiera program pocztowy; `br` = nowa linia w akapicie (nie do robienia odstępów!).

### Etap 4 - obrazy: galeria (0:40–0:50)

```html
<section id="galeria">
  <h2>Galeria</h2>

  <!-- figure = obraz z podpisem; alt opisuje treść; width/height rezerwują miejsce -->
  <figure>
    <img
      src="obrazy/koncert.jpg"
      alt="Zespół gra na koncercie w Tarnowie - Kuba przy mikrofonie, za nim Zosia przy klawiszach"
      width="600"
      height="400"
    >
    <figcaption>Koncert w Tarnowie, maj 2026</figcaption>
  </figure>

  <!-- wersja bez własnych plików: obraz poglądowy z placehold.co -->
  <figure>
    <img
      src="https://placehold.co/600x400/0d6efd/ffffff?text=Sesja+w+studiu"
      alt="Zdjęcie poglądowe: zespół podczas sesji nagraniowej w studiu"
      width="600"
      height="400"
    >
    <figcaption>Sesja nagraniowa albumu „Mgła i Bit" (zdjęcie poglądowe)</figcaption>
  </figure>
</section>
```

Dyskusja formatów przy slajdzie 10 (JPG/PNG/WebP/SVG); jeśli użyliście plików lokalnych - pokaż w DevTools (Network) ich rozmiary.

### Etap 5 - audyt a11y na własnej stronie (0:50–1:00, bez pisania kodu)

Checklista na głos, uczniowie sprawdzają u siebie: `lang="pl"` ✓, jeden `h1` ✓, nagłówki bez przeskoków ✓, każda `figure` z `alt` ✓. **[DEMO]** przejście Tabem; opcjonalnie czytnik ekranu. Zapisz na tablicy 4 zasady WCAG.

### Etap 6 - tabela (1:15–1:25)

```html
<section id="koncerty">
  <h2>Koncerty</h2>

  <table>
    <caption>Trasa jesienna 2026 - planowane koncerty</caption>
    <thead>
      <tr>
        <th scope="col">Data</th>
        <th scope="col">Miasto</th>
        <th scope="col">Miejsce</th>
        <th scope="col">Bilet</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>12.11.2026</td>
        <td>Tarnów</td>
        <td>Klub Pod Dachem</td>
        <td>60 zł</td>
      </tr>
      <!-- dwa kolejne wiersze wg tego samego wzorca -->
    </tbody>
  </table>
</section>
```

### Etap 7 - multimedia (1:25–1:30)

```html
<!-- video z pliku; controls = przyciski odtwarzacza -->
<video controls width="600">
  <source
    src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
    type="video/mp4"
  >
  Twoja przeglądarka nie obsługuje wideo.
</video>

<!-- iframe = wstawka innej strony; title czyta czytnik ekranu! -->
<iframe
  src="https://www.youtube.com/embed/dQw4w9WgXcQ"
  width="560"
  height="315"
  title="Teledysk polecany przez zespół"
  allowfullscreen
>
</iframe>

<!-- audio z controls -->
<audio controls src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
  Twoja przeglądarka nie obsługuje elementu audio.
</audio>
```

### Etapy 8–14 - formularz krok po kroku (1:30–1:45)

**Etap 8** - szkielet + pierwsze pole (wzorzec `label`/`for`/`id`):

```html
<section id="zapis">
  <h2>Zapisz się do Klubu Fana</h2>
  <form action="#" method="post">
    <!-- for wskazuje id pola: klik w etykietę uaktywnia pole -->
    <label for="imie">Imię *</label>
    <input type="text" id="imie" name="imie" required minlength="2">
  </form>
</section>
```

**Etap 9** - e-mail (walidacja formatu za darmo):

```html
<label for="email">E-mail *</label>
<input type="email" id="email" name="email" required>
```

**Etap 10** - data (kalendarz bez JavaScriptu):

```html
<label for="koncert">Koncert, na który chcesz przyjść</label>
<input type="date" id="koncert" name="koncert">
```

**Etap 11** - liczba z zakresem:

```html
<label for="bilety">Liczba biletów (1–6)</label>
<input type="number" id="bilety" name="bilety" min="1" max="6">
```

**Etap 12** - wzorzec (`pattern` + `title` z podpowiedzią):

```html
<label for="kod">Kod promocyjny (format: BP-2026)</label>
<input
  type="text"
  id="kod"
  name="kod"
  pattern="[A-Z]{2}-[0-9]{4}"
  title="Dwie wielkie litery, myślnik i cztery cyfry, np. BP-2026"
>
```

**Etap 13** - lista rozwijana i pole długiego tekstu:

```html
<label for="skad">Skąd znasz zespół?</label>
<select id="skad" name="skad">
  <option value="koncert">byłem/byłam na koncercie</option>
  <option value="instagram">Instagram</option>
  <option value="znajomi">polecają znajomi</option>
  <option value="inne">inne</option>
</select>

<label for="utwor">Twój ulubiony utwór - i dlaczego?</label>
<textarea id="utwor" name="utwor" rows="3"></textarea>
```

**Etap 14** - zgoda i przycisk + **test walidacji**:

```html
<input type="checkbox" id="zgoda" name="zgoda" required>
<label for="zgoda">Zgadzam się dostawać newsletter *</label>

<button type="submit">Zapisz mnie do Klubu Fana</button>
```

Klik „Zapisz mnie" przy pustym formularzu → przeglądarka blokuje wysłanie i wskazuje pierwsze puste pole; wpisz zły kod promocyjny (np. `xyz`) → komunikat z treści `title`. Pokaż typy wow na słowo: `type="color"` i `type="range"` (30 sekund, „sam przetestuj w wariancie B").

---

## Notatki prowadzącego

- **Praktyka uczniowska:** live coding z pisaniem u siebie ≈ 60' (Sekcja 1: etapy 1–4; Sekcja 2: etapy 6–14) + praca samodzielna 25' + audyt Tabem 4' ≈ **90 z 125 minut czynnych zajęć (~70%)** - warunek min. 60% spełniony z zapasem; jeśli ściskasz czas, tnij opowieści przy slajdach, nigdy ćwiczenia.
- **Statystyki a11y** - używaj wyłącznie trzech zweryfikowanych liczb (sekcja 0:50–1:00): WHO 2023 (1,3 mld / 16% / 1 na 6), WebAIM Million 2026 (95,9% stron głównych z błędami WCAG 2), EAA - dyrektywa (UE) 2019/882, obowiązuje od 28 VI 2025. Przed zajęciami odśwież dane u źródła - pełne adresy w [PLAN.md](PLAN.md), sekcja „Linki - źródła i narzędzia".
- **Akcent Akademii Tarnowskiej** - dokładnie jedno zdanie w bloku formularzy (1:30–1:45, skrypt wyżej). Zero tonu reklamy.
- **Przekaz o narzędziach** (jedno zdanie do wypowiedzenia przy pokazie walidacji - etap 14: przeglądarka pilnuje formularza za darmo - albo przy narzędziach z linków, np. WAVE czy TinyPNG): „W dzisiejszych czasach nie jest ważne, jak umiecie budować, ale szybko potraficie korzystać z narzędzi, które za nas pracę wykonują."
- **Czytnik ekranu (opcjonalnie, max 2 minuty):** macOS - VoiceOver (Cmd+F5, czytanie nagłówków przez Cmd+F5 → strzałki); Windows - NVDA (darmowy). Nie ucz obsługi - pokaż tylko, że strona „mówi" i że nagłówki po kolei robią robotę.
- **Tempo Sekcji 1:** ściana divów to serce zajęć - nie skracaj etapu 1 poniżej 8 minut; jeśli klasa szybka, w etapie 2 dodaj drugi cytat lub dłuższy słowniczek.
- **Uczniowie bez VS Code:** jak na 0101 - StackBlitz (`stackblitz.com`) lub CodeSandbox (`codesandbox.io`), projekt HTML; plik startowy wklejają do `index.html`.
- **Wstawka YouTube w demo** (etap 7) to celowo film-żart (Rick Astley) - mały humor na przebudzenie po przerwie; jeśli wolisz, podmień `src` iframe'a na teledysk pasujący do demo.
- **Ukryte stylowanie w pliku startowym („easter egg"):** `index.html` ucznia ma w head **zakomentowany** skrypt Tailwind CDN i kilka klas układu na divach. Domyślnie strona jest więc czysta (puenta „po zamianie divów wygląda prawie tak samo" działa jak dotąd). Jeśli zostanie chwili po etapie 14 - pokaż na żywo: odkomentowanie jednej linii delikatnie styluje stronę; zapowiedz, że na 0103 (CSS3) zrozumieją, skąd to się bierze.
- **Plan B bez internetu:** obrazy lokalne z `obrazy/`, zamiast iframe - zrzut ekranu z komentarzem „tu normalnie wchodzi wstawka YouTube"; formularz i walidacja działają offline w całości.
- **5 pytań w stylu INF.03** z tego spotkania (baza kartkówki na 0103): [rozwiazania/pytania-inf03-z-kluczem.md](rozwiazania/pytania-inf03-z-kluczem.md). **Nie pokazuj ich uczniom na zajęciach.**
- **Kontynuacja:** fanpage uczniów wraca na 0103 (stylowanie CSS) i 0104 (publikacja + pierwszy JS) - przypomnij o zabezpieczeniu projektu (`fanpage/` z katalogiem `obrazy/`).

## Checklista jakości (AGENTS.md)

- [x] Suma czasów = 135 min (kartkówka 10 + sekcja 50 + przerwa 15 + sekcja 35 + sekcja 25), rozpiska co 2–10 min z oznaczonymi momentami live coding i pracy samodzielnej.
- [x] Kartkówka: zakres z 0101, 3 pytania zamknięte INF.03 + 2 otwarte, klucz + punktacja 0–5 + skala ocen ([kartkowka.md](kartkowka.md) / [rozwiazania/kartkowka-klucz.md](rozwiazania/kartkowka-klucz.md)).
- [x] Kod: domknięte znaczniki, poprawne atrybuty, działająca walidacja formularza (`required`, `pattern`, `min`/`max`), komentarze po polsku.
- [x] Ćwiczenia w wariantach A/B/C, każde z pełnym rozwiązaniem; rozwiązania wyłącznie w `rozwiazania/`.
- [x] Nawiązanie do INF.03 (formularz + tabela + semantyka w formacie egzaminacyjnym) + 5 pytań egzaminacyjnych z kluczem w materiałach prowadzącego.
- [x] Jeden subtelny akcent Akademii Tarnowskiej (blok formularzy, skrypt dosłowny).
- [x] Zadanie domowe (30–45 min) + zakres kartkówki na następne spotkanie (0103).
- [x] Statystyki wyłącznie zweryfikowane, każda ze źródłem i rokiem (WHO 2023, WebAIM 2026, EAA 2019/882 od 28 VI 2025).
