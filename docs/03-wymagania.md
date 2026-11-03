# Wymagania — System URLOPY

**Wersja:** 0.2  
**Data:** 2026-11-03  
**Autorzy:** Zespół projektowy URLOPY (Yevhenii, Mukhammed, Yauheni, Andrii, Aldiyar)

## 1. Potrzeby

| ID | Potrzeba (językiem klienta) | Kto zgłosił | Źródło |
|---|---|---|---|
| N-01 | Pracownik chce w jednym czytelnym miejscu sprawdzić swoje saldo urlopowe oraz kalendarz zespołu przed złożeniem wniosku. | Pracownik | wywiad-1, ustalenie U-01 |
| N-02 | System nie może dopuścić do sytuacji, w której wniosek zostanie złożony bez wyznaczonego i zaakceptowanego zastępcy (w przypadku planowanych urlopów). | Przełożony | wywiad-1, ustalenie U-03 |
| N-03 | „Wysyłanie maila z wnioskiem i czekanie na odpowiedź w morzu wiadomości” → potrzeba: cyfrowy przepływ wniosków z powiadomieniami w czasie rzeczywistym i szybką akceptacją przez przełożonego. | Pracownik | wywiad-1, cytat 1: „Wysyłam maila z wnioskiem do szefa, a on zapomina...” |
| N-04 | Urlop na żądanie w nagłych wypadkach musi zostać zgłoszony rano w dniu rozpoczęcia pracy, z natychmiastowym powiadomieniem przełożonego (zatwierdzenie ex post). | Pracownik | wywiad-1, ustalenie U-04 |
| N-05 | Pracownik potrzebuje możliwości zgłoszenia urlopu cyklicznego lub dłuższego wyprzedzenia planów urlopowych bez wielokrotnego powtarzania ręcznych czynności. | Pracownik | wywiad-1, ustalenie U-03 |
| N-06 | Dni wolne nie mogą przekraczać ustawowego rocznego limitu, a system musi automatycznie weryfikować poprawność salda przed przepuszczeniem wniosku. | Administrator | Karta Projektu / przepisy |
| N-07 | Pracownik chce mieć możliwość samodzielnego złożenia prośby o anulowanie zatwierdzonego wniosku urlopowego, bez konieczności pisania osobnych maili do kadr. | Pracownik | wywiad-1, rozstrzygnięcie Issue #12 |

## 2. Wymagania funkcjonalne (FR)

