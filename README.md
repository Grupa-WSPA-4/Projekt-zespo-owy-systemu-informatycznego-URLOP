# Projekt-zespo-owy-systemu-informatycznego-URLOP
## KARTA PROJEKTU — WERSJA 0.1

### 1. Podstawowe informacje

**Nazwa projektu:**
System obsługi urlopów pracowniczych 

**Krótka nazwa / akronim:**

URLOPY

**Zespół:**

| Imię i nazwisko | Rola główna | Kontakt / login repozytorium |
|---|---|---|
| Yevhenii Bytsko|Kierownik | |
| Yauheni Dzerhach|Architekt i Projektant bazy danych | |
| Andrii Vydrych|Projektant UI/UX & Frontend | |
| Aldiyar Zhailauov|Tester & Backend Developer | |
| Mukhammed Mukhamedya|Analityk biznesowy | |

---

## 2. Problem

### Jaki problem chcemy rozwiązać?

Opiszcie problem w 3–6 zdaniach.

Nie opisujcie jeszcze technologii.

Obecnie wnioski urlopowe pracowników w firmie składane są w formie papierowej lub za pomocą wiadomości e-mail. Powoduje to duże opóźnienia w akceptacji, zagubienie dokumentów, trudności w ustaleniu, kto aktualnie jest w biurze, oraz brak przejrzystego podglądu wykorzystanego i przysługującego limitu dni urlopowych przez poszczególnych pracowników.

---

## 3. Kogo dotyczy problem?

Problem dotyczy pracowników, którzy nie mają łatwego podglądu swoich urlopów i muszą ręcznie pytać kadrę; przełożonych, którzy gubią się w papierowych wnioskach; oraz działu kadrowo-płacowego, który traci czas na ręczne rozliczanie limitów.

---

## 4. Cel systemu

Dokończcie zdanie:

> Celem systemu jest umożliwienie pracownikom elektronicznego składania wniosków urlopowych, automatyczna weryfikacja dostępnych limitów dni, usprawnienie procesu akceptacji przez przełożonych oraz zapewnienie przejrzystego kalendarza nieobecności w firmie.
---

## 5. Użytkownicy systemu

| Użytkownik / rola | Do czego będzie używał systemu? |
|---|---|
|Pracownik |Składanie wniosków urlopowych, sprawdzanie limitu dni, podgląd historii swoich wniosków i kalendarza nieobecności. |
|Kierownik / Przełożony |Przeglądanie wniosków podwładnych, zatwierdzanie lub odrzucanie wniosków urlopowych, podgląd grafiku zespołu. |
| Administrator / Kadry|Zarządzanie użytkownikami, konfiguracja limitów urlopowych, nadzór nad systemem i raportowanie. |


---

## 6. Interesariusze

| Interesariusz | Dlaczego system jest dla niego istotny? |
|---|---|
| Dział Księgowości / Kadr|System ułatwia rozliczanie czasu pracy i zapobiega błędom w naliczaniu urlopów. |
| Zarząd firmy|Zapewnia ciągłość pracy w działach dzięki lepszemu planowaniu nieobecności. |
| Dział IT|Odpowiada za utrzymanie, bezpieczeństwo i poprawne działanie platformy. |


---

## 7. Zakres IN

Co system **będzie** realizował?

1. Rejestracja i logowanie użytkowników z podziałem na role (Pracownik, Kierownik, Admin).
2. Składanie wniosków o urlop (wybór typu: wypoczynkowy, na żądanie itp., oraz zakresu dat).
3. Automatyczne sprawdzanie, czy pracownik posiada wystarczający limit dni urlopowych.
4. Proces akceptacji lub odrzucenia wniosku przez przełożonego (ze zmianą statusu wniosku).
5. Podgląd historii złożonych wniosków oraz aktualnego stanu urlopów (limit: przysługuje / wykorzystano / pozostało).
6. Kalendarz firmowy/zespołowy pokazujący nadchodzące nieobecności.
7. Podstawowy panel administracyjny do zarządzania kontami i limitami.

---

## 8. Zakres OUT

Czego system **nie będzie** realizował?

1. Integracji z zewnętrznymi systemami ZUS i Państwowej Inspekcji Pracy.
2. Naliczania list płac, premii i rozliczania nadgodzin finansowych.
3. Zaawansowanego planowania zmian nocnych i harmonogramów godzinowych pracy.
4. Obsługi zwolnień lekarskich (L4) i delegacji służbowych (skupiamy się czysto na urlopach).

---

## 9. Najważniejsze funkcje

Wymieńcie maksymalnie 10 funkcji.

1. Formularz składania nowego wniosku urlopowego.
2. Lista oczekujących wniosków do akceptacji dla menedżera.
3. System statusów wniosku (Oczekujący, Zatwierdzony, Odrzucony, Anulowany).
4. Automatyczne odejmowanie dni z puli pracownika po akceptacji.
5. Kalendarz nieobecności dla zespołu.
6. Licznik (saldo) urlopów widoczny dla pracownika.
7. Powiadomienia e-mail (lub systemowe) o zmianie statusu wniosku.
8. Archiwum historycznych urlopów z poprzednich lat.

---

## 10. Główne obiekty / dane

Jakiego rodzaju informacje system prawdopodobnie będzie przechowywał?

Przykład:

- użytkownik,
- rezerwacja,
- sala.

Dla naszego systemu:

1. Użytkownik (pracownik, dane osobowe, rola, przełożony)
2. LimitUrlopowy (rok, pula dni, wykorzystane dni)
3. WniosekUrlopowy (data złożenia, data od–do, typ urlopu, status, komentarz)
4. TypUrlopu (urlop wypoczynkowy, na żądanie, okolicznościowy)

---

## 11. Główne założenia

Przykład:

> Zakładamy, że każdy użytkownik posiada konto.

Zakładamy, że każdy pracownik ma przypisanego bezpośredniego przełożonego, który zatwierdza jego urlop.

Zakładamy, że pula dni urlopowych jest wprowadzana do systemu na początku roku przez dział kadr.

---

## 12. Wstępne ryzyka

Co może utrudnić wykonanie projektu?

| Ryzyko | Dlaczego może być problemem? |
|---|---|
|Błędy w logice kalendarza|Nakładanie się dni wolnych lub błędne liczenie dni roboczych z pominięciem weekendów/świąt. |
|Zbyt złożone uprawnienia |Struktura wielopoziomowej akceptacji (np. zastępca kierownika) może skomplikować kod. Rozwiązanie: uprościć do jednego przełożonego. |

---

## 13. Wstępnie rozważane technologie

Ta część **nie jest najważniejsza na tym etapie**.

Frontend:

....................................................................................

Backend:

....................................................................................

Baza danych:

....................................................................................

Inne:

....................................................................................

---
