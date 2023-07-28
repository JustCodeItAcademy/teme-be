# TEME BACK-END 📚

## Algoritmi 

### 1. Scrie un program care sa calculeze cum vei vopsi un gard
Avem un gard format din n scanduri, n fiind citit de la tastatura. n trebuie sa fie minim 3.
Un copil vopseste cu culoarea rosie din 2 in 2 scanduri (prima scandura colorata cu rosu este scandura 2), iar alt copil vopseste cu culoarea albastra din 3 in 3 scanduri (prima scandura colorata cu albastru este scandura 3).
Scandura 1 ramane nevopsita.
Exista posibilitatea ca o scandura sa fie violet, atunci cand cand ambii copii o vopsesc (de exemplu, scandura 6 va fi vopsita de ambii copii).
Calculeaza (din cele n scanduri) cate scanduri vopsite cu albastru vor fi, cate scanduri vopsite cu rosu vor fi, cate scanduri vopsite cu violet vor fi, si cate scanduri nevopsite vor fi.

### 2. Implementeaza jocul "piatra-foarfece-hartie".
Utilizatorul are la dispozitie alegerile "piatra", "foarfece", sau "hartie".
Alegerea utilizatorului va fi citita de la tastatura.
Alegerea calculatorului va fi generata random.
Daca alegerile sunt egale, atunci se va afisa "remiza".
Daca utilizatorul alege piatra si calculatorul foarfeca, sau utilizatorul foarfeca si calculatorul hartie, sau utilizatorul hartie si calculatorul piatra, atunci utilizatorul castiga.
Daca este fix invers, atunci calculatorul castiga.

Implementeaza apoi versiunea jocului in care se alege cel mai bun jucator din 3 runde de joc.

### 3. Genereaza mesajele pentru sistemul de like-uri al Facebook-ului.
Ai la dispozitie ca si input un array cu numele persoanelor care au dat like (la ceva) si trebuie sa generezi textul corespunzator, dupa regula pe care o deduci din urmatorul exemplu:
```json
[] -> "no one likes this"
["Peter"] -> "Peter likes this"
["Jacob", "Alex"] -> "Jacbok and Alex like this"
["Max", "John", "Mark"] -> "Max, John and mark like this"
["Alex", "Jacob", "Mark", "Max"] -> "Alex, Jacob and 2 others like this"
```
### 4. Verifica daca un String este o rotatie a altui String.
De exemplu, String-ul "cab" este rotatie a string-ului "abc", dar string-ul "acb" nu este rotatie a string-ului "abc".

### 5. Scrie un program care sa inverseze cuvintele dintr-un String.
De exemplu, pentru "programarea este usoara", se va afisa "usoara este programarea".

### 6. Scrie un program care sa codifice un String dupa metoda "Run Length Encoding".
Aceasta metoda detecteaza secventele de litere identice dintr-un String si le transforma intr-o cifra, care reprezinta de cate ori apare acea litera in acea secventa.
De exemplu, String-ul "AAAAAAAAAAAAABBCCCCDD" va fi convertit in "9A4A2B4C2D". Observa ca nu se foloseste 13A, secventele maxime fiind de 9 litere.

### 7. Scrie un program care sa construiasca o lista cu toate substring-urile unui String.
De exemplu, pentru String-ul "baca", lista de substring-uri este ["b","ba","bac","baca","a","ac","aca","c","ca"]

### 8.Scrie un program care sa calculeze costul stergerii caracterelor alaturate dintr-un String.
Citeste de la tastatura un String s. Stergerea celei de-a k-a litere din s are costul costs[k].
Dupa stergerea unei litere, costul stergerii celorlalte litere ramane acelasi.
De exemplu, pentrus s = "ab" si costs=[1,3], dupa stergerea lui 'a', costul stergerii lui 'b' va fi tot 3.

Vrei sa sterge niste litere din s astfel incat sa obtii un String fara litere identice una langa alta.
Trebuie sa afisezi la ecran care este costu minim al tututor stergerilor pe care ar trebuie sa le faci ca sa obtii un astfel de String?

De exemplu, pentru s = "abccbd", si costs = [0,1,2,3,4,5], costul total este 2.
De exemplu, pentru s = "aabbcc", si costs = [1,2,1,2,1,2], costul total este 3.