| ID | Treść | Źródło | Priorytet (MoSCoW) | Uwagi |
|---|---|---|---|---|
| FR-01 | System musi umożliwiać użytkownikom logowanie i uwierzytelnianie z podziałem na role (Pracownik, Kierownik, Administrator). | N-01, N-06 | **Must** | Podział uprawnień |
| FR-02 | System musi udostępniać pracownikowi panel podglądu bieżącego salda urlopowego (dni przysługujące, wykorzystane, pozostałe). | N-01, N-03 | **Must** | Widoczne po zalogowaniu |
| FR-03 | System musi umożliwiać pracownikowi składanie wniosku urlopowego z wyborem typu (wypoczynkowy, na żądanie, okolicznościowy) oraz przedziału dat. | N-01, N-03, N-05 | **Must** | Formularz wniosku |
| FR-04 | System musi wymuszać wskazanie pracownika zastępującego przy składaniu planowanego wniosku urlopowego. | N-02, N-05 | **Must** | Pole obowiązkowe |
| FR-05 | System musi automatycznie weryfikować po stronie serwera, czy pracownik posiada wystarczającą liczbę dni w saldie przed zapisaniem wniosku. | N-06 | **Must** | Walidacja biznesowa |
| FR-06 | System musi przesyłać powiadomienia e-mail do przełożonego o nowo złożonym wniosku urlopowym. | N-03 | **Must** | Serwer pocztowy |
| FR-07 | System musi umożliwiać kierownikowi przeglądanie listy wniosków podległych pracowników wraz z informacją o zastępstwach. | N-02, N-03 | **Must** | Panel kierownika |
| FR-08 | System musi umożliwiać kierownikowi zatwierdzenie lub odrzucenie wniosku urlopowego ze zmianą jego statusu. | N-03 | **Must** | Akceptacja / Odrzucenie |
| FR-09 | System musi automatycznie pomniejszać saldo urlopowe pracownika w momencie pozytywnego zatwierdzenia wniosku przez kierownika. | N-06 | **Must** | Aktualizacja salda |
| FR-10 | System musi udostępniać kalendarz nieobecności w ujęciu zespołowym i firmowym dla uprawnionych użytkowników. | N-01, N-03 | **Must** | Widok kalendarza |
| FR-11 | System musi obsługiwać tryb zgłaszania urlopu na żądanie w dniu jego wystąpienia z powiadomieniem priorytetowym dla kierownika. | N-04 | **Must** | Tryb natychmiastowy |
| FR-12 | System musi umożliwiać pracownikowi wysłanie prośby o anulowanie zatwierdzonego wniosku, wymagającą akceptacji kierownika. | N-07 | **Must** | Anulowanie wniosku |
| FR-13 | System musi umożliwiać administratorowi zarządzanie kontami użytkowników i strukturą organizacyjną firmy. | N-06 | **Must** | Panel administratora |
| FR-14 | System musi umożliwiać administratorowi/kadrom wprowadzanie oraz aktualizowanie rocznych limitów urlopowych dla pracowników. | N-06 | **Must** | Zarządzanie limitami |
| FR-15 | System musi generować podstawowe raporty i zestawienia nieobecności oraz historii urlopów w firmie. | N-01, N-03 | **Should** | Raporty kadrowe |

## 3. Wymagania niefunkcjonalne (NFR) — wg ISO/IEC 25010

| ID | Kategoria (ISO/IEC 25010) | Treść (mierzalna) | Źródło | Priorytet | Uwagi (sposób sprawdzenia) |
|---|---|---|---|---|---|
| NFR-01 | Wydajność (Performance Efficiency) | Czas ładowania głównych widoków (kalendarz, saldo, lista wniosków) nie powinien przekraczać 2 sekund przy standardowym obciążeniu. | N-01, N-03 | **Must** | test obciążeniowy |
| NFR-02 | Bezpieczeństwo (Security) | Wszystkie hasła użytkowników muszą być szyfrowane algorytmem bcrypt, a transmisja danych odbywać się przez HTTPS. | N-01, N-06 | **Must** | audyt bezpieczeństwa |
| NFR-03 | Użyteczność / Kompatybilność (Usability) | Interfejs systemu (UI) musi być w pełni responsywny i poprawnie działać na urządzeniach mobilnych oraz komputerach. | N-01, N-03, N-04 | **Must** | testy na urządzeniach mobilnych |
| NFR-04 | Niezawodność (Reliability) | Baza danych systemu musi posiadać mechanizm regularnych kopii zapasowych (backupów) wykonywanych co najmniej raz dziennie. | N-06 | **Must** | weryfikacja harmonogramu backupów |
| NFR-05 | Użyteczność (Usability) | Formularz składania wniosku urlopowego musi być intuicyjny i wymagać maksymalnie 3 kliknięć od otwarcia strony do przesłania zgłoszenia. | N-03, N-05 | **Should** | testy użyteczności (UX) |
| NFR-06 | Skalowabilidad (Maintainability) | Architektura systemowa musi umożliwiać bezproblemową rozbudowę o nowe role lub działy firmy bez przebudowy bazy danych. | N-06 | **Should** | przegląd architektury |
| NFR-07 | Zgodność (Compatibility / Compliance) | System musi uwzględniać polskie przepisy Kodeksu Pracy w zakresie naliczania limitów, urlopów na żądanie oraz rocznych rozliczeń. | N-06 | **Must** | weryfikacja prawna |
| NFR-08 | Utrzymaniowalność (Maintainability) | Kod źródłowy projektu musi być w pełni udokumentowany, a wersjonowanie zmian prowadzone w repozytorium GitHub zgodnie z ADR. | N-01 | **Must** | przegląd repozytorium |

