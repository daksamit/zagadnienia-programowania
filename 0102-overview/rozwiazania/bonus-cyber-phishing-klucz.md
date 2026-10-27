# 0102 · Bonus ⭐ „Detektyw phishingu" - klucz dla prowadzącego

Materiał **wyłącznie dla prowadzącego**. Dotyczy bonusu cyberbezpieczeństwa z pakietu ucznia: [0102/README.md](../../0102/README.md) (sekcja „Bonus ⭐ - detektyw phishingu").

| | |
|---|---|
| **Czas** | minimalnie 3–5 min omówienia na końcu Sekcji 3; pełny wariant ~10 min (grupy, które zdążyły wariant C) |
| **Forma** | dobrowolny bonus dla chętnych; **nie podlega ocenie i nie wchodzi do kartkówki na 0103** |
| **Kiedy zadać** | w Sekcji 3 uczniom, którzy skończyli wariant C, albo jako dodatkowe zadanie domowe dla chętnych (detektyw dostępności dostaje wtedy „brata") |

## Dlaczego ten bonus na zajęciach z HTML

Phishing to najbardziej „HTML-owy" temat w cyberbezpieczeństwie: fałszywa strona to dobrze zbudowany dokument, a ofiara odróżnia go tylko wtedy, gdy umie czytać kod. Bonus nagradza dokładnie tę wiedzę z dzisiejszego dnia: linki (`href` vs tekst), ścieżki bezwzględne i budowę adresu (0101), formularze, `method`, typy `input`, komentarze HTML. Uczymy **rozpoznawania i obrony** - analizujemy gotową makietę, nie budujemy ataku.

## 8 czerwonych flag (komplet)

| # | Flaga | Gdzie w kodzie | Dlaczego to flaga | Powiązanie z zajęciami |
|---|---|---|---|---|
| 1 | Presja czasu i groźba | „zostanie zablokowane", „24 godziny", „trwale usunięte" | klasyczny social engineering - ofiara działa pod emocją i nie analizuje | reguła: „pilne = podejrzane" |
| 2 | Ogólnikowy zwrot | „Drogi Kliencie" | nadawca nie zna imienia; bank i portal znają swoich klientów | kontekst, nie HTML |
| 3 | Tekst linku ≠ `href` | tekst: `https://www.paypal.com/logowanie`, `href`: `paypa1-…/potwierdz` | najważniejsza flaga: użytkownik widzi tekst, przeglądarka idzie po `href` | 0102: linki; pytanie zamienne INF.03 o `target`/`rel` |
| 4 | `http://` zamiast `https://` | w `href` i `action` | dane i strona jadą otwartym tekstem; prawdziwy portal płatności zawsze wymaga HTTPS | 0101: HTTPS na kartkówce |
| 5 | Domena-pułapka | `paypa1-bezpieczne-logowanie.example` | „1" zamiast „l" (typosquatting) + nadmiarowe „bezpieczne-logowanie"; `-` i dodatkowe słowa maskują cudzą domenę | 0101: budowa URL; 0102: ścieżki bezwzględne |
| 6 | `method="get"` przy polu hasła | `<form … method="get">` | login i hasło wylądowałyby w pasku adresu, historii przeglądarki i logach pośrednich | 0102: formularze; eksperyment GET vs POST z zadania |
| 7 | Niewidoczne pole | `<input type="hidden" name="kampania">` | atakujący taguje sobie, która wersja maila przynosi dane; ofiara go nie widzi, a jest wysyłane | 0102: typy `input` |
| 8 | Komentarz HTML w źródle | `<!-- v3: poprzednia domena zablokowana… -->` | ślad „fabryki phishingu": strona to kolejna iteracja po blokadzie poprzedniej; widoczny tylko w view source | lekcja ogólna: przeglądarka dostaje cały kod - komentarze też |

**Progi:** 5 flag = bardzo dobrze; 6–7 = sokole oko; 8 = kompletny detektyw. Jeśli uczeń wskazał coś spoza tabeli i da się to obronić (patrz „poza konkursem") - licz jako flagę.

## Poza konkursem - o czym warto wspomnieć przy omówieniu

- **`label`-e są poprawnie powiązane** (`for`/`id`) - szablon phishera bywa zrobiony staranniej niż niejedna prawdziwa strona; dobra ironiczna puenta po dzisiejszym bloku a11y.
- **Stopka „© 2026 PayPal Inc."** - kopiowany detal budujący wiarygodność; przypomina `footer` z ćwiczeń.
- **Domena `.example`** jest zarezerwowana do przykładów (RFC 2606) - makieta fizycznie nigdzie nie wyśle danych, można ją bezpiecznie otwierać i „wysyłać".
- **Eksperyment GET vs POST:** `get` dokleja dane do adresu (zostają w historii przeglądarki i logach), `post` wysyła je w ciele zapytania. Na INF.03 wraca przy PHP - dziś wystarczy intuicja „hasło nigdy w adresie".

## Scenariusz omówienia (3–5 min)

1. Szybka runda: kto znalazł 5+? kto 8? (ręka do góry - bez oceniania).
2. Omawiaj flagi od „widocznych na oko" do „tylko w źródle": presja → zwrot → link → `http`/domena → formularz (`get`, `hidden`) → komentarz. Kolejność sama w sobie jest puentą: **im więcej umiesz w HTML, tym więcej widzisz**.
3. Puenta obowiązkowa: strony nie ocenia się po wyglądzie, tylko po źródle - **wszystko, co wysyłasz do przeglądarki, jest publiczne** (to samo dotyczy np. haseł i kluczy zostawianych w komentarzach prawdziwych projektów).
4. Jeśli klasa nie robiła eksperymentu GET vs POST na żywo - zrób go przy swoim projekcie na rzutniku (30 sekund).

## Czego w bonusie świadomie nie ma

- Nie pokazujemy, jak budować stronę phishingową od zera, pisać marki ani omijać filtrów antyspamowych - analiza obronna gotowej makiety to edukacja świadomości zagrożeń, nie instruktaż ataku.
- Nie ma „prawdziwego" ataku tabnabbing na żywo - wątek `rel="noopener"` zostaje na poziomie świadomości z puli INF.03; powrót do niego jest naturalny przy JS (0104).
