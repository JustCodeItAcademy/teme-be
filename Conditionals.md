# TEME BACK-END 📚

## IF statement

### 1. [LIVE] Citeste de la tastatura doua numere si afiseaza-l la consola pe cel mai mare dintre ele.
De exemplu, pentru valorie initiale:
```json
int a = 13;
int b = 14; 
```  
programul ar trebui sa afiseze in consola valoarea 14

HINT1: poti afisa valoarea impreuna cu un mesaj corespunzator folosind operatorul "+".
de exemplu, linia de cod:
```json
 System.out.println("numarul mai mai mare este " + b)
 ```  
va afisa in consola textul "numarul mai mare este 14", pentru ca Java concateneaza valoarea 14 cu String-ul "numarul mai mare este", rezultand un nou String
HINT2: Ar putea exista cazuri la care nu ne-am gandit? Daca da, trateaza-le.
 
### 2. [LIVE] Produci software pentru un fierbator de apa. Citeste de la tastatura temperatura curenta a apei si:
* Var1: afiseaza un mesaj corespunzator daca temperatura este mai mare de 100 de grade (apa fierbe)
* Var2: afiseaza un mesaj corespunzator daca apa fierbe, si un alt mesaj corespunzator in caz contrar
* Var3: afiseaza un mesaj corespunzator daca temperatura este mai mare de 100 de grade (apa fierbe), un alt mesaj daca temperatura este mai mica decat 50 de grade (apa este in curs de fierbere) si un altul daca apa are temperatura intre 50 si 100 de grade (apa este aproape fiarta)

### 3.[LIVE] Citeste de la tastatura un caracter care reprezinta da sau nu. In functie de acest input, afiseaza in consola “de acord” sau “nu sunt de acord”.
De exemplu, pentru:
```json
char c = ‘y’
```  
Se va afisa in consola “de acord”


### 4. Exerseaza scrisul de cod respectand urmatorii pasi:

```json
Pasul 1: Creează o variabilă de tip double cu valoarea 20.00.
Pasul 2: Creează o a doua variabilă de tip double cu valoarea 80.00.
Pasul 3: Adună ambele numere împreună, apoi înmulțește cu 100.00.
Pasul 4: Folosește operatorul de rest pentru a afla care este restul impartirii valorii obtinute la pasul 3 la numarul 40.00.
Pasul 5: Creează o variabilă booleană care atribuie valoarea true, dacă restul din pasul 4 este 0.00, sau false dacă nu este zero.
Pasul 6: Afișează variabila booleană doar pentru a vedea care este rezultatul.
Pasul 7: Scrie o instrucțiune if-then care afișează mesajul 'got some remainder', dacă valoarea booleana obtinuta la pasul 5 nu este true.
```




### 5. Avand la dispozitie o variabila care stocheaza un numar, afiseaza in consola daca numarul este par sau impar.
De exemplu, pentru valoarea initiala:
```json
int a = 12
```  
se va afisa in consola textul "numarul este par"



### 6.Construieste un calculator de baza. 
Citeste de la tastatura 2 numere si un caracter care reprezinta operatia pe care vrei sa o realizezi: +, -, * sau /.
Apoi afiseaza rezultatul calculului respectiv in consola. 
Ai grija sa tratezi cazul in care se face impartire la 0.

### 7. Vrei sa determini BMI-ul (Body Mass Index) al unei persoane. Citeste de la tastatura greutatea si inaltimea unui om. Apoi calculeaza BMI-ul utilizand formula: “greutate / (inaltime * intaltime)”
Apoi, daca BMI-ul este mai mic decat 18, 5 afiseaza in consola “esti sub greutatea normala”.
* Daca BMI-ul este intre 18.5 si 24.9, afiseaza in consola “ai greutatea normala”.
* Daca BMI-ul este intre 25 si 29.9, afiseaza in consola “esti peste greutatea normala”.
* Daca BMI-ule este mai mare deact 29.9, afiseaza in consola “esti obez”.