## 4. Reguły biznesowe (BR)

| ID | Reguła | Źródło | Uwagi (których FR dotyczy) |
|---|---|---|---|
| **BR-01** | Suma dni wykorzystanych i zawnioskowanych nie może przekraczać przysługującego rocznego limitu urlopowego pracownika. | N-06 | FR-05, FR-09 |
| **BR-02** | Wniosek urlopowy o charakterze planowanym musi zawierać wskazane i zaakceptowane zastępstwo. | N-02 | FR-04, FR-07 |
| **BR-03** | Urlop na żądanie pomniejsza pulę urlopu wypoczynkowego i może być zgłoszony maksymalnie do 4 dni w roku kalendarzowym. | N-04 | FR-03, FR-11 |
| **BR-04** | Anulowanie zatwierdzonego wniosku wymaga ponownej akceptacji przez przełożonego w celu przywrócenia dni do salda pracownika. | N-07 | FR-12 |
| **BR-05** | Wniosek o urlop na żądanie musi zostać złożony najpóźniej w dniu rozpoczęcia pracy rano, przed godziną rozpoczęcia obowiązków. | N-04 | FR-11 |

## 5. Ograniczenia

- **Ograniczenie technologiczne:** Wykorzystanie architektury trójwarstwowej oraz relacyjnej bazy danych (uzasadnienie: łatwość modelowania relacji użytkowników i wniosków).
- **Ograniczenie dziedzinowe:** Brak obsługi zwolnień lekarskich (L4), delegacji oraz list płac (uzasadnienie: przyjęty i zamknięty zakres OUT projektu).
- **Ograniczenie zasobów:** Prace zespołu realizowane są w ramach projektu akademickiego (uzasadnienie: wykorzystanie wyłącznie darmowych narzędzi open-source).

## 6. Historyjki użytkownika (dla wymagających „Must”)

### US-01: Podgląd salda i historii urlopów
**Jako** Pracownik, **chcę** widzieć moje aktualne saldo urlopowe oraz historię złożonych wniosków, **aby** wiedzieć, ile dni wolnych mogę jeszcze zaplanować.  
Wymagania: FR-01, FR-02, FR-15, NFR-01, NFR-03 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Pomyślne wyświetlenie salda**
  - **Given** pracownik jest zalogowany w systemie,
  - **When** przechodzi do zakładki „Moje saldo”,
  - **Then** widzi liczbę dni przysługujących, wykorzystanych oraz pozostałych do końca roku.
- **Scenariusz 2: Prędkość ładowania widoku**
  - **Given** baza danych zawiera historię wniosków użytkownika,
  - **When** użytkownik otwiera panel salda,
  - **Then** widok ładuje się w czasie poniżej 2 sekund.

### US-02: Przegląd kalendarza nieobecności
**Jako** Kierownik, **chcę** widzieć kalendarz nieobecności mojego zespołu, **aby** kontrolować obsadę i zapobiegać nakładaniu się urlopów.  
Wymagania: FR-01, FR-10, NFR-01, NFR-03 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Wyświetlenie grafiku zespołu**
  - **Given** kierownik jest zalogowany i wybiera widok kalendarza nieobecności,
  - **When** wskazuje bieżący miesiąc,
  - **Then** system prezentuje zatwierdzone urlopy wszystkich podwładnych w czytelnej formie siatki.

