
# TEME BACK-END 📚

## Variabile, tipuri de date, operatori

### 1. [LIVE] Scrie un program care sa citeasca de la tastatura numele tau, iar apoi sa afiseze mesajul “Salut”, urmat de numele tau.


### 2. Scrie un program care sa interschimbe valorile a doua variabile de tip int
De exemplu, pentru valorile initiale: 
```json
int a = 10;
int b = 20;
```  
ar trebui sa se afiseze in consola valoarea 20 cand il printezi pe a, si valoarea 10 cand il printezi pe b
 
### 3. Scrie un program care sa calculeze media aritmetica a 3 numere
De exemplu, pentru valorile initiale:
```json
double a = 4;
double b = 3;
double c = 1;
```  
programul ar trebui sa afiseze in consola valoarea 2.66
 
### 4. Scrie un program care converteste din grade Fahrenheit in grade Celsius
De exemplu, pentru valoarea initiala:
```json
int temperature = 95 
```  
programul ar trebui sa afiseze in consola valoarea 35 (valoarea in grade celsius)

### 5. [LIVE] Determina daca un utilizator se poate loga in aplicatie. 
Ai la dispozitie variabilele username si password deja declarate si initializate.  

Citeste de la tastatura inputUsername si inputPassword (adica username-ul si parola pe care ti le da utilizatorul).

Apoi, determina daca ce a introdus utilizatorul este acelasi lucru cu username-ul si parola existente.

Foloseste variabila isUserLoggedIn care sa retina daca utilizatorul s-a logat, sau nu, in aplicatie

### 6. Un utilizator poate vizualiza un video premium daca este un membru premium, sau daca a cumparat acel vide. In plus, server-ul trebuie sa fie on-line
Citeste de la tastatura:
```json
boolean isPremiumMember;
boolean hasBoughtVideo;
boolean isServerOnline;
```  
Foloseste variabila canViewVideo care sa retina daca utilizatorul poate sau nu sa vizualizeze video premium.

### 7.Un student poate sa participe la un curs avansat daca a completat “prerequisites” (adica anumite cursuri anterioare) si daca nota medie in prerequisites este A sau B. Cursul trebuie sa aiba, de asemenea, locuri libere.
Citeste de la tastatura:
```json
 boolean hasCompletedPrerequisites 
 char gradeInPrerequisites 
 boolean hasOpenSpots 
 ```  
Foloseste variabila canTakeCourse care sa retina daca studentul poate sa participe la curs, sau nu.

### 8.Cream o aplicatie pentru o biblioteca. O carte poate fi imprumutata daca nu este deja imprumutata si daca clientul nu are mai mult de 3 carti imprumutate. In plus, clientul trebuie sa nu aiba deloc datorii
Citeste de la tastatura:
```json
boolean isBookRented
int numberOfRentedBooks
boolean hasLateFees
```  
Foloseste variabila canRentBook care sa retina daca clientul poate sa imprumute cartea, sau nu.

### 9.Un angajat este eligibil pentru o promovare daca lucreza in companie de cel putin 5 ani si scorul de performanta este mai mare decat 8, sau daca are o recomandare de la manager si nu are sanctiuni disciplinare. Totusi, promovarea se poate face doar daca compania nu are promovarile inghetate.
Citeste de la tastatura:
```json
int yearsWorked 
double performanceScore 
boolean hasManagerRecommendation
boolean hasDisciplinaryAction 
boolean isPromotionFreeze 
```  
Foloseste variabila isEligibleForPromotion care sa retina daca angajatul poate promova, sau nu.

 ### 10.Un utilizator poate accesa o pagina secreta de pe un website daca are rolul de administrator sau daca are atat rolul de manager si este si parte din proiectul paginii secrete. In plus, utilizatorul trebuie sa aiba 2FA (two factor authentication) si sa nu fie marcat cu activitate suspicioasa. In plus, server-ul trebuie sa fie pornit.
Citeste de la tastatura:
```json
 boolean isAdministrator
 boolean isManager 
 boolean isPartOfProject
 boolean hasTwoFactorEnabled
 boolean isFlaggedSuspicious
 boolean isServerUp 
 ```  
Foloseste variabila canAccessPage care sa retina daca utilizatorul poate accesa pagina secreta, sau nu.

