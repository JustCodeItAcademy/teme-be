
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
Creează o clasă `Person`, care să fie abstractă. 

Atribute:
* `firstName`
* `lastName`

Metode: `introduce()` (care să fie metodă abstractă)

Creează o clasă `Teacher`, care să extindă `Person`

Atribute:
* `department`
* `subject` (adică ce predă profesorul)

Metode: 
* `introduce()` - implementează metoda abstractă din subclasă și afișează un mesaj. 
ex: “I am John Decker, I teach Math and I am a teacher”

Creează o clasă `Student`, care să extindă `Person`

Atribute:
* `groupClass` (adică clasa în care este studentul)

Metode: 
* `introduce()` - implementează metoda abstractă din subclasă și afișează un mesaj. 
ex: “I am Dave Brown, I am in 12A class and I am a student”

### 3. Creează o clasă care să simuleze un adăpost de animale
Creează clasa `Animal`

Atribute:
* `name`
* `age`

Metode:
* metoda abstractă `makeSound()`

Creează clasa `Cat`, care extinde `Animal`

Atribute: niciun atribut nou

Metoda `makeSound()`
* va afișa un mesaj ca de exemplu: “Pisica Tom face miau”

Creează clasa `Dog`, care extinde `Animal`

Atribute: niciun atribut nou

Metoda `makeSound()`
* va afișa un mesaj ca de exemplu: “Câinele Azor latră”

Creează o clasă `Shelter`

Atribute:
* `animals` (adică o listă de animale)

Metode:
* `makeNoise()` - această metodă va face ca toate animalele din listă să scoată sunet
* `addAnimal()` - această metodă va adăuga un animal în lista de animale
* `main()` - în această metodă se vor adăuga animale în lista folosind metoda `addAnimal()`, iar mai apoi se va apela metoda `makeNoise()` pentru ca fiecare animal din listă să facă sunetul corespuzător (de câine sau de pisică, după caz)



### 4. Creează o aplicație de gestionare a conturilor deschise la o bancă pentru un client.
Creează o clasă abstractă numită `BankAccount`

Atribute:
* `balance` (câți bani se află în cont, o valoare de tip `double` care semnifică suma în lei)
* `accountNumber`

Metode: (va trebui să îți dai seama ce returnează și ce parametrii primește fiecare metodă)
* `withdraw()` - metodă abstractă
* `deposit()` - metodă abstractă

Creează o clasă numită `StudentAccount`, care să extindă `BankAccount`

Atribute:
* `maxDepositAmount` - va trebui să nu își schimbe valoarea o dată ce a fost inițializată

Metode: (va trebui să îți dai seama ce returnează și ce parametrii primește fiecare metodă)
* `withdraw()` - se pot retrage maxim câți bani sunt în cont în momentul retragerii
* `deposit()` - se pot depune maxim “maxDepositAmount” bani o dată

Creează o clasă numită `SpendingAccount`, care să extindă `BankAccount`

Atribute:
* `maxWithdrawalAmount` - poate să își schimbe valoarea o dată ce a fost inițializată

Metode: (va trebui să îți dai seama ce returnează și ce parametrii primește fiecare metodă)
* `withdraw()` - se pot retrage cu maxim “maxWithdrawalAmount” RON mai mult decât există în cont în momentul retragerii
  * ex: dacă în cont sunt 5000 de RON, iar maxWithdrawalAmount este 2000 RON, se pot retrage maxim 7000 RON
* `deposit()` - oricâți bani se pot depune în cont

Creează o clasă `Person`

Atribute:
* `firstName`
* `lastName`
* `accountList` - adică un array care ține lista de conturi ale unei persoane

Metode: (va trebui să îți dai seama ce returnează și ce parametrii primește fiecare metodă)
* `addAccount()` - va da posibilitatea persoanei să adauge un cont în lista de conturi
* `listAccounts()` - va printa `accountNumber` împreună cu `balance` pentru fiecare cont din listă
* `deposit()` - va adăuga o anumită sumă de bani într-un cont
* `withdraw()` - va retrage o anumită sumă de bani dintr-un cont
* `checkAccountDetails()` - va printa toate detaliile unui anumit cont
* `main()`

Creează o clasă `BankingApp`

Clasa va avea doar metoda `main()`, unde se va instanția o persoană și se vor testa metodele pe care le poate face persoana (adăugare cont, deposit, etc.).


### 5. Creeaza un program care sa simuleze un cont bancar
Clasa BankAccount va avea urmatoarele atribute:
* sold curent
* moneda contului
* limita maxima de retragere din cont

Clasa BankAccount va avea urmatoarele functionalitati:
* retragerea unei anumite sume de bani (daca nu se depaseste limita maxima de retragere si daca exista suficienti bani)
* depunerea unei anumite sume de bani
* afisarea unui extras de cont cu situatia actuala a contului
* afisarea limitei maxime de retragere din cont

Creeaza mai multe conturi bancare in Main si apeleaza-le comportamentele.  

### 6. Creeaza un mini joc de lupte
Jocul trebuie sa aiba o functie care sa returneze numele castigatorului unei lupte la care participa doi luptatori.
Fiecare lupator ataca pe rand celalalt luptator si cel care il omoara pe celalalt primul, castiga (adica castiga cel care ramane in viata).
Un jucator moare atunci cand health-ul lui este mai mic sau egal cu 0.
Un luptator are urmatoarele atribute:
* health
* damagePerAttack (cat din health i se scade celuilalt jucator, atunci cand jucatorul curent ataca)
* name
Se vor citi de la tastatura atributele celor 2 jucatori, dar si care dintre jucatori va ataca primul.

### 7. Imagineaza-ti ca esti un student cu un ghiozdan.
Ghiozdanul are o anumita capacitate si tu trebuie sa pui niste carti in el.
Fiecare carte are titlu, numar de pagini si greutate.
Poti sa pui carti in ghiozdan pana la o anumita greutate maxima (daca la nu moment dat o carte depaseste greutate maxima, nu poti sa o mai pui in ghiozdan)
Clasa Book va avea atributele:
* title
* numberOfPages
* Weight

Clasa Backpack va avea atributele:
* maxWeight
* currentWeight
* bookList (un array de maxim 30 de carti)
* numberOfBooks (numarul curent de carti din bookList)

Clasa Backpack va avea urmatoarele functionalitati:
* getTotalPages() - va returna numarul total de pagini ale tuturor cartilor din ghiozdan
* getCurrentBooks() - va returna lista de carti care sunt in ghiozdan
* addBook() - va adauga o carte in ghiozdan, daca adaugarea ei nu depaseste greutatea maxima

Intr-o clasa main, instantiaza obiectele de care ai nevoie, pentru a testa functionalitatile.
