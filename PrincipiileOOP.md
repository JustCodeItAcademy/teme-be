
# TEME BACK-END 📚

## Principiile OOP (mai puțin confortabil)

### 1. Construiește o aplicație care să modeleze în cod forme geometrice și operațiile cu ele

#### Interfața `Shape`

Metode:
* `computeArea()` - tipul returnat este `double` și nu primește niciun parametru

#### Clasa `Circle` (implementează interfața `Shape`)

Atribute:
* `radius` (raza cercului)

Metode:
* `computeArea()`

#### Clasa `Rectangle` (implementează interfața `Shape`)

Atribute:
* `height` (lungime)
* `width` (lățime)

Metode:
* `computeArea()`

#### Clasa `Canvas`

Metoda `main()`:
* În această metodă vei testa calculul ariei atât pentru cercuri cât și pentru dreptunghiuri



### 2. Creează o aplicație care să simuleze o școală
#### Clasa `Person` (abstractă)

Atribute:
* `firstName`
* `lastName`

Metode:
* Metoda abstractă `introduce()`

#### Clasa `Teacher` (extinde `Person`)

Atribute:
* `department`
* `subject` (adică ce predă profesorul)

Metode:
* Metoda `introduce()` - implementează metoda abstractă din subclasă și afișează un mesaj. Exemplu: “I am John Decker, I teach Math and I am a teacher”

#### Clasa `Student` (extinde `Person`)

Atribute:
* `groupClass` (adică clasa în care este studentul)

Metode:
* Metoda `introduce()` - implementează metoda abstractă din subclasă și afișează un mesaj. Exemplu: “I am Dave Brown, I am in 12A class and I am a student”


### 3. Creează o clasă care să simuleze un adăpost de animale

#### Clasa `Animal`

Atribute:
* `name`
* `age`

Metode:
* Metoda abstractă `makeSound()`

#### Clasa `Cat` (extinde `Animal`)

Atribute: niciun atribut nou

Metoda `makeSound()`:
* Va afișa un mesaj ca de exemplu: “Pisica Tom face miau”

#### Clasa `Dog` (extinde `Animal`)

Atribute: niciun atribut nou

Metoda `makeSound()`:
* Va afișa un mesaj ca de exemplu: “Câinele Azor latră”

#### Clasa `SecurityDog` (extinde `Dog`)

Atribute: niciun atribut nou

Metoda `makeSound()`:
* Va afișa un mesaj ca de exemplu: “Câinele Azor latră agresiv”

#### Clasa `Shelter`

Atribute:
* `animals` (adică o listă de animale)

Metode:
* `makeNoise()`:
  - Această metodă va face ca toate animalele din listă să scoată sunet

* `addAnimal()`:
  - Această metodă va adăuga un animal în lista de animale

* `main()`:
  - În această metodă se vor adăuga animale în lista folosind metoda `addAnimal()`
  - Apoi se va apela metoda `makeNoise()` pentru ca fiecare animal din listă să facă sunetul corespunzător (de câine sau de pisică, după caz)

### 4. Ești în procesul de dezvoltare a unei aplicații care colectează informații despre ce site-uri web au fost vizitate de către ce utilizatori. 

Există trei clase: User (Utilizator), WebSite (Site web) și Visit (Vizită). Multe câmpuri și metode ale acestor clase sunt identice.

Scrie o clasă de bază abstractă nouă numită BaseEntity (Entitate de bază). Clasele furnizate trebuie să o extindă. Mută toate câmpurile și metodele repetitive în noua clasă.

După modificările tale, următorul cod trebuie să funcționeze corect:

```js
User user = new User();
user.setName("John Grant");

BaseEntity userEntity = user;
userEntity.setId(100);
userEntity.setVersion(1);

WebSite site = new WebSite();
site.setUrl("https://hyperskill.org");

BaseEntity siteEntity = site;
siteEntity.setId(101);
siteEntity.setVersion(1);

Visit visit = new Visit();
visit.setUser(user);
visit.setSite(site);

BaseEntity baseVisit = visit;
baseVisit.setId(102);
baseVisit.setVersion(103);

```

