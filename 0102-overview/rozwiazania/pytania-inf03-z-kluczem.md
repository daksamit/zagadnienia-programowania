# 0102 · 5 pytań w stylu INF.03 — z kluczem odpowiedzi

Materiał dla prowadzącego · zakres: spotkanie 0102 (HTML5 — semantyka, treść, formularze, tabele, a11y) · format: jednokrotny wybór A–D, jak w części pisemnej egzaminu INF.03.

**Punktacja:** 1 pkt za pytanie; kartkówka na 0103 to 4–5 pytań z tej puli (pytania 6. i 7. są zamienne — włączaj je zamiast jednego z powyższych).

**Rola tego pliku:** pula bazowa kartkówki na 0103 (razem z 1–2 pytaniami otwartymi, zgodnie z zasadami kursu). Przed 0103 przebuduj kolejność odpowiedzi, żeby klucz nie był ten sam. **Nie pokazuj pytań uczniom na zajęciach.**

---

## Pytanie 1

W serwisie informacyjnym każda wiadomość (tytuł, data, treść) stanowi samodzielną, powtarzalną całość, rozsyłaną też w RSS. Którego znacznika semantycznego użyjesz dla jednej wiadomości?

- A. `<section>`
- B. `<article>`
- C. `<aside>`
- D. `<div>`

**Odpowiedź: B** — `article` przeznaczony jest dla samodzielnych, powtarzalnych całości treści (news, post, wpis); `section` grupuje powiązane treści w obrębie strony, `aside` to treść poboczna, a `div` nie niesie żadnego znaczenia.

## Pytanie 2

Który zapis obrazu jest najlepszy z punktu widzenia dostępności (a11y)?

- A. `<img src="kot.png" title="Kot">`
- B. `<img src="kot.png" alt="Rudy kot śpiący na parapecie">`
- C. `<img src="kot.png" alt="obrazek">`
- D. `<img src="kot.png">`

**Odpowiedź: B** — atrybut `alt` ma opisywać rzeczywistą treść obrazu (czytnik ekranu przeczyta go użytkownikowi); „obrazek" nic nie komunikuje, `title` nie zastępuje `alt`, a brak `alt` uniemożliwia osobom niewidomym poznanie zawartości obrazu.

## Pytanie 3

W tabeli HTML5 komórkę nagłówkową (dla kolumny lub wiersza) definiuje znacznik:

- A. `<td>`
- B. `<thead>`
- C. `<th>`
- D. `<caption>`

**Odpowiedź: C** — `th` to komórka nagłówkowa; `thead` grupuje wiersze nagłówka (nie jest komórką), `caption` nadaje tytuł całej tabeli, a `td` jest komórką danych.

## Pytanie 4

Który zapis pola formularza spowoduje, że przeglądarka sama sprawdzi format adresu e-mail przed wysłaniem?

- A. `<input type="text" name="email" validate>`
- B. `<input type="mail" name="email">`
- C. `<input type="email" name="email">`
- D. `<input type="text" name="email" format="email">`

**Odpowiedź: C** — `type="email"` to wbudowany typ pola z automatyczną walidacją formatu; typ `mail` oraz atrybuty `validate` i `format` nie istnieją w HTML5.

## Pytanie 5

Atrybut, po dodaniu którego przeglądarka zablokuje wysłanie formularza z pustym polem, to:

- A. `required`
- B. `checked`
- C. `placeholder`
- D. `readonly`

**Odpowiedź: A** — `required` czyni pole wymaganym: bez jego wypełnienia formularz nie zostanie wysłany; `checked` dotyczy zaznaczenia radio/checkbox, `placeholder` to podpowiedź widoczna w polu, a `readonly` blokuje edycję pola (nie wymusza jego wypełnienia).

## Pytanie 6 (zamienne — linki)

Link `<a href="https://przyklad.pl" target="_blank">Strona zewnętrzna</a>` otwiera się w nowej karcie. Który atrybut dodatkowo poprawia bezpieczeństwo?

- A. `secure="true"`
- B. `rel="noopener"`
- C. `hreflang="pl"`
- D. `target="_top"`

**Odpowiedź: B** — `rel="noopener"` odcina otwieraną stronę od dostępu do obiektu `window` strony otwierającej (ochrona przed tzw. tabnabbingiem); pozostałe atrybuty nie pełnią tej funkcji, a `target="_top"` wręcz nadpisze sposób otwarcia.

## Pytanie 7 (zamienne — formularze i a11y)

Aby kliknięcie etykiety „E-mail" uaktywniło pole `<input type="email" id="mail">`, znacznik `<label>` musi mieć atrybut:

- A. `name="mail"`
- B. `id="mail"`
- C. `for="mail"`
- D. `link="mail"`

**Odpowiedź: C** — atrybut `for` wiąże etykietę z polem o podanym `id`: klik w etykietę uaktywnia pole (i czytnik ekranu odczytuje etykietę przy polu); `name` nazywa dane wysyłane na serwer, a atrybut `link` nie istnieje.

---

## Klucz w skrócie

| Pytanie | 1 | 2 | 3 | 4 | 5 | 6 (zamienne) | 7 (zamienne) |
|---|---|---|---|---|---|---|---|
| Odpowiedź | B | B | C | C | A | B | C |

## Zgodność z zakresem kartkówki na 0103

| Obszar zakresu (wg scenariusza 0103) | Pokryte pytaniem |
|---|---|
| semantyczne znaczniki (co wybierasz: `article` czy `div`?) | 1 |
| typy `input` i dopasowanie do danych | 4 |
| `label` + a11y | 2, 7 |
| tabele | 3 |
| walidacja HTML5 (`required`, `pattern`, `min`/`max`) | 5 |
| dodatkowo: linki i `rel="noopener"` | 6 |

Do kartkówki na 0103 (10 min) weź 4–5 z powyższych (przetasowane) + 1–2 pytania otwarte, np.: „Napisz komplet pola formularza: etykieta «Telefon» powiązana z polem, do którego wolno wpisać tylko 9 cyfr" albo „Wymień trzy znaczniki semantyczne budujące szkielet strony i napisz jednym zdaniem, co ląduje w każdym z nich".
