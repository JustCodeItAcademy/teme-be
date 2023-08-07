
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



### 4. Creeaza un program care sa simuleze o masina
Clasa Car are urmatoarele atribute:
* numar de roti
* viteza maxima
* brand
* culoare
* viteza curenta
* treapta curenta de viteza

Clasa Car are urmatoarele functionalitati:
* porneste masina (treapta de viteza devine 1 si viteza curenta devine 1)
* accelereaza (mareste viteza curenta cu o anumita valoare, iar daca se accelereaza cu mai mult de 20 km/ora, treapta de viteza se mareste automat)
* decelereaza (scade viteza curenta cu o anumita valoare, iar daca se decelereaza cu mai mult de 20 km/ora, treapta de viteza se scade automat)
* mareste treapta de viteza
* scade treapta de viteza
* converteste o anumita valoare a vitezei din km/ora in mile/ora

Creeaza mai multe masini in Main si apeleaza-le comportamentele.

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