### US-03: Składanie wniosku urlopowego z zastępcą
**Jako** Pracownik, **chcę** złożyć wniosek urlopowy ze wskazaniem osoby zastępującej, **aby** formalnie zgłosić planowaną nieobecność.  
Wymagania: FR-03, FR-04, FR-05, BR-02 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Poprawne złożenie wniosku z zastępcą**
  - **Given** pracownik ma wystarczające saldo i wyznaczył pracownika zastępującego,
  - **When** wypełnia formularz wniosku i kliknie „Wyślij”,
  - **Then** wniosek trafia do przełożonego ze statusem „Oczekujący”.
- **Scenariusz 2: Blokada braku zastępstwa**
  - **Given** pracownik próbuje złożyć wniosek planowany bez wyboru zastępcy,
  - **When** klika przycisk wysłania wniosku,
  - **Then** system wyświetla komunikat o błędzie i uniemożliwia zapisanie wniosku.

### US-04: Zatwierdzanie wniosków przez przełożonego
**Jako** Kierownik, **chcę** akceptować lub odrzucać wnioski urlopowe podwładnych, **aby** zarządzać czasem pracy zespołu.  
Wymagania: FR-07, FR-08, FR-09, BR-01 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Zatwierdzenie wniosku i aktualizacja salda**
  - **Given** kierownik ma oczekujący wniosek na liście zadań,
  - **When** klika „Zatwierdź”,
  - **Then** status wniosku zmienia się na „Zatwierdzony”, a saldo pracownika zostaje automatycznie pomniejszone.

### US-05: Obsługa urlopu na żądanie
**Jako** Pracownik, **chcę** zgłosić urlop na żądanie w trybie nagłym, **aby** poinformować pracodawcę o nieobecności w dniu jej wystąpienia.  
Wymagania: FR-03, FR-11, BR-03, BR-05 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Zgłoszenie rano w dniu pracy**
  - **Given** pracownik znajduje się w sytuacji nagłej i otwiera system rano,
  - **When** wybiera typ „Urlop na żądanie” i wysyła zgłoszenie,
  - **Then** system wysyła powiadomienie priorytetowe do kierownika, a wniosek trafia do akceptacji ex post.

### US-06: Anulowanie zatwierdzonego wniosku
**Jako** Pracownik, **chcę** poprosić o anulowanie zatwierdzonego wniosku urlopowego, **aby** odzyskać dni urlopowe w razie zmiany planów.  
Wymagania: FR-12, BR-04 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Wysłanie prośby o anulowanie**
  - **Given** pracownik posiada zatwierdzony wniosek, którego data jeszcze się nie rozpoczęła,
  - **When** wybiera opcję „Anuluj wniosek” i zatwierdza wybór,
  - **Then** wniosek zmienia status na oczekujący na anulowanie przez kierownika.

### US-07: Zarządzanie kontami i limitami przez administratora
**Jako** Administrator, **chcę** zarządzać kontami użytkowników oraz rocznymi limitami urlopowymi, **aby** utrzymać aktualność danych w systemie.  
Wymagania: FR-13, FR-14, NFR-02 · Priorytet: **Must**

Kryteria akceptacji:
- **Scenariusz 1: Zmiana limitu urlopowego pracownika**
  - **Given** administrator jest zalogowany w panelu administracyjnym,
  - **When** edytuje profil pracownika i zmienia roczny limit dni,
  - **Then** nowe saldo zostaje zapisane w bazie danych.

## 7. Pytania otwarte

| Nr | Pytanie | Do kogo | Issue | Status |
|---|---|---|---|---|
| Q-01 | Czy urlop na żądanie wymaga formalnego zatwierdzenia przez kierownika w systemie? | Klient / Kierownik Kadr | #11 | Rozstrzygnięto (Tak, zatwierdzenie ex post) |
| Q-02 | Co się dzieje w przypadku nagłej rezygnacji z urlopu przez pracownika po jego zatwierdzeniu? | Klient | #12 | Rozstrzygnięto (Wniosek o anulowanie i akceptacja kierownika) |