### 6. Creează o aplicație de gestionare a conturilor deschise la o bancă pentru un client.
#### Clasa abstractă `BankAccount`

Atribute:
* `balance` (câți bani se află în cont, o valoare de tip double care semnifică suma în lei)
* `accountNumber`

Metode:
* Metoda abstractă `withdraw()`
* Metoda abstractă `deposit()`

#### Clasa `StudentAccount` (extinde `BankAccount`)

Atribute:
* `maxDepositAmount` - va trebui să nu își schimbe valoarea o dată ce a fost inițializată

Metode:
* Metoda `withdraw()` - se pot retrage maxim câți bani sunt în cont în momentul retragerii
* Metoda `deposit()` - se pot depune maxim “maxDepositAmount” bani o dată

#### Clasa `SpendingAccount` (extinde `BankAccount`)

Atribute:
* `maxWithdrawalAmount` - poate să își schimbe valoarea o dată ce a fost inițializată

Metode:
* Metoda `withdraw()` - se pot retrage cu maxim “maxWithdrawalAmount” RON mai mult decât există în cont în momentul retragerii (exemplu: dacă în cont sunt 5000 de RON, iar maxWithdrawalAmount este 2000 RON, se pot retrage maxim 7000 RON)
* Metoda `deposit()` - oricâți bani se pot depune în cont

#### Clasa `Person`

Atribute:
* `firstName`
* `lastName`
* `accountList` - adică un array care ține lista de conturi ale unei persoane

Metode:
* Metoda `addAccount()` - va da posibilitatea persoanei să adauge un cont în lista de conturi
* Metoda `listAccounts()` - va printa accountNumber împreună cu balance pentru fiecare cont din listă
* Metoda `deposit()` - va adăuga o anumită sumă de bani într-un cont
* Metoda `withdraw()` - va retrage o anumită sumă de bani dintr-un cont
* Metoda `checkAccountDetails()` - va printa toate detaliile unui anumit cont

#### Clasa `BankingApp`

Clasa va avea doar metoda `main()`, unde se va instanția o persoană și se vor testa metodele pe care le poate face persoana (adăugare cont, deposit, etc.).



### 7.Creează o aplicație de plăți

In aceasta aplicatie voi putea stoca mai multe carduri personale si voi putea plati cu cel pe care il aleg.
Construieste desing-ul si functionalitatile astfel:

#### Interfața `Payable`
Metode:
* `pay(double amount)` - care primește ca parametru o valoare de tip double (suma plătită)

#### Clasa `Card`
Atribute:
* `isActive`
* `PIN`
* `cardNumber`
* `cardHolderName`
* `cardBalance`
Metode:
* `changePin()` - schimbă valoarea PIN-ului, dar doar dacă aceasta este o valoare formată din 4 cifre
* `freezeCard()` - face ca cardul să fie inactiv

#### Clasa `DebitCard`, care va extinde `Card` și va implementa interfața `Payable`
Atribute:
* `maxTransactionAmount`
Metode:
* `pay()` - nu se va putea plăti mai mult decât `maxTransactionAmount`
* `changeTransactionLimit()` - va da o nouă valoare atributului `maxTransactionAmount`

#### Clasa `CreditCard`, care va extinde `Card` și va implementa interfața `Payable`
Atribute:
* `maxOverDraft` - nu se va putea schimba valoarea acestui atribut
Metode:
* `pay()` - nu se va putea plăti mai mult decât `cardBalance + maxOverDraft`

#### Clasa `Address`
Atribute:
* `street`
* `number`
* `city`
Metode: doar getteri și setteri