### 8. Ai o aplicatie de bilete la cinema si vrei sa determini pretul unui bilet. Pretul normal este de 10 lei. Daca persoana este copil (are varsta mai mica decat 12 ani), sau pensionar (mai mult de 65 de ani), atunci pretul este de 5 lei. In plus, in fiecare marti, este un discount de 2 lei pentru toata lumea.
Citeste de la tastatura varsta persoanei si ziua din saptamana, apoi afiseaza in consola pretul biletului.
 
### 9. Vrei sa construiesti un serviciu de tip RO-ALERT
Citeste de la tastatura previziunea pentru vreme si viteza vantului. Previziunea pentru vreme poate fi “rainy” sau “snowing”.
Daca previziunea pentru vreme este “rainy” sau previziunea este “snowing” si viteaza vantului este mai mare decat 30, afiseaza in consola mesajul “Ramai in casa, este periculos afara”
Altfel, afiseaza mesajul: “S-ar putea sa fie frumos afara”

De exemplu, pentru valorile initiale:
```json
String currentForecast = "rainy"
int currentWindSpeed = 40
```  
se va afisa in consola mesajul "Ramai in casa, este periculos afara"
 
### 10. Citeste de la tastatura un numar si afiseaza in consola “fizz” daca numarul este multimplu de 3, “buzz” daca numarul este multiplu de 5 si “fizzbuzz” daca numarul este divizibil atat cu 3 cat si cu 5 
De exemplu, pentru valoarea citita:
```json
int number = 15
```  
se va afisa in consola "fizzbuzz", pentru ca 15 se imparte exact atat la 5, cat si la 3
iar pentru:
```json
int number = 9
```  
se va afisa in consola "fizz", pentru ca 9 se imparte exact doar la 3
 
### 11. Citeste 3 numere de la tastatura si scrie un program care sa printeze in consola:
* “toate numerele sunt egale”, daca toate numerele sunt egale
* “toate numerele sunt diferite”, daca toate numerele sunt diferite
* “cel putin doua sunt egale”, daca oricare doua numere dintre cele trei sunt egale 
De exemplu, pentru valorile initiale:
```json
int a = 3
int b = 3
int c = 4
```  
se va afisa in consola: "cel putin doua sunt egale"

### 12. Scrieți o metoda Java care calculează scorul final al unui jucător într-un joc. Funcția va primi patru parametri:

```json
gameOver, de tip boolean, care indică dacă jocul s-a terminat sau nu.
score, de tip int, care reprezintă scorul actual al jucătorului.
levelCompleted, de tip int, care indică numărul nivelului pe care jucătorul l-a completat.
bonus, de tip int, care reprezintă bonusul de puncte primit pentru completarea nivelului.
```

Funcția va calcula scorul final în următorul mod:

- Dacă jocul s-a terminat (adică gameOver este true), funcția adaugă la scor produsul dintre nivelul completat (levelCompleted) și bonusul (bonus), plus un bonus suplimentar de 1000 de puncte.

Metoda va returna apoi scorul final calculat. Apeleaza metoda in metoda main()

### 13. Determinat pozitia unui jucator intr-un joc, in functie de scorul sau
Vom crea două metode:
Prima metodă ar trebui să se numească displayScorePosition().
- Această metodă ar trebui să aibă doi parametri, unul pentru numele unui jucător și unul pentru poziția unui jucător în lista de scoruri.
- Această metodă ar trebui să afișeze un mesaj de genul "Tim a reușit să ajungă pe poziția 2 în lista de scoruri".

A doua metodă ar trebui să se numească calculateHighScorePosition.
- Această metodă ar trebui să aibă doar un parametru, scorul jucătorului.
- Această metodă ar trebui să returneze un număr între 1 și 4, astfel:

```json
Scor mai mare sau egal cu 1000 -> poziția 1
Scor mai mare sau egal cu 500 dar mai mic decât 1000 -> poziția	2
Scor mai mare sau egal cu 100 dar mai mic decât 500 -> poziția	3
Toate celelalte scoruri -> poziția	4
```

