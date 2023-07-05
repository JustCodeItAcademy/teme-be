
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
