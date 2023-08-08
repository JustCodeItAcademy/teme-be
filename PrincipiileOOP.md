
# TEME BACK-END 📚

## Principiile OOP (mai puțin confortabil)

### 1. Construiește o aplicație care să modeleze în cod forme geometrice și operațiile cu ele
Creează o interfață `Shape`

Metode: 
* `computeArea()` - tipul returnat este `double` și nu primește niciun parametru

Creează o clasă `Circle` care implementează interfața `Shape`

Atribute: 
* `radius` (raza cercului)

Metode:
* `computeArea()`

Creează o clasă `Rectangle` care implementează interfața `Shape`

Atribute:
* `height` (lungime)
* `width` (lățime)

Metode:
* `computeArea()`

Creează o clasă `Canvas`, în care să ai o metodă `main` unde vei testa calculul ariei atât pentru cercuri cât și pentru dreptunghiuri

Creează clasa `Dog` care are ca și atribute nume, culoare și rasă.
Comportamentele câinelui sunt "bark" (adică se afișează în consolă "woof") și "run" (adică se afișează în consolă "dog is running").
Creează mai mulți câini în `Main` și apelează-le comportamentele.

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



### 4. Creează o aplicație de gestionare a conturilor deschise la o bancă pentru un client.
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



### 5.Creează o aplicație de plăți

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
