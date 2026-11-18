# Lista kandydatów „Make or Buy” 

Zgodnie z analizą procesów biznesowych TO-BE oraz specyfikacją wymagań dla systemu URLOP, poniżej przedstawiono zestawienie głównych funkcji systemu. Tabela wskazuje, które elementy zostaną zaprogramowane przez zespół od podstaw (**make**), a które zostaną zrealizowane przy użyciu gotowych rozwiązań — usług uczelni, zewnętrznych API lub bibliotek open-source (**buy**).

## Tabela kandydatów

| Funkcja / wymaganie | Gotowe rozwiązanie (kandydat) | Wstępnie | Uzasadnienie / pytanie |
|---|---|---|---|
| **FR-XX: Logowanie i uwierzytelnianie użytkowników** | SSO uczelni (WSPA) / protokół OAuth2 | **buy** | Uczelnia posiada własne SSO; dodatkowo wymaganie NFR zabrania nam przechowywania haseł użytkowników w naszej bazie. |
| **FR-XX: Powiadomienia e-mail (np. o akceptacji wniosku)** | Serwer poczty uczelni (SMTP) / Zewnętrzna usługa (np. SendGrid) | **buy** | Brak uzasadnienia dla pisania własnego serwera poczty. **Pytanie:** czy uczelnia udostępni nam dane SMTP do wysyłki e-maili z aplikacji? |
| **FR-XX: Weryfikacja dni ustawowo wolnych od pracy** | Zewnętrzne API (np. Nager.Date lub polskie API rządowe) | **buy** | Ręczne utrzymywanie słownika świąt i weekendów jest podatne na błędy. Zewnętrzne API automatycznie dostarczy te dane do kalkulatora urlopów. |
| **FR-XX: Widok kalendarza urlopów (UI)** | Gotowa biblioteka front-end (np. FullCalendar.io) | **do decyzji** | Przyspieszy budowę interfejsu, ale wymaga sprawdzenia, czy łatwo zintegruje się z naszym systemem i modelem danych. |
| **FR-XX: Eksport zatwierdzonego wniosku do PDF** | Gotowa biblioteka w języku Python (np. ReportLab lub WeasyPrint) | **buy** | Generowanie układu dokumentów PDF od zera jest nieefektywne; gotowe biblioteki to rynkowy standard. |
| **NFR-XX: Przechowywanie danych i relacji** | Relacyjna baza danych (PostgreSQL lub SQLite) | **buy** | Używamy sprawdzonego gotowego silnika DBMS, nie tworzymy własnego mechanizmu zapisu danych na dysku. |
| **FR-04, FR-05: Rejestracja wniosku, proces akceptacji i kolizje** | — | **make** | Rdzeń domeny biznesowej systemu. System musi obsługiwać specyficzne reguły (BR-01...BR-07), co wymaga autorskiej implementacji. |
| **FR-XX: Obliczanie dostępnego limitu urlopowego** | — | **make** | Ścisłe reguły biznesowe zależące od stażu pracy i specyfiki organizacji, które musimy zaimplementować i przetestować samodzielnie. |

## Podsumowanie
Większość komponentów infrastrukturalnych oraz technicznych (baza danych, wysyłka e-maili, logowanie, generowanie PDF) zostanie oparta na gotowych rozwiązaniach (**buy**), co pozwoli zaoszczędzić czas zespołu z ograniczonym budżetem (0 PLN). Z kolei cały rdzeń biznesowy systemu, czyli logika procesowania wniosków urlopowych i walidacja reguł, zostanie zaimplementowany od zera (**make**). Ostateczne decyzje architektoniczne zostaną udokumentowane w postaci rejestru ADR (Architecture Decision Records).