### 11.Un jucator poate avansa la nivelul urmator doar daca are mai mult de 1000 de puncte sau daca are o cheie de aur, si in plus, nu este sub atac. Mai mult, jocul trebuie sa nu fie pus pe pauza si serverul trebuie sa ruleze.
Citeste de la tastatura:
```json
 int playerPoints 
 boolean hasGoldenKey 
 boolean isUnderAttack 
 boolean isGamePaused 
 boolean isServerRunning 
 ```  
Foloseste variabila canAdvanceLevel care sa retina daca jucatorul poate sa avanseze, sau nu.

### 12.O racheta poate decola daca are nivelul de combustibil mai mare decat 50%, daca toate sistemele functioneaza (reprezentate de un system check), si daca vremea este buna. Racheta nu poate decola daca are oameni la bord. Exceptia este ca poate decola cu oameni la bord, daca este o misiune de salvare
Citeste de la tastatura:
```json
double fuelLevel 
boolean isSystemsCheckPassed 
boolean isWeatherClear
boolean hasLivingCreaturesInCargo
boolean isRescueMission 
```  
Foloseste variabila canTakeOff care sa retina daca racheta poate sa decoleze, sau nu.

### 13.Un angajat poate sa rezerve un meeting room doar daca este disponibil si daca nu a depasit numarul de rezervari per saptamana. Daca camera este o camera speciala (cu multe locuri), atunci poate fi rezervata doar daca echipa angajatului are mai mult de 10 membri.
Citeste de la tastatura:
```json
boolean isRoomAvailable
boolean isQuotaExceeded
boolean isHighCapacityRoom
int teamSize
```  
Foloseste variabila canBookRoom care sa retina daca angajatul poate sa rezerve sala, sau nu.

### 14.Un aplicant pentru un credit va obtine creditul daca are un credit score peste 700 si daca are o sursa de venit stabila. Daca creditul este mare (peste 100000 euro), atunci clientul trebuie sa ofere si colateral ca sa fie aprobat. In plus, banca nu trebuie sa fie intr-o perioada in care nu ofera credite.
Citeste de la tastatura:
```json
int creditScore
boolean hasSteadyIncome 
double loanAmount 
boolean hasCollateral 
boolean isBankInCreditFreeze 
```  
Foloseste variabila isLoanApproved care sa retina daca creditul este aprobat, sau nu.

### 15.O retea securizata poate fi accesata daca utilizatorul este un angajat si are badge-ul activ, sau daca este un contractor cu badge-ul activ si cu contractul neexpirat. In plus, trebuie sa nu fie o perioada de mentenanta a retelei.
Citeste de la tastatura:
```json
boolean isEmployee 
boolean isContractor
boolean isBadgeActive 
boolean isContractExpired 
boolean isMaintenanceHour 
```  
Foloseste variabila canAccessNetwork care sa retina daca reteaua poate fi accesata, sau nu.

If statement: 
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

### 4. Avand la dispozitie o variabila care stocheaza un numar, afiseaza in consola daca numarul este par sau impar.
De exemplu, pentru valoarea initiala:
```json
int a = 12
```  
se va afisa in consola textul "numarul este par"

### 5.Construieste un calculator de baza. 
Citeste de la tastatura 2 numere si un caracter care reprezinta operatia pe care vrei sa o realizezi: +, -, * sau /.
Apoi afiseaza rezultatul calculului respectiv in consola. 
Ai grija sa tratezi cazul in care se face impartire la 0.

### 6. Vrei sa determini BMI-ul (Body Mass Index) al unei persoane. Citeste de la tastatura greutatea si inaltimea unui om. Apoi calculeaza BMI-ul utilizand formula: “greutate / (inaltime * intaltime)”
Apoi, daca BMI-ul este mai mic decat 18, 5 afiseaza in consola “esti sub greutatea normala”.
* Daca BMI-ul este intre 18.5 si 24.9, afiseaza in consola “ai greutatea normala”.
* Daca BMI-ul este intre 25 si 29.9, afiseaza in consola “esti peste greutatea normala”.
* Daca BMI-ule este mai mare deact 29.9, afiseaza in consola “esti obez”.

### 7. Ai o aplicatie de bilete la cinema si vrei sa determini pretul unui bilet. Pretul normal este de 10 lei. Daca persoana este copil (are varsta mai mica decat 12 ani), sau pensionar (mai mult de 65 de ani), atunci pretul este de 5 lei. In fiecare marti, este un discount de 2 lei pentru toata lumea.
Citeste de la tastatura varsta persoanei si ziua din saptamana, apoi afiseaza in consola pretul biletului.
 