#### Clasa `ShoppingAccount`
Atribute:
* `cardList` - o listă de carduri
* `addressList` - o listă de adrese
* `firstName`
* `lastName`
* `currentPaymentMethod` - poate fi de fapt un `CreditCard` sau un `DebitCard`
* `currentBillingAddress`
Metode:
* `addPaymentMethod()`
* `addAddress()` 
* `removePaymentMethod()` 
* `removeAddress()`
* `selectPaymentMethod(String cardNumber)` - setează `currentPaymentMethod` în funcție de numărul de card primit ca și parametru
* `selectAddress(String street)` - setează `currentBillingAddress` în funcție de strada primită ca și parametru
* `generateInvoice(amount, address, card)` - se va printa un mesaj în funcție de suma, cardul și adresa cu care a fost făcută tranzacția (de exemplu: “Nume: Olimpiu Stefan. Ați plătit suma 2300 RON folosind cardul cu numărul 1234 1234 1234 1234 pentru adresa: str. Republicii, nr. 12, Cluj-Napoca”)

#### Clasa `Shop`
Clasa `Shop` va avea o metodă `main` unde vor fi testate funcționalitățile implementate (se va crea un `shopping account`, se vor adăuga adrese și modalități de plată în el, se va selecta o adresă, se va selecta o modalitate de plată, se va plăti o anumită sumă de bani folosind metoda de plată selectată și apoi se va genera o factură)

### 8. Creeaza o aplicatie de gestiune a unei companii
O companie are un nume, data infiintarii, o lista de departamente
Un departament un nume si o lista de angajati.
Un angajat are nume, prenume, salariu si o adresa.
O adresa are oras, strada, numar.

#### 8.1. Scrie o metoda care afiseaza numele angajatului

#### 8.2. Scrie o metoda care afiseaza strada adresei angajatului

#### 8.3. Scrie o metoda care afiseaza toate atributele adresei angajatului

#### 8.4. scrie un program care afiseaza numarul de angajati din departament

#### 8.5. scrie o metoda care printeaza toti angajatii din departament

#### 8.6. scrie o metoda care printeaza toate strazile adreselor angajatilor din departament

#### 8.7. scrie o metoda care cauta un anumit angajat dupa nume in departament, si ii afiseaza numele daca il gaseste

#### 8.8. scrie o metoda care printeaza adresa unui anumit angajat din departament

#### 8.9. scrie o metoda care cauta o adresa (dupa strada) in lista de angajati a departamentului, si ii afiseaza strada daca o gaseste

#### 8.10. scrie o metoda care printeaza toate departamentele din companie

#### 8.11. scrie o metoda care printeaza toti angajatii dintr-un anumit departament din companie

#### 8.12. scrie o metoda care printeaza cati angajati are un anumit departament din companie

#### 8.13. scrie o metoda care printeaza toate strazile adreselor angajatilor dintr-un anumit departament din companie

#### 8.14. scrie o metoda care printeaza strada adresei unui anumit angajat din companie

#### 8.15. scrie o metoda care cauta un angajat (dupa nume) intr-un anumit departament din companie si ii afiseaza numele, daca il gaseste

#### 8.16. scrie o metoda care printeaza toti angajatii din toate departamentele din companie

#### 8.17. scrie o metoda care printeaza numarul total de angajati din toate departamentele din companie

#### 8.18. scrie o metoda care cauta un angajat in toate departamentele din companie si ii afiseaza numele, daca il gaseste

#### 8.19. scrie o metoda care printeaza numele angajatului cu cel mai mare salariu dintr-un anumit departament

#### 8.20. scrie o metoda care printeaza numele angajatului cu cel mai mare salariu din companie

#### 8.21. scrie o metoda care printeaza numele angajatului cu cel mai mic salariu din companie

#### 8.22. scrie o metoda care printeaza numele angajatului cu cel mai mic salariu dintr-un anumit departament;

### 9. Parcările sunt o necesitate urbană.
#### Varianta 1

