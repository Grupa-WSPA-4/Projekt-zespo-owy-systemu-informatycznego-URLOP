# Słownik pojęć (Wersja 0.3)

Niniejszy słownik zawiera kluczowe pojęcia biznesowe, statusy, role oraz pojęcia techniczne systemu **URLOPY**, uzupełnione o synonimy, homonimy i źródła pozyskania wiedzy (w tym wnioski z wywiadu z klientem).

## 1. Pojęcia biznesowe i dziedzinowe

### 1. Wniosek urlopowy
* **Nazwa pojęcia:** Wniosek urlopowy
* **Definicja:** Dokument cyfrowy składany przez pracownika w systemie, zawierający prośbę o udzielenie dni wolnych od pracy w określonym przedziale czasowym.
* **Typy / Warianty:** Urlop wypoczynkowy, urlop na żądanie, urlop okolicznościowy.
* **Synonim:** Podanie o urlop
* **Homonim:** —
* **Źródło:** Wymagania wstępne / Wywiad 1
* **Aktorzy / Relacje:** Składany przez **Pracownika**, weryfikowany i zatwierdzany przez **Przełożonego**.

### 2. Limit urlopowy (Pula dni)
* **Nazwa pojęcia:** Limit urlopowy
* **Definicja:** Roczna liczba dni wolnych przysługujących pracownikowi na mocy Kodeksu Pracy lub umowy, od której odejmowane są dni zatwierdzonych urlopów.
* **Synonim:** Pula urlopowa, wymiar urlopu
* **Homonim:** —
* **Źródło:** Karta Projektu / Wywiad 1
* **Zasady biznesowe:** Liczba dni jest wprowadzana lub aktualizowana przez **Administratora / Kadry** na początku roku kalendarzowego.

### 3. Saldo urlopowe
* **Nazwa pojęcia:** Saldo urlopowe
* **Definicja:** Aktualny stan dni urlopowych pracownika wyrażony wzorem: $\text{Limit przysługujący} - \text{Dni wykorzystane} - \text{Dni zawnioskowane (oczekujące)}$.
* **Synonim:** Stan konta urlopowego
* **Homonim:** —
* **Źródło:** Analiza wymagań funkcjonalnych
* **Aktorzy / Relacje:** Widoczne dla **Pracownika**, **Przełożonego** oraz **Administratora / Kadr**.

### 4. Urlop na żądanie
* **Nazwa pojęcia:** Urlop na żądanie
* **Definicja:** Szczególna forma urlopu wypoczynkowego (maksymalnie 4 dni w roku kalendarzowym), zgłaszana w trybie natychmiastowym najpóźniej rano w dniu rozpoczęcia pracy.
* **Synonim:** Zgłoszenie rano / nagłe wolne
* **Homonim:** —
* **Źródło:** Wywiad 1 (U-04)
* **Zasady biznesowe:** Dni te są odejmowane z ogólnego limitu urlopu wypoczynkowego pracownika, a wniosek wymaga zatwierdzenia przez przełożonego w trybie priorytetowym.

### 5. Urlop okolicznościowy
* **Nazwa pojęcia:** Urlop okolicznościowy
* **Definicja:** Dodatkowe dni wolne przysługujące pracownikowi z tytułu szczególnych wydarzeń życiowych (np. ślub, narodziny dziecka, pogrzeb).
* **Synonim:** Wolne okolicznościowe
* **Homonim:** —
* **Źródło:** Standardy Kodeksu Pracy
* **Zasady biznesowe:** Nie pomniejsza podstawowej puli urlopu wypoczynkowego.

### 6. Kalendarz nieobecności
* **Nazwa pojęcia:** Kalendarz nieobecności
* **Definicja:** Moduł wizualny prezentujący harmonogram zatwierdzonych oraz planowanych urlopów w ujęciu zespołu lub całej firmy.
* **Synonim:** Grafik zespołu, harmonogram nieobecności
* **Homonim:** Plan urlopów (w firmowym żargonie oznaczający sztywne roczne plany)
* **Źródło:** Wywiad 1
* **Aktorzy / Relacje:** Używany przez **Przełożonego** i **Pracowników** do planowania pracy i zapobiegania nakładaniu się nieobecności.

### 7. Zastępstwo
* **Nazwa pojęcia:** Zastępstwo
* **Definicja:** Wskazanie innego pracownika, który przejmuje kluczowe obowiązki służbowe osoby przebywającej na urlopie w wybranym okresie.
* **Synonim:** Osoba zastępująca, zastępca
* **Homonim:** —
* **Źródło:** Wywiad 1 (U-03)
* **Zasady biznesowe:** Przy planowanym urlopie pracownik samodzielnie wyznacza zastępcę, natomiast w sytuacjach nagłych (np. L4) osobę wspierającą wskazuje przełożony.

### 8. Rok rozliczeniowy
* **Nazwa pojęcia:** Rok rozliczeniowy
* **Definicja:** Okres 12 miesięcy (zgodny z rokiem kalendarzowym), w którym naliczany i rozliczany jest przysługujący limit urlopowy.
* **Synonim:** Rok kalendarzowy
* **Homonim:** —
* **Źródło:** Karta Projektu

---

## 2. Statusy i cykl życia wniosku

