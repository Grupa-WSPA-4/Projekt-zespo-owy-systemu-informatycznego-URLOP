# Aktorzy i kandydaci na przypadki użycia (Use Cases) – System URLOPY

Dokument zawiera zestawienie aktorów oraz kandydatów na przypadki użycia wyprowadzonych bezpośrednio z historyjek użytkownika (`US-01` – `US-08`) zapisanych w backlogu produktu.

---

## 1. Lista aktorów systemu

| Aktor | Typ aktora | Rola i opis w systemie |
| :--- | :--- | :--- |
| **Pracownik** | Główny (ludzki) | Podstawowy użytkownik systemu. Składa wnioski urlopowe (zwykłe oraz na żądanie), wskazuje zastępcę, sprawdza swoje saldo dni wolnych oraz przegląda kalendarz nieobecności zespołu. |
| **Przełożony** | Główny (ludzki) | Kierownik zespołu lub manager. Rozpatruje wnioski urlopowe podwładnych (akceptuje lub odrzuca), weryfikuje zastępstwa oraz monitoruje dostępność pracowników w kalendarzu. |
| **Administrator** | Główny (ludzki) | Osoba zarządzająca stroną techniczną i organizacyjną systemu. Tworzy konta użytkowników, przypisuje strukturę zespołów oraz definiuje roczne pule dni urlopowych. |
| **Kadry (HR)** | Główny (ludzki) | Przedstawiciel działu kadr i płac. Generuje zaawansowane raporty nieobecności pracowników na potrzeby rozliczeń i ewidencji czasu pracy. |

---

## 2. Kandydaci na przypadki użycia (z historyjek)

| ID | Kandydat na przypadek użycia | Główny aktor | Źródło (Historyjka / FR) | Cel biznesowy |
| :--- | :--- | :--- | :--- | :--- |
| **UC-01** | Podgląd salda i historii urlopów | Pracownik | `US-01` (`FR-02`, `FR-15`) | Umożliwienie pracownikowi szybkiego sprawdzenia liczby dostępnych dni urlopowych oraz historii wykorzystanych wolnych. |
| **UC-02** | Przegląd kalendarza nieobecności zespołu | Pracownik, Przełożony | `US-02` (`FR-10`) | Zapewnienie przejrzystego wglądu w zaplanowane i zatwierdzone urlopy w zespole w celu uniknięcia konfliktów terminów. |
| **UC-03** | Złożenie wniosku urlopowego ze wskazaniem zastępcy | Pracownik | `US-03` (`FR-03`, `FR-04`, `FR-05`) | Cyfrowe zgłoszenie planowanego urlopu wraz z automatyczną weryfikacją limitu dni oraz wyznaczeniem osoby zastępującej. |
| **UC-04** | Zgłoszenie urlopu na żądanie | Pracownik | `US-05` (`FR-11`) | Szybkie zgłoszenie nagłej nieobecności w trybie natychmiastowym z uwzględnieniem ustawowego limitu 4 dni w roku. |
| **UC-05** | Anulowanie zatwierdzonego wniosku urlopowego | Pracownik | `US-06` (`FR-12`) | Wycofanie zaakceptowanego wcześniej urlopu (przed jego rozpoczęciem) i automatyczny zwrot dni do puli pracownika. |
| **UC-06** | Rozpatrzenie wniosku urlopowego (akceptacja / odrzucenie) | Przełożony | `US-04` (`FR-07`, `FR-08`, `FR-09`) | Podjęcie decyzji w sprawie wniosku pracownika, przegląd zastępstw oraz automatyczne pomniejszenie salda po akceptacji. |
| **UC-07** | Zarządzanie kontami i rocznymi limitami urlopowymi | Administrator | `US-07` (`FR-13`, `FR-14`) | Utrzymanie aktualnej bazy pracowników, przypisanie ich do przełożonych oraz konfiguracja przysługujących wymiarów urlopu. |
| **UC-08** | Generowanie raportów nieobecności | Kadry (HR) | `US-08` (`FR-15`) | Eksport zestawień wykorzystanych i zaplanowanych urlopów dla potrzeb działu kadr i księgowości. |