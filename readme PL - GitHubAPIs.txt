GitHubAPIs_TestSample

1. Projekt testuje przykladowe konto na GitHub'ie i korzysta z REST API opisanego w dokumentacji https://docs.github.com/en/rest?apiVersion=2022-11-28  
   W tym prostym przykladzie korzystalem glownie z requestow dotyczacych repozytoriow: https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28

2. Opis projektu:
   Projekt ma za zadanie przetestowac mozliwosc utworzenia nowego repozytorium dla aktualnego user'a a nastepnie jego odczyt, edycje i usuniecie. 

   Projekt wykorzystuje podstawowe metody (CRUD): POST, READ, PUT(PATCH), DELETE i uzywa autoryzacji OAuth2, ustawionej dla calej kolekcji w zmiennej 'Token'.
   Zmienne 'Token', 'User' i 'url' sa zdefiniowane w srodowisku 'GitHub Environment'.
   Zmienna kolekcji ('NewRepo') przechowuje nazwe, nowo utworzonego, repozytorium a nastepnie jest uzywana do jego odczytu, edycji i usuwania.

   Na poczatku wystepuje request 'Get authenticated user', z ktorego pozyskiwany jest login (user). 
   Test, zawarty w tym requescie, sprawdza czy wykonal sie on z sukcesem i ustawia zmienna srodowiskowa 'User' na aktualnego user'a z odpowiedzi (response).
   Po utworzeniu nowego repozytorium oraz po jego edycji jest odpowiednio aktualizowana zmienna kolekcji 'NewRepo', do ktorej odwoluja sie kolejne requesty.   

   Dane do requestow przypisywane sa ze zmiennych srodowiskowych lub kolekcji, ktore sa aktualizowane przy wykorzystaniu skryptow wewnatrz testow. 

3. Celem tego prostego projektu 'end-to-end' jest zaprezentowanie podstawowych umiejetnosci z zakresu testowania REST API 
   w POSTMAN, ktore nabylem korzystajac z online'owych tutoriali. 

4. Zakres wiedzy:
   - Tworzenie kolekcji, requestow, podstawowych testow i skryptow.
   - Korzystanie z Collection Runnera
   - Tworzenie i odwolywanie sie do zmiennych (wew. body, endpoint'ow, testow) na roznych poziomach (tutaj Environment, Collection)
   - Tworzenie prostych skryptow:
     > Przekazywanie zmiennych pomiedzy requestami i ustawianie zmiennych na roznych poziomach.
     > Tworzenie prostych asercji
     > Logowanie na konsole
     > Korzystanie ze Snippets'ow 
   
UWAGA!:
Po wypushowaniu tego projektu do repozytorium, wewnetrzny security scaner na githubie zdezaktualizowal zainicjowany token.
Projekt wymaga odswiezenia tokena zdefiniowanego w srodowisku 'GitHub Environment', po jego zaimportowaniu.
Scope tokenu jest ustawiony w taki sposob, ze nie ujawnia wrazliwych danych wiec moge go w razie potrzeby udostepnic 
osobie zainteresowanej, do weryfikacji dzialania projektu.

      