În final, vom apeleaza ambele metode și afiseaza rezultatele pentru următoarele scoruri: 1500, 1000, 500, 100 și 25.
 
### 14. Citeste de la tastatura un numar care reprezinta un an, si afiseaza la consola daca anul este bisect sau nu. Un an este bisect daca este divizibil cu 400 sau cu 4 si in acelasi timp nu este divizibil cu 100
De exemplu, pentru valoarea initiala:
```json
int year = 2020
```  
se va afisa in consola: "anul 2020 este bisect"
 
### 15. Citeste de la tastatura doua numere, guess si answer si creeaza un joc de ghicit:
* daca raspunsul este mai mic decat solutia (adica valoarea variabilei guess, afiseaza “nu ai ghicit, numarul este prea mic”
* daca raspunsul este mai mare decat solutia, afiseaza “nu ai ghicit, numarul este prea mare”
* daca raspunsul este egal cu solutia, afiseaza “ai ghicit” 
De exemplu, pentru valorile initiale:
```json
int guess = 7
int answer = 8
```  
se va afisa in consola: "nu ai ghicit, numarul este prea mare"

### 16. Citeste de la tastatura un numar intre -10 si 10. 
* Daca valoarea citita este 10, -10, sau 0, printeaza un mesaj corespunzator (ex: "numarul este -10", in caz ca valoarea citita este -10)
* Altfel, printeaza fie "numarul este pozitiv", fie "numarul este negativ", dupa caz

### 17. Scrie un program care citeste de la tastatura 3 numere, reprezentand lugimile laturilor unui triunghi.
Trebuie sa afisezi in consola daca cele 3 laturi formeaza un triunghi valid, sau nu.
Un triunghi este valid daca suma lungimilor oricaror doua laturi este mai mare decat lugimea celei de-a 3-a laturi.

### 18. Scrie un program care intreaba utilizatorul care este parola secreta. 
Citeste de la tastatura raspunsul utilizatorului.\
* Printeaza apoi "corect", daca utilizatorul a raspuns cu 42, "forty-two" sau "forty-two", indiferent daca a folosit litere mari sau mici
* Atlfel, printeaza "incorect"

### 19. Angajatii unei banci trebuie sa intampine clientii cu salutul "Buna ziua", altfel vor fi penalizati.
Scrie un program care citeste de la tastatura salutul folosit.
* Daca salutul incepe cu "Buna ziua", atunci printeaza "nicio penalizare"
* Daca salutul incepe cu "B", dar nu este "Buna ziua", atunci printeaza "20 de lei penalizare"
* Daca salutul nici macar nu incepe cu "B", printeaza "100 de lei penalizare"
Ignora literele mari si literele mici din salut. Ignora si orice spatii care apar inainte de primul cuvant din salut

### 20. Scrie un program care sa spuna ce format media are un fisier, in functie de extensia lui.
Citeste de la tastatura numele fisierului.
* Daca extensia fisierului este .jpg, .jpeg, sau .png, atunci fisierul este o imagine
* Daca extensia fisierului este .webm, su .mp4, fisierul este un video.
* Daca extensia fisierului este .zip, fisierul este o arhiva

### 21. Vrem sa construim un sistem “smart home”. Sistemul controleaza caldura, lumina, si alarma.
Trebuie sa tinem cont de urmatoarele conditii:
Cladura se va porni daca temperatura este mai mica decat 20 de grade si fie este iarna, fie este cineva acasa
Luminile se vor porni daca afara este intuneric si daca cineva este acasa. Totusi, daca persoana care este acasa doarme, atunci luminile nu se vor porni
Alarma se va activa daca nimeni nu este acasa si fie este intuneric, fie fereastra este deschisa.

Casa are multi senzori care primesc informatii:
* Valoarea temperaturii
* Daca este sau nu cineva acasa
* Daca este sau nu intuneric afara
* Daca este sau nu fereastra deschisa
* Daca persoana din casa doarme
* Daca este iarna

Citeste de la tastatura valorile senzorilor si apoi implementeaza logica necesara.

### 22. Avem o platforma de cursuri online. 
Cursantii se pot inscrie la un curs daca indeplinesc toate urmatoarele 3 conditii:
Au platit costul cursului sau au o bursa pentru curs
Exista locuri disponibile in curs
Perioada de inscrieri este deschisa, sau au un cont premium

De asemenea, vor primi un discount la urmatorul curs daca indeplinesc cel putin una dintre urmatoarele 3 conditii:
au completat cel putin 2 cursuri in trecut si au un rating mediu mai mare decat 8 din 10 de la instructori
au recomandat plaftorma la cel putin 3 prieteni in trecut.

Citeste de la tastatura urmatoarele informatii:
* Daca studentul a platit costul cursului sau nu
* Daca studentul are bursa sau nu
* Numarul de locuri disponibile la curs
* Daca perioada de inscrieri este deschisa sau nu
* Daca studentul are cont premium sau nu
* Numarul de cursuri completate in trecut de catre sutdent
* Rating-ul mediu obtinut de student
* Numarul de prieteni recomandati de student

Apoi implementeaza logica necesara


### 23. Scrie un program care sa transforme viteza de la kilometri pe ora, la mile pe ora.
Scrieți o metodă numită toMilesPerHour() care are un parametru de tip double cu numele kilometersPerHour. Această metodă trebuie să returneze valoarea rotunjită a parametrului transformat la mile pe ora.

- Dacă parametrul kilometersPerHour este mai mic decât 0, metoda toMilesPerHour trebuie să returneze -1 pentru a indica o valoare invalidă.
- În caz contrar, dacă este pozitiv, calculează valoarea milelor pe oră, rotunjește-o și returnează-o. 

Exemple:
```json
toMilesPerHour(1.5); → ar trebui să returneze valoarea 1
toMilesPerHour(10.25); → ar trebui să returneze valoarea 6
toMilesPerHour(-5.6); → ar trebui să returneze valoarea -1
toMilesPerHour(25.42); → ar trebui să returneze valoarea 16
toMilesPerHour(75.114); → ar trebui să returneze valoarea 47
```

Scrie o altă metodă numită printConversion() care accepta un parametru de tip double, cu numele kilometersPerHour.
Această metodă nu trebuie să nu returneze nimic (void) și trebuie să calculeze conversia de la kilometri pe ora la mile pe ora (luand in considerare parametrul primit si apeland metoda toMilesPerHour()).

Apoi trebuie să afișeze un mesaj în formatul "XX km/h = YY mi/h".

- XX reprezintă valoarea originală in kilometri pe ora.
- YY reprezintă numarul de mile pe ora calculat.

Dacă parametrul apelul functiei toMilesPerHour() returneaza valoarea -1, atunci să se afișeze textul "Valoare Invalidă".

Exemple:
```json
printConversion(1.5); → ar trebui să afișeze următorul text (în consolă - System.out): 1.5 km/h = 1 mi/h
printConversion(10.25); → ar trebui să afișeze următorul text (în consolă - System.out): 10.25 km/h = 6 mi/h
printConversion(-5.6); → ar trebui să afișeze următorul text (în consolă - System.out): Valoare Invalidă
printConversion(25.42); → ar trebui să afișeze următorul text (în consolă - System.out): 25.42 km/h = 16 mi/h
printConversion(75.114); → ar trebui să afișeze următorul text (în consolă - System.out): 75.114 km/h = 47 mi/h
```

Apeleaza metoda Math.round() pentru a rotunji numărul de mile pe oră (double). Metoda round() returnează long.
Exemplu de folosire:
```json
double number = 1.5;
long rounded = Math.round(number);
```

### 24. Dorim sa implementam logica unui semafor pentru masini.
Culorile posibile ale semaforului sunt verde, galben si rosu.
Avem urmatoarele scenarii:
* Daca lumina este verde, afisam in consola in consola faptul ca masinile circula. Apoi lumina trebuie sa devina galben
* Daca lumina este galben, afisam in consola faptul ca masinile se pregatesc sa opreasca. Apoi lumina trebuie sa devina rosu
* Daca lumina este rosu, afisam in consola faptul ca masinile s-au oprit. Apoi lumina trebuie sa devina verde

Implementeaza codul care face toate verificarile in locul indicat din urmatoarea bucata de cod:

```json
        Scanner scanner = new Scanner(System.in);
        String trafficLight = scanner.nextLine();

        for (int i = 0; i < 10; i++) {
            System.out.println("Iteration: " + i);

            /* insereaza codul aici */

            TimeUnit.SECONDS.sleep(2);
        }

```  

### 25. Dorim sa implementam logica unui lift.
Trebuie sa tinem cont de urmatoarele conditii:
* Daca etajul curent este mai mic decat etajul dorit, afisam in consola faptul ca liftul urca
* Daca etajul curent este mai mare decat etajul dorit, afisam in consola faptul ca liftul coboara
* Daca etajul curent este acelasi cu etajul dorit, afisam in consola ca usile se deschis
* Liftul poate functiona doar daca nu este in mentenanta
* Daca liftul este la etajul 0 si nu este in mentenanta, afisam in consola ca usile sunt deschise (adica tot timpul usile raman deschise la parter)

Citeste de la tastatura etajul curent, etajul dorit, si daca liftul este in mentenanta sau nu.
Apoi implementeaza logica necesara.

### 26. Dorim sa implementam logica unui semafor pentru masini, unde exista o trecere de pietoni.
Culorile posibile ale semaforului sunt verde, si rosu.
Trebuie sa luam in considerare urmatoarele scenarii:
* Daca semaforul este verde si nu asteapta niciun pieton, afisam in consola faptul ca masinile circula
* Daca semaforul este verde si exista pietoni care asteapta, afisam in consola faptul ca lumina se va schimba la rosu. Si dupa un delay, semaforul trebuie sa se schimbe la rosu
* Daca semaforul este rosu si inca exista pietoni care asteapta, afisam in consola faptul ca acum trec pietonii
* Daca semaforul este rosu si nu mai exista pietoni care asteapta, afisam in consola ca lumina se va schimba la verde. SI dupa un delay, semaforul trebuie sa se schimbe la verde.


Citeste de la tastatura lumina semaforului pentru masini (trafficLight) si statusul pietonilor (arePedestriansWaiting).

Apoi implementeaza codul care face toate verificarile in locul indicat din urmatoarea bucata de cod:

```json
        Scanner scanner = new Scanner(System.in);
        String trafficLight = scanner.nextLine();
        boolean isPedestrianWaiting = scanner.nextBoolean();

        for (int i = 0; i < 10; i++) {
            System.out.println("Iteration: " + i);

            if (i == 3) {
                isPedestrianWaiting = true;
            }

            if (i == 6) {
                isPedestrianWaiting = false;
            }

            /* insereaza codul aici */
        }
```  

Foloseste comanda:
```json
TimeUnit.SECONDS.sleep(2)
```  
pentru a introduce un delay de 2 secunde acolo unde este cazul

Ruleaza codul si observa cum se desfasoara traficul.

### 27. Creeaza un automat de cafea. 
Automatul are 3 tipuri de cafea: espresso, care costa 5 lei, latte, care costa 7 lei si cappuccino, care costa 6 lei.\
Clientul poate adauga extra lapte pentru 1 leu, sau extra zahar in mod gratuit.\
Citeste de la tastatura tipul cafelei si daca clientul doreste extra lapte sau extra zahar.\
Apoi afiseaza in consola pretul total.\

### 28. Citeste de la tastatura 3 numere si afiseaza in consola cel mai mare(maximul) si cel mai mic (minimul) dintre cele 3 numere.

### 29. Citeste de la tastatura 3 numere si afiseaza-le in ordine crescatoare in consola. Foloseste doar instructiunea IF
