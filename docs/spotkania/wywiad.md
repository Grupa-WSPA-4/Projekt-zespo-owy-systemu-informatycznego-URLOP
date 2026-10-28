# Wywiad 1 — System URLOPY

**Data:** 2026-11-04 · **Czas:** 15 min · **Forma:** wywiad krzyżowy (zajęcia 3)

## Uczestnicy

| Osoba | Rola w wywiadzie |
|---|---|
| Yevhenii (@mageka1s) | prowadzący rozmowę |
| Mukhammed (@kapeshonx) | protokolant |
| Yauheni (@HappyChoper) | obserwator słownika |
| Andrzej Kowalski (Kierownik Działu Administracji) | klient |

## Cel wywiadu
- poznać obecny sposób pracy i jego problemy z wnioskowaniem o urlopy,
- ustalić faktyczne role, uprawnienia i hierarchię akceptacji,
- zidentyfikować ukryte procesy i potencjalne wąskie gardła w firmie,
- uzyskać pełne odpowiedzi na otwarte pytania z fazy przygotowawczej.

## Ustalenia

| Nr | Ustalenie | Status |
|---|---|---|
| U-01 | Wnioski papierowe i mailowe powodują zagubienie dokumentów w szczycie urlopowym. | potwierdzone |
| U-02 | Kierownik działu ma zawsze ostateczne słowo, chyba że akurat sam choruje lub jest na urlopie. | potwierdzone (wymaga delegacji uprawnień) |
| U-03 | Zastępca musi być wyznaczony przed złożeniem wniosku, inaczej system nie przepuści dalej. | potwierdzone |
| U-04 | Urlop na żądanie nie wymaga wcześniejszego planowania, ale musi zostać zgłoszony systemowo najpóźniej w dniu rozpoczęcia pracy rano. | potwierdzone (rozstrzygnięcie Issue #11) |
| U-05 | W przypadku nagłych nieobecności (np. nagłe L4 lub pilne sprawy rodzinne), pracownik informuje szefa telefonicznie, a wniosek systemowy uzupełnia wstecznie HR lub sam pracownik po powrocie. | potwierdzone (rozstrzygnięcie Issue #12) |

## Cytaty klienta (dosłownie)

1. > „Wysyłam maila z wnioskiem do szefa, a on zapomina, bo ma 50 innych wiadomości dziennie.”
2. > „Skąd mam wiedzieć, kto zastępuje koleżankę, skoro nikt tego nigdzie nie zapisuje?”
3. > „Jak komuś coś wyskoczy rano w domu, to dzwoni do mnie lub pisze na czacie, a formalnościami zajmujemy się później.”

## Nowe terminy

| Słowo klienta | Znaczenie wg klienta | Synonim / homonim? | W słowniku jako |
|---|---|---|---|
| zastępca | osoba przejmująca obowiązki podczas nieobecności | synonim | Osoba zastępująca |
| plan urlopów | roczne, sztywne rozpisanie urlopów w grudniu | homonim | Harmonogram zespołu |
| zgłoszenie rano | informacja o nagłej nieobecności w dniu jej wystąpienia | synonim | Urlop na żądanie / nagłe zwolnienie |

## Sprzeczności

| Wypowiedź A | Wypowiedź B | Jak rozstrzygnąć? |
|---|---|---|
| „Pracownik sam szuka zastępcy na własną rękę.” (U-05) | „Szef narzutas, kto ma kogo zastępować w razie nagłego L4.” (U-06) | Rozstrzygnięto w Issue #12: Pracownik wyznacza zastępcę przy planowanym urlopie, natomiast przy nagłych sytuacjach awaryjnych przełożony wskazuje osobę wspierającą. |

## Otwarte pytania i odpowiedzi

| Nr | Pytanie | Issue | Odpowiedź (po uzyskaniu) |
|---|---|---|---|
| Q-01 | Czy urlop na żądanie wymaga formalnego zatwierdzenia przez kierownika w systemie? | #11 | **Tak, ale ma status natychmiastowego powiadomienia.** Kierownik zatwierdza go ex post lub w trybie priorytetowym, aby system poprawnie odliczył dni z puli urlopów na żądanie. |
| Q-02 | Co się dzieje w przypadku nagłej rezygnacji z urlopu przez pracownika po jego zatwierdzeniu? | #12 | Pracownik wysyła w systemie prośbę o anulowanie urlopu, którą kierownik musi jednym kliknięciem zatwierdzić, aby przywrócić dni do salda. |

## Wnioski zespołu
- Zaskoczyło nas, jak duża część komunikacji urlopowej opiera się obecnie na prywatnych wiadomościach i ustnych ustaleniach w sytuacjach nagłych.
- Warto uwzględnić w systemie prosty mechanizm "anulowania zatwierdzonego wniosku" oraz szybkiego raportowania nagłych nieobecności (np. urlop na żądanie).
- Wywiad w pełni pokrył kluczowe obszary biznesowe i dostarczył twardych wytycznych do stworzenia przypadków użycia (Use Cases).