### 8. Vrei sa construiesti un serviciu de tip RO-ALERT
Citeste de la tastatura previziunea pentru vreme si viteza vantului. Previziunea pentru vreme poate fi “rainy” sau “snowing”.
Daca previziunea pentru vreme este “rainy” sau previziunea este “snowing” si viteaza vantului este mai mare decat 30, afiseaza in consola mesajul “Ramai in casa, este periculos afara”
Altfel, afiseaza mesajul: “S-ar putea sa fie frumos afara”

De exemplu, pentru valorile initiale:
```json
String currentForecast = "rainy"
int currentWindSpeed = 40
```  
se va afisa in consola mesajul "Ramai in casa, este periculos afara"
 
### 9. Citeste de la tastatura un numar si afiseaza in consola “fizz” daca numarul este multimplu de 3, “buzz” daca numarul este multiplu de 5 si “fizzbuzz” daca numarul este divizibil atat cu 3 cat si cu 5 
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
 
### 10. Citeste 3 numere de la tastatura si scrie un program care sa printeze in consola:
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
 
### 11. Citeste de la tastatura un numar care reprezinta un an, si afiseaza la consola daca anul este bisect sau nu. Un an este bisect daca este divizibil cu 400 sau cu 4 si in acelasi timp nu este divizibil cu 100
De exemplu, pentru valoarea initiala:
```json
int year = 2020
```  
se va afisa in consola: "anul 2020 este bisect"
 
### 12. Citeste de la tastatura doua numere, guess si answer si creeaza un joc de ghicit:
* daca raspunsul este mai mic decat solutia (adica valoarea variabilei guess, afiseaza “nu ai ghicit, numarul este prea mic”
* daca raspunsul este mai mare decat solutia, afiseaza “nu ai ghicit, numarul este prea mare”
* daca raspunsul este egal cu solutia, afiseaza “ai ghicit” 
De exemplu, pentru valorile initiale:
```json
int guess = 7
int answer = 8
```  
se va afisa in consola: "nu ai ghicit, numarul este prea mare"

### 13. Scrie un program care citeste de la tastatura 3 numere, reprezentand lugimile laturilor unui triunghi.
Trebuie sa afisezi in consola daca cele 3 laturi formeaza un triunghi valid, sau nu.
Un triunghi este valid daca suma lungimilor oricaror doua laturi este mai mare decat lugimea celei de-a 3-a laturi.

### 14. Vrem sa construim un sistem “smart home”. Sistemul controleaza caldura, lumina, si alarma.
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

### 15. Avem o platforma de cursuri online. 
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

### 16. Dorim sa implementam logica unui semafor pentru masini.
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

### 17. Dorim sa implementam logica unui lift.
Trebuie sa tinem cont de urmatoarele conditii:
* Daca etajul curent este mai mic decat etajul dorit, afisam in consola faptul ca liftul urca
* Daca etajul curent este mai mare decat etajul dorit, afisam in consola faptul ca liftul coboara
* Daca etajul curent este acelasi cu etajul dorit, afisam in consola ca usile se deschis
* Liftul poate functiona doar daca nu este in mentenanta
* Daca liftul este la etajul 0 si nu este in mentenanta, afisam in consola ca usile sunt deschise (adica tot timpul usile raman deschise la parter)

Citeste de la tastatura etajul curent, etajul dorit, si daca liftul este in mentenanta sau nu.
Apoi implementeaza logica necesara.

### 18. Dorim sa implementam logica unui semafor pentru masini, unde exista o trecere de pietoni.
Trebuie sa luam in considerare urmatoarele scenarii:
*Daca semaforul este verde si nu asteapta niciun pieton, afisam in consola faptul ca masinile circula
*Daca semaforul este verde si exista pietoni care asteapta, afisam in consola faptul ca lumina se va schimba la rosu. Si dupa un delay, semaforul trebuie sa se schimbe la rosu
*Daca semaforul este rosu si inca exista pietoni care asteapta, afisam in consola faptul ca acum trec pietonii
*Daca semaforul este rosu si nu mai exista pietoni care asteapta, afisam in consola ca lumina se va schimba la verde. SI dupa un delay, semaforul trebuie sa se schimbe la verde.


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



### 19. Citeste de la tastatura 3 numere si afiseaza in consola cel mai mare(maximul) si cel mai mic (minimul) dintre cele 3 numere.

### 20. Citeste de la tastatura 3 numere si afiseaza-le in ordine crescatoare in consola. Foloseste doar instructiunea IF
