### Edycja analityczna Humdrum


# Instrukcja pracy w projekcie

Ta instrukcja prowadzi krok po kroku przez cały proces pracy w projekcie.
Nie jest wymagana wcześniejsza znajomość GitHuba ani programowania.

1️⃣ Wymagania wstępne (jednorazowo)
1. Konto GitHub

Upewnij się, że masz konto na https://github.com

Zostaniesz dodany(a) do projektu przez kierownika projektu — zaakceptuj zaproszenie, które przyjdzie e-mailem lub w GitHubie.

2. Instalacja VS Code

Wejdź na: https://code.visualstudio.com

Pobierz wersję dla swojego systemu (Windows / macOS / Linux)

Zainstaluj program (standardowe ustawienia, „Dalej, dalej”)

3. Połączenie VS Code z GitHubem (jednorazowo)

Otwórz VS Code

Kliknij ikonę Source Control (rozgałęzienie po lewej stronie)

Kliknij Clone Repository

Wybierz Clone from GitHub

Zostaniesz poproszony(a) o zalogowanie do GitHuba w przeglądarce — zaloguj się i zatwierdź

Wybierz repozytorium projektu z listy lub wpisz:
https://github.com/annamatuszewska/edycja-humdrum.git

Wybierz folder na swoim komputerze, gdzie projekt ma się zapisać

Po chwili projekt otworzy się w VS Code.

---
2️⃣ Zasada organizacyjna projektu (bardzo ważne)

Pracujesz tylko na swoim podfolderze

Pracujesz zawsze na osobnym branchu

Jeden branch = jedna partia (50 plików)

Po wysłaniu Pull Request nie zmieniasz już tego brancha

Zakładamy, że zakresy plików nie nachodzą na siebie.

---
3️⃣ Rozpoczęcie pracy nad nową partią
Krok 1 – przejście na główną wersję projektu

W VS Code:

Otwórz Terminal (górne menu → Terminal → New Terminal)

Wpisz:

git checkout main
git pull


To pobiera najnowszą wersję projektu.

Krok 2 – utworzenie nowego brancha

Branch tworzysz zawsze przed rozpoczęciem nowej partii.

Schemat nazwy brancha:
imię-nazwaksiazki-nrplikustart-nrplikukoniec

Przykład:
anna-dwok02-0001-0050

Komenda:
git checkout -b imię-nazwaksiazki-nrplikustart-nrplikukoniec


Od tego momentu wszystkie zmiany zapisują się na tym branchu.

---
4️⃣ Praca z plikami

Edytuj tylko pliki ze swojej partii

Pliki:

poprawiane: w folderze humdrum/...

nowe teksty: w folderze tekst/...

Nie zmieniaj innych folderów ani plików

Pliki zapisuj normalnie (Ctrl+S / Cmd+S).

---
5️⃣ Zakończenie pracy nad partią (commit)

Po zakończeniu edycji wszystkich 50 plików:

Krok 1 – sprawdzenie zmian

W terminalu:

git status

Krok 2 – dodanie plików do commita
git add .

Krok 3 – zapisanie commita
git commit -m "Nazwaksiazki pliki nrplikustart–nrplikukoniec"

Przykład:
git commit -m "DWOK02 pliki 001–050"

---
6️⃣ Wysłanie pracy do sprawdzenia (Pull Request)
Krok 1 – wysłanie brancha
git push -u origin NAZWA_BRANCHA

Krok 2 – utworzenie Pull Request

VS Code wyświetli komunikat o wysłaniu brancha — kliknij Create Pull Request
(jeśli nie widzisz komunikatu, wejdź na GitHub w przeglądarce — pojawi się przycisk „Compare & pull request”)

Upewnij się, że:

base: main

compare: Twój branch

W opisie wpisz krótko:

jaka książka

zakres plików (np. 001–050)

Kliknij Create Pull Request

Na tym etapie Twoja praca jest gotowa.

Po akceptacji Pull Request

Po zaakceptowaniu i połączeniu (merge) przez kierownika projektu:

Krok 1 – odświeżenie informacji o repo
git fetch -p

Krok 2 – usunięcie lokalnego brancha
git branch -d NAZWA_BRANCHA


To porządkuje lokalną listę branchy.

---
8️⃣ Rozpoczęcie kolejnej partii

Dla kolejnej partii zawsze powtarzasz schemat:

git checkout main
git pull
git checkout -b NOWA_NAZWA_BRANCHA

---
9️⃣ Kiedy używać git pull?

Używaj:

zawsze przed rozpoczęciem nowej partii

gdy kierownik projektu poinformuje, że projekt został zaktualizowany

Nie musisz używać git pull w trakcie pracy nad jedną partią.

---
1️⃣0️⃣ Najważniejsze zasady (podsumowanie)

✔️ jedna partia = jeden branch

✔️ po wysłaniu Pull Request przechodzisz do kolejnej partii

✔️ nie zmieniasz plików poza swoim zakresem

✔️ zawsze zaczynasz nowy branch z main