Ele oferă locuri unde poți lăsa mașina fără să-ți faci griji că ar fi furată sau ridicată. Sistemele moderne de parcare auto sunt automate și sunt capabile de auto-gestionare. În acest proiect, vei crea un sistem similar, dar într-o formă simplificată.

Să începem prin scrierea unui program care poate plasa mașina ta într-o parcare și elibera locul atunci când mașina pleacă. Acesta va fi "scheletul" parcării noastre funcționale și vom adăuga la el în pașii următori. În momentele aglomerate, parcarea poate rămâne fără locuri vacante. Programul ne va oferi informații agregate despre starea actuală a parcării.

Prima versiune a programului tău ar trebui să afișeze următoarele, ca exemplu:

```
Mașina albă cu numarul BN39GIM s-a parcat.
Mașina galbenă cu numarul HD23ABC a părăsit parcarea.
Mașina verde cu numarul CJ96BOS s-a parcat.
```
#### Varianta 2

Avem nevoie de mai multe locuri de parcare, spre deosebire de varianta 1, unde nu am alocat mai multe locuri de parcare. Sa zicem ca avem 20 de locuri.

Când utilizatorul vrea să parcheze mașina, programul ar trebui să găsească un loc de parcare disponibil cu cel mai mic număr.

Utilizatorul poate scrie comenzile `park` și `leave` de mai multe ori și poate tasta `exit` pentru a încheia programul.

Dacă parcarea este plină și nu mai există loc, programul ar trebui să afișeze Mesajul: `Ne pare rău, parcarea este plină..`

Dacă există mai multe locuri disponibile pentru o mașină, programul ar trebui să aloce întotdeauna locul cu cel mai mic număr.

```
Mașina albă cu numarul BN39GIM s-a parcat.
Mașina galbenă cu numarul HD23ABC a părăsit parcarea.
Mașina verde cu numarul CJ96BOS s-a parcat.
```
##### Exemplu:
Simbolul `>` reprezinta input-ul oferit de utilizator.

```
> park BN39GIM White
White car parked in spot 1.
>leave 2
There is no car in spot 2.
> park HD23ABC Green
Green car parked in spot 2.
...(parking 20 cars)...

> park CJ96BOS Red
Sorry, the parking lot is full.
> leave 1
Spot 1 is free.
> park CJ96BOS Red
Red car parked in spot 1.
> exit
```
#### Varianta 3
Tot ce facem e sa adaugam, pe langa comenzile `park` si `leave`, comenzile `create` si `status`

Comanda `create` va crea o parcare cu un anumit numar de locuri. De exemplu, `create 3` va crea o parcare cu 3 locuri.

Comanda `status` va printa toate locurile ocupate, in ordine crescatoare. Pentru fiecare loc, se va printa numarul locului, numarul de inregistrare al masinii si culoarea masinii.
Daca nu este niciun loc ocupat, se va printa `Parking lot is empty`

##### Exemplu:
Simbolul `>` reprezinta input-ul oferit de utilizator.

```
> park BN39GIM White
Sorry, a parking lot has not been created.
> create 3
Created a parking lot with 3 spots.
> status
Parking lot is empty.
> park BN39GIM White
White car parked in spot 1.
> park HD23ABC Green
Green car parked in spot 2.
> park CJ96BOS Red
Red car parked in spot 3.
> leave 2
Spot 2 is free.
> status
1 BN39GIM White
3 CJ96BOS Red
> exit
```
#### Varianta 4
Comanda `reg_by_color` afișează toate numerele de înmatriculare ale mașinilor de o anumită culoare, luând culoarea ca parametru. Culoarea poate fi scrisă cu litere mari sau mici. De exemplu, `reg_by_color black`. Răspunsul ar trebui să conțină numerele de înmatriculare separate prin virgule. Ordinea ar trebui să fie aceeași ca în comanda status. Dacă nu există mașini de această culoare, ar trebui sa printezi: `no black cars found`

