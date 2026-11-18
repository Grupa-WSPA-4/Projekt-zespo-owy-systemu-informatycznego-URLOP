# Macierz śledzenia

**Wersja:** 0.1

| Potrzeba | Wymaganie | Historyjka | Priorytet |
|---|---|---|---|
| N-01 | FR-02 Podgląd salda urlopowego i historii | US-01 | Must |
| N-01 | FR-10 Dostęp do kalendarza nieobecności | US-02 | Must |
| N-01 | NFR-01 Wydajność głównych widoków (< 2 s) | US-01, US-02 (kryterium) | Must |
| N-02 | FR-04 Wymuszenie wskazania zastępcy | US-03 | Must |
| N-02 | FR-07 Przegląd zastępstw przez kierownika | US-04 | Must |
| N-03 | FR-03 Składanie wniosku urlopowego | US-05 | Must |
| N-03 | FR-06 Powiadomienia e-mail dla przełożonego | US-05 (kryterium) | Must |
| N-03 | FR-08 Akceptacja lub odrzucenie wniosku | US-06 | Must |
| N-04 | FR-11 Obsługa trybu urlopu na żądanie | US-08 | Must |
| N-05 | FR-03 Składanie wniosku (z wyprzedzeniem) | US-05 | Must |
| N-06 | FR-05 Automatyczna weryfikacja salda | US-05 (kryterium) | Must |
| N-06 | FR-09 Automatyczne pomniejszenie salda | US-06 (kryterium) | Must |
| N-06 | FR-13 Zarządzanie kontami i strukturą | US-09 | Must |
| N-06 | FR-14 Zarządzanie rocznymi limitami | US-10 | Must |
| N-06 | NFR-07 Zgodność z Kodeksem Pracy | przekrojowe | Must |
| N-07 | FR-12 Anulowanie zatwierdzonego wniosku | US-07 | Must |



| ID | Wymaganie Funkcjonalne (FR) | Proces |
|---|---|---|
| **FR-01** | Pracownik wybiera datę od-do i składa wniosek urlopowy. | **Proces wnioskowania o urlop** |
| **FR-02** | System weryfikuje dostępny limit dni wolnych pracownika. | **Proces wnioskowania o urlop** |
| **FR-03** | System blokuje wniosek przy niewystarczającym limicie dni. | **Proces wnioskowania o urlop** |
| **FR-04** | Pracownik podgląda status swojego wniosku (oczekujący/odrzucony). | **Proces wnioskowania o urlop** |
| **FR-05** | Przełożony przegląda listę oczekujących wniosków swojego zespołu. | **Proces akceptacji urlopów** |
| **FR-06** | Przełożony akceptuje lub odrzuca wniosek pracownika. | **Proces akceptacji urlopów** |
| **FR-07** | System aktualizuje pulę dni wolnych po akceptacji wniosku. | **Proces akceptacji urlopów** |
| **FR-08** | System wyświetla zatwierdzone urlopy zespołu w kalendarzu. | **Proces monitorowania nieobecności** |
