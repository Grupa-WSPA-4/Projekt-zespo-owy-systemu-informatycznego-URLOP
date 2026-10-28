# Wymagania

## Potrzeby (z wywiadu 1)

| ID | Potrzeba | Źródło / cytat | Typ | Kto zgłasza |
|---|---|---|---|---|
| N-01 | Pracownik chce w jednym czytelnym miejscu sprawdzić swoje saldo urlopowe oraz kalendarz zespołu przed złożeniem wniosku. | wywiad-1, ustalenie U-01 | potrzeba | Pracownik |
| N-02 | System nie może dopuścić do sytuacji, w której wniosek zostanie złożony bez wyznaczonego i zaakceptowanego zastępcy (w przypadku planowanych urlopów). | wywiad-1, ustalenie U-03 | żądanie | Przełożony |
| N-03 | „Wysyłanie maila z wnioskiem i czekanie na odpowiedź w morzu wiadomości” → potrzeba: cyfrowy przepływ wniosków z powiadomieniami w czasie rzeczywistym i szybką akceptacją przez przełożonego. | wywiad-1, cytat 1: „Wysyłam maila z wnioskiem do szefa, a on zapomina...” | rozwiązanie | Pracownik |
| N-04 | Urlop na żądanie w nagłych wypadkach musi zostać zgłoszony rano w dniu rozpoczęcia pracy, z natychmiastowym powiadomieniem przełożonego (zatwierdzenie ex post). | wywiad-1, ustalenie U-04 | żądanie | Pracownik |
| N-05 | Pracownik potrzebuje możliwości zgłoszenia urlopu cyklicznego lub dłuższego wyprzedzenia planów urlopowych bez wielokrotnego powtarzania ręcznych czynności. | wywiad-1, ustalenie U-03 | potrzeba | Pracownik |
| N-06 | Dni wolne nie mogą przekraczać ustawowego rocznego limitu, a system musi automatycznie weryfikować poprawność salda przed przepuszczeniem wniosku. | Karta Projektu / przepisy | potrzeba (ukryta) | Administrator |
| N-07 | Pracownik chce mieć możliwość samodzielnego złożenia prośby o anulowanie zatwierdzonego wniosku urlopowego, bez konieczności pisania osobnych maili do kadr. | wywiad-1, rozstrzygnięcie Issue #12 | potrzeba | Pracownik |

---

## Wymagania Funkcjonalne (FR)

| ID | Nazwa / Opis wymagania | Powiązane potrzeby |
|---|---|---|
| **FR-01** | System musi umożliwiać użytkownikom logowanie i uwierzytelnianie z podziałem na role (Pracownik, Kierownik, Administrator). | N-01, N-06 |
| **FR-02** | System musi udostępniać pracownikowi panel podglądu bieżącego salda urlopowego (dni przysługujące, wykorzystane, pozostałe). | N-01, N-03 |
| **FR-03** | System musi umożliwiać pracownikowi składanie wniosku urlopowego z wyborem typu (wypoczynkowy, na żądanie, okolicznościowy) oraz przedziału dat. | N-01, N-03, N-05 |
| **FR-04** | System musi wymuszać wskazanie pracownika zastępującego przy składaniu planowanego wniosku urlopowego. | N-02, N-05 |
| **FR-05** | System musi automatycznie weryfikować po stronie serwera, czy pracownik posiada wystarczającą liczbę dni w saldie przed zapisaniem wniosku. | N-06 |
| **FR-06** | System musi przesyłać powiadomienia e-mail do przełożonego o nowo złożonym wniosku urlopowym. | N-03 |
| **FR-07** | System musi umożliwiać kierownikowi przeglądanie listy wniosków podległych pracowników wraz z informacją o zastępstwach. | N-02, N-03 |
| **FR-08** | System musi umożliwiać kierownikowi zatwierdzenie lub odzyskanie/odrzucenie wniosku urlopowego ze zmianą jego statusu. | N-03 |
| **FR-09** | System musi automatycznie pomniejszać saldo urlopowe pracownika w momencie pozytywnego zatwierdzenia wniosku przez kierownika. | N-06 |
| **FR-10** | System musi udostępniać kalendarz nieobecności w ujęciu zespołowym i firmowym dla uprawnionych użytkowników. | N-01, N-03 |
| **FR-11** | System musi obsługiwać tryb zgłaszania urlopu na żądanie w dniu jego wystąpienia z powiadomieniem priorytetowym dla kierownika. | N-04 |
| **FR-12** | System musi umożliwiać pracownikowi wysłanie prośby o anulowanie zatwierdzonego wniosku, wymagającą akceptacji kierownika. | N-07 |
| **FR-13** | System musi umożliwiać administratorowi zarządzanie kontami użytkowników i strukturą organizacyjną firmy. | N-06 |
| **FR-14** | System musi umożliwiać administratorowi/kadrom wprowadzanie oraz aktualizowanie rocznych limitów urlopowych dla pracowników. | N-06 |
| **FR-15** | System musi generować podstawowe raporty i zestawienia nieobecności oraz historii urlopów w firmie. | N-01, N-03 |

---

## Wymagania Niefunkcjonalne (NFR)

| ID | Nazwa / Opis wymagania | Powiązane potrzeby |
|---|---|---|
| **NFR-01** | **Wydajność:** Czas ładowania głównych widoków (kalendarz, saldo, lista wniosków) nie powinien przekraczać 2 sekund przy standardowym obciążeniu. | N-01, N-03 |
| **NFR-02** | **Bezpieczeństwo danych:** Wszystkie hasła użytkowników muszą być szyfrowane przy użyciu silnych algorytmów haszujących (np. bcrypt), a transmisja danych musi odbywać się przez protokół HTTPS. | N-01, N-06 |
| **NFR-03** | **Dostępność i Responsywność (UX):** Interfejs systemu (UI) musi być w pełni responsywny i poprawnie działać na urządzeniach mobilnych (smartfony, tablety) oraz komputerach. | N-01, N-03, N-04 |
| **NFR-04** | **Niezawodność:** Baza danych systemu musi posiadać mechanizm regularnych kopii zapasowych (backupów) wykonywanych co najmniej raz dziennie. | N-06 |
| **NFR-05** | **Użyteczność:** Formularz składania wniosku urlopowego musi być intuicyjny i wymagać maksymalnie 3 kliknięć od otwarcia strony do przesłania zgłoszenia. | N-03, N-05 |
| **NFR-06** | **Skalowabilidad:** Architektura systemowa musi umożliwiać bezproblemową rozbudowę o nowe role lub działy firmy bez konieczności przebudowy struktury bazy danych. | N-06 |
| **NFR-07** | **Zgodność z prawem (Compliance):** System musi uwzględniać polskie przepisy Kodeksu Pracy w zakresie naliczania limitów, urlopów na żądanie oraz rocznych rozliczeń. | N-06 |
| **NFR-08** | **Utrzymaniowalność:** Kod źródłowy projektu musi być w pełni udokumentowany, a wersjonowanie zmian prowadzite w repozytorium GitHub zgodnie z przyjętymi standardami (ADR). | N-01 |