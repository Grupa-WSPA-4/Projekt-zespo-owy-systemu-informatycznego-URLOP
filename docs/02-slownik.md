# Słownik pojęć

## 1. Pojęcia biznesowe i dziedzinowe

### 1. Wniosek urlopowy

* **Nazwa pojęcia:** Wniosek urlopowy

* **Definicja:** Dokument cyfrowy składany przez pracownika w systemie, zawierający prośbę o udzielenie dni wolnych od pracy w określonym przedziale czasowym.

* **Typy / Warianty:** Urlop wypoczynkowy, urlop na żądanie, urlop okolicznościowy.

* **Aktorzy / Relacje:** Składany przez **Pracownika**, weryfikowany i zatwierdzany przez **Przełożonego**.

### 2. Limit urlopowy (Pula dni)

* **Nazwa pojęcia:** Limit urlopowy

* **Definicja:** Roczna liczba dni wolnych przysługujących pracownikowi na mocy Kodeksu Pracy lub umowy, od której odejmowane są dni zatwierdzonych urlopów.

* **Zasady biznesowe:** Liczba dni jest wprowadzana lub aktualizowana przez **Kadr / Administratora** na początku roku kalendarzowego.

### 3. Saldo urlopowe

* **Nazwa pojęcia:** Saldo urlopowe

* **Definicja:** Aktualny stan dni urlopowych pracownika wyrażony wzorem: $\text{Limit przysługujący} - \text{Dni wykorzystane} - \text{Dni zawnioskowane (oczekujące)}$.

* **Aktorzy / Relacje:** Widoczne dla **Pracownika**, **Przełożonego** oraz **Kadr**.

### 4. Urlop na żądanie

* **Nazwa pojęcia:** Urlop na żądanie

* **Definicja:** Szczególna forma urlopu wypoczynkowego (maksymalnie 4 dni w roku kalendarzowym), zgłaszana w trybie natychmiastowym.

* **Zasady biznesowe:** Dni te są odejmowane z ogólnego limitu urlopu wypoczynkowego pracownika.

### 5. Urlop okolicznościowy

* **Nazwa pojęcia:** Urlop okolicznościowy

* **Definicja:** Dodatkowe dni wolne przysługujące pracownikowi z tytułu szczególnych wydarzeń życiowych (np. ślub, narodziny dziecka, pogrzeb).

* **Zasady biznesowe:** Nie pomniejsza podstawowej puli urlopu wypoczynkowego.

### 6. Kalendarz nieobecności

* **Nazwa pojęcia:** Kalendarz nieobecności

* **Definicja:** Moduł wizualny prezentujący harmonogram zatwierdzonych oraz planowanych urlopów w ujęciu zespołu lub całej firmy.

* **Aktorzy / Relacje:** Używany przez **Przełożonego** do planowania pracy i zapobiegania nakładaniu się nieobecności.

### 7. Zastępstwo

* **Nazwa pojęcia:** Zastępstwo

* **Definicja:** Wskazanie innego pracownika, który przejmuje obowiązki służbowe osoby przebywającej na urlopie w wybranym okresie.

### 8. Rok rozliczeniowy

* **Nazwa pojęcia:** Rok rozliczeniowy

* **Definicja:** Okres 12 miesięcy (zgodny z rokiem kalendarzowym), w którym naliczany i rozliczany jest przysługujący limit urlopowy.

## 2. Statusy i cykl życia wniosku

### 9. Status: Oczekujący

* **Nazwa pojęcia:** Status: Oczekujący

* **Definicja:** Początkowy stan wniosku urlopowego tuż po złożeniu go przez pracownika. Wniosek oczekuje na decyzję przełożonego.

### 10. Status: Zatwierdzony

* **Nazwa pojęcia:** Status: Zatwierdzony

* **Definicja:** Stan wniosku zaakceptowanego przez przełożonego. Oznacza formalne udzielenie urlopu i automatyczne odjęcie dni z salda pracownika.

### 11. Status: Odrzucony

* **Nazwa pojęcia:** Status: Odrzucony

* **Definicja:** Stan wniosku, który nie został zaakceptowany przez przełożonego (np. z powodu braku zastępstwa lub braku limitu dni).

### 12. Status: Anulowany

* **Nazwa pojęcia:** Status: Anulowany

* **Definicja:** Stan wniosku wycofanego przez pracownika przed jego rozpoczęciem lub przed decyzją kierownika.

## 3. Aktorzy i uprawnienia (Systemowe)

### 13. Pracownik (Rola)

* **Nazwa pojęcia:** Pracownik

* **Definicja:** Podstawowa rola w systemie uprawniająca do składania wniosków, podglądu własnego salda, historii oraz kalendarza zespołu.

### 14. Przełożony / Kierownik (Rola)

* **Nazwa pojęcia:** Przełożony / Kierownik

* **Definicja:** Rola uprawniająca do weryfikacji, akceptowania lub odrzucania wniosków złożonych przez podległych pracowników oraz podglądu grafiku zespołu.

### 15. Administrator / Kadry (Rola)

* **Nazwa pojęcia:** Administrator / Kadry

* **Definicja:** Rola posiadająca pełne uprawnienia w systemie: zarządzanie kontami użytkowników, przydzielanie limitów rocznych oraz generowanie raportów.

## 4. Pojęcia techniczne i architektoniczne

### 16. Architektura trójwarstwowa

* **Nazwa pojęcia:** Architektura trójwarstwowa

* **Definicja:** Wzorzec podziału aplikacji na trzy niezależne części: warstwę prezentacji (interfejs użytkownika), warstwę logiki biznesowej (serwer) oraz warstwę danych (baza danych).

### 17. Interfejs programistyczny aplikacji

* **Nazwa pojęcia:** Interfejs programistyczny aplikacji

* **Definicja:** Zbiór reguł i protokołów umożliwiający bezpieczną komunikację i wymianę danych pomiędzy interfejsem użytkownika a serwerem.

### 18. Encja bazy danych

* **Nazwa pojęcia:** Encja bazy danych

* **Definicja:** Obiekt w bazie danych reprezentujący kluczową strukturę informacji w systemie (np. Użytkownik, Wniosek Urlopowy, Limit Urlopowy).

### 19. Walidacja biznesowa

* **Nazwa pojęcia:** Walidacja biznesowa

* **Definicja:** Logika po stronie serwera sprawdzająca poprawność wprowadzonych danych przed zapisem (np. czy $data\_do \ge data\_od$, czy pracownik posiada wystarczającą liczbę dni).

### 20. Repozytorium kodu

* **Nazwa pojęcia:** Repozytorium kodu

* **Definicja:** Centralne miejsce przechowywania kodu źródłowego, historii zmian oraz dokumentacji projektu na platformie programistycznej.