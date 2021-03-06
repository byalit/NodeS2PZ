## Zasady zaliczenia przedmiotu

Ostateczny termin zaliczenia: 26.06.2022 (ostatni zjazd)

Sposób zaliczenia:
- przygotowujesz implementacje wybranych przez siebie funkcji
- przesyłasz mi rozwiązania poprzez email, Slack (sugeruje nie umieszczać ich w publicznym repozytorium :) )
- omawiamy przygotowane rozwiązanie poprzez Teams, Zoom, meet.jit.si:
    - kalendarz https://calendly.com/pawel-lukaszuk-jsd/nodejs
- w razie wątpliwości kontaktujesz się ze mną za pomocą Slack, email    

Skala ocen:
- 0-8 pkt &rarr; 2
- 9-11 pkt &rarr; 3
- 12-14 pkt &rarr; 3.5
- 15-18 pkt &rarr; 4
- 19-22 pkt &rarr; 4.5
- 23 i więcej pkt &rarr; 5

### **Uwagi**
1. Możesz użyć dowolnej wersji Node.js $\ge$ 14.
2. Możesz użyć dowolnego modułu `npm` (o ile zadanie nie mówi inaczej)

## Cel biznesowy

Celem projektu jest stworzenie aplikacji pozwalającej na zarządzanie ogłoszeniami online - tablica ogłoszeń.

Każde ogłoszenie ma:
- tytuł
- opis
- autora
- kategorię
- tagi (wiele tagów)
- cenę
- ... (miejsce na Twoje pomysły, najlepsze będą punktowane dodatkowo)

Interfejs graficzny nie jest wymagany. Funkcjonalność będzie sprawdzona przy pomocy Postmana. Należy pamiętać o obsłudze błędów, nazewnictwie endpointów, obsłudze metod HTTP oraz zwracanych kodów odpowiedzi HTTP.

Lista funkcji:

0. [zadanie konieczne do zaliczenia] Aplikacja jest udokumentowana za pomocą Postmana - kolekcją zawierającą przykłady żądań do wszystkich przygotowanych funkcji

1. [1 punkt] Port z którego korzysta aplikacja powinien być ustawiany za pomocą zmiennych środowiskowych

2. [1 punkt] Aplikacja na żądania wysłane pod adres `/heartbeat` odpowiada zwracając aktualną datę i godzinę

3. [1 punkt] Aplikacja umożliwia dodawanie ogłoszenia

4. [2 punkty] Aplikacja umożliwia zwracanie wszystkich ogłoszeń oraz pojedynczego ogłoszenia

5. [1 punkt] Aplikacja umożliwia usuwanie wybranego ogłoszenia

6. [1 punkt] Aplikacja umożliwia modyfikowanie wybranego ogłoszenia

7. [1 punkt za każde kryterium wyszukiwania/maksymalnie 5 punktów] Aplikacja pozwala na wyszukiwanie ogłoszeń według różnych kryteriów (tytuł, opis, zakres data, zakres ceny itp).

8. [4-8 punktów] Aplikacja zapisuje ogłoszenia w bazie danych [8 punktów] lub plikach [4 punkty]

9. [2 punkty] Usuwanie i modyfikowanie ogłoszeń jest zabezpieczone hasłem (np. middleware weryfikujące hasło), przy braku dostępu zwracany jest stosowny komunikat i kod odpowiedzi HTTP. Nie jest wymagane zabezpieczenie na poziomie *produkcyjnym*, raczej podstawowe rozwiązanie.

10. [4 punkty] Aplikacja ma 3 zdefiniowanych na stałe użytkowników, każdy z nich może usuwać i modyfikować tylko te ogłoszenia które sam dodał, przy braku dostępu zwracany jest stosowny komunikat i kod odpowiedzi HTTP

11. [3 punkty] Aplikacja po uruchomieniu z parametrem (np `node app.js debug`) zapisuje w pliku czas odebrania każdego żądania, metodę HTTP oraz adres na który przyszło żądanie

12. [2 punkty] Aplikacja po odebraniu żądania do adresu który nie istnieje powinna zwracać statyczny obrazek zamiast domyślnej strony błędu 404

13. [2 punkty] W przypadku wystąpienia błędów aplikacji, szczegóły błędu zapisywane są w console.log a użytkownik dostaje stosowny komunikat i kod odpowiedzi HTTP