Comanda `spot_by_color` este similară cu cea anterioară, dar afișează toate umerele locurilor de parcare unde sunt parcate masini de o anumita culoare.

Comanda `spot_by_reg` îți returnează numărul locului unde este parcată o mașină pe baza numărului său de înmatriculare, de exemplu, spot_by_reg BN39GIM. Această comandă va returna, de asemenea, un mesaj de eroare dacă mașina ta nu a fost găsită: `No cars with number BN39GIM where found`. Pentru comoditate, să presupunem că toate numerele de înmatriculare ale mașinilor sunt unice.

##### Exemplu:
Simbolul `>` reprezinta input-ul oferit de utilizator.

```
> spot_by_color yellow
Sorry, a parking lot has not been created.
> create 4
Created a parking lot with 4 spots.
> park BN39GIM White
White car parked in spot 1.
> park BN39ABC White
White car parked in spot 2.
> park CJ96BOS Red
Red car parked in spot 3.
> park CJ96SSS Red
Red car parked in spot 4.
> reg_by_color GREEN
No cars with color GREEN were found.
> reg_by_color WHITE
BN39GIM, BN39ABC
> spot_by_color GREEN
No cars with color GREEN were found.
> spot_by_color red
3, 4
> spot_by_reg ABC
No cars with registration number ABC were found.
> spot_by_reg BN39ABC
2
> spot_by_reg CJ96BOS
3
> exit
```
### 10. Creaza un sistem de gestiune pentru o sala de cinema 

#### Context:
Clientul tău este o sală de cinema care are nevoie de un sistem de gestiune. Există două tipuri de utilizatori: `admin` (care gestionează sala) și `client` (adică cel care vine să se uite la film).

#### Cerințe pentru `Admin`:
1. **Creează structura sălii**: generează un grid format dintr-un anumit număr de linii și coloane.
2. **Vede statisticile pentru sala sa**:
    - Câte bilete sunt vândute (adică câte locuri sunt ocupate).
    - Care este procentajul de locuri ocupate.
    - Care este suma obținută din vânzări în momentul actual.
    - Care este suma maximă care se poate obține din vânzări dacă se vând toate locurile.
3. **Resetează** toate locurile din sală ca fiind libere.

#### Cerințe pentru `Client`:
1. **Vede structura sălii**: care locuri sunt ocupate și care nu.
2. **Află prețul unui loc** de la un anumit rând și coloană:
    - Dacă numărul total de locuri este mai mic decât 60, prețul este 10.
    - Altfel, dacă numărul total de locuri este mai mare decât 60 și biletul selectat este în prima jumătate, prețul este 10; dacă este în a doua jumătate, prețul este dublu.
3. **Cumpără un bilet** pentru un loc de la un anumit rând și coloană.

#### Enunț Tehnic:

##### **Clasa `CinemaHall`**

- **Atribute**:
    - `numberOfRows`
    - `numberOfCols`
    - `Grid`

- **Metode**:

    - `initializeGridWithEmptySeats()`: Va pune caracterul ‘E’, semnificând “empty”, în fiecare celulă din grid. Adică face ca toate locurile să fie disponibile.
    
    - `showStatistics()`: Va printa în consolă câte bilete sunt vândute, procentajul de locuri ocupate, suma obținută din vânzări până acum și suma maximă care se poate obține din vânzări.
    
    - `printGrid()`: Va afișa în consolă structura sălii de cinema.
    
    - `getPrice(int row, int col)`: Va afișa prețul pentru un loc de la un anumit rând și coloană.
    
    - `buyTicket(int row, int col)`: Va seta locul de la un anumit rând și coloană ca fiind ocupat. Dacă locul este deja ocupat sau nu există, va arunca o excepție `InvalidSeatException`.

##### **Clasa `Main`**

- Creează clasa `Main` unde se testează toate operațiile menționate mai sus.