### 9. Status: Oczekujący
* **Nazwa pojęcia:** Status: Oczekujący
* **Definicja:** Początkowy stan wniosku urlopowego tuż po złożeniu go przez pracownika. Wniosek oczekuje na decyzję przełożonego.
* **Synonim:** Do akceptacji / Nowy wniosek
* **Homonim:** —
* **Źródło:** Projekt systemowy

### 10. Status: Zatwierdzony
* **Nazwa pojęcia:** Status: Zatwierdzony
* **Definicja:** Stan wniosku zaakceptowanego przez przełożonego. Oznacza formalne udzielenie urlopu i automatyczne odjęcie dni z salda pracownika.
* **Synonim:** Zaakceptowany / Przyjęty
* **Homonim:** —
* **Źródło:** Projekt systemowy

### 11. Status: Odrzucony
* **Nazwa pojęcia:** Status: Odrzucony
* **Definicja:** Stan wniosku, który nie został zaakceptowany przez przełożonego (np. z powodu braku zastępstwa lub braku limitu dni).
* **Synonim:** Odrzucone podanie
* **Homonim:** —
* **Źródło:** Projekt systemowy

### 12. Status: Anulowany
* **Nazwa pojęcia:** Status: Anulowany
* **Definicja:** Stan wniosku wycofanego przez pracownika przed jego rozpoczęciem lub w wyniku nagłej rezygnacji, zatwierdzony przez kierownika w celu przywrócenia dni do salda.
* **Synonim:** Wycofany
* **Homonim:** —
* **Źródło:** Wywiad 1 (Rozstrzygnięcie Issue #12)

---

## 3. Aktorzy i uprawnienia (Systemowe)

### 13. Pracownik (Rola)
* **Nazwa pojęcia:** Pracownik
* **Definicja:** Podstawowa rola w systemie uprawniająca do składania wniosków, wyznaczania zastępców, podglądu własnego salda, historii oraz kalendarza zespołu.
* **Synonim:** Użytkownik podstawowy
* **Homonim:** —
* **Źródło:** Karta Projektu / Diagram Kontekstowy

### 14. Przełożony / Kierownik (Rola)
* **Nazwa pojęcia:** Przełożony / Kierownik
* **Definicja:** Rola uprawniająca do weryfikacji, akceptowania lub odrzucania wniosków złożonych przez podległych pracowników oraz podglądu grafiku zespołu.
* **Synonim:** Szef, Manager
* **Homonim:** Dziekan (w kontekście uczelnianym)
* **Źródło:** Karta Projektu / Wywiad 1

### 15. Administrator (Rola)
* **Nazwa pojęcia:** Administrator
* **Definicja:** Rola posiadająca pełne uprawnienia techniczne i organizacyjne w systemie: zarządzanie kontami użytkowników, przydzielanie ról oraz zarządzanie rocznymi limitami urlopowymi.
* **Synonim:** Admin / Kadry
* **Homonim:** —
* **Źródło:** Aktualizacja diagramu kontekstowego (Zgodność z zakresem IN)

---

## 4. Pojęcia techniczne i architektoniczne

### 16. Architektura trójwarstwowa
* **Nazwa pojęcia:** Architektura trójwarstwowa
* **Definicja:** Wzorzec podziału aplikacji na trzy niezależne warstwy: warstwę prezentacji (interfejs użytkownika), warstwę logiki biznesowej (serwer) oraz warstwę danych (baza danych).
* **Synonim:** 3-tier architecture
* **Homonim:** —
* **Źródło:** Karta Projektu

### 17. Interfejs programistyczny aplikacji (API)
* **Nazwa pojęcia:** Interfejs programistyczny aplikacji
* **Definicja:** Zbiór reguł i protokołów umożliwiający bezpieczną komunikację i wymianę danych pomiędzy interfejsem użytkownika a serwerem.
* **Synonim:** API
* **Homonim:** —
* **Źródło:** Dokumentacja architektoniczna

### 18. Encja bazy danych
* **Nazwa pojęcia:** Encja bazy danych
* **Definicja:** Obiekt w bazie danych reprezentujący kluczową strukturę informacji w systemie (np. Użytkownik, Wniosek Urlopowy, Limit Urlopowy).
* **Synonim:** Tabela / Model danych
* **Homonim:** —
* **Źródło:** Dokumentacja bazy danych

### 19. Walidacja biznesowa
* **Nazwa pojęcia:** Walidacja biznesowa
* **Definicja:** Logika po stronie serwera sprawdzająca poprawność wprowadzonych danych przed zapisem (np. czy data zakończenia nie jest wcześniejsza niż data rozpoczęcia, czy pracownik posiada wystarczającą liczbę dni w saldie).
* **Synonim:** Reguła walidacyjna
* **Homonim:** —
* **Źródło:** Wymagania niefunkcjonalne / biznesowe

### 20. Repozytorium kodu
* **Nazwa pojęcia:** Repozytorium kodu
* **Definicja:** Centralne miejsce przechowywania kodu źródłowego, historii zmian oraz dokumentacji projektu na platformie programistycznej (GitHub).
* **Synonim:** Repo / Git repository
* **Homonim:** —
* **Źródło:** ADR-001