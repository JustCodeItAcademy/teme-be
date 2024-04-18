# TEME BACK-END 📚

## Clase si obiecte (mai putin confortabil)

### 1. Creeaza un program care sa simuleze un caine
Creeaza clasa Dog care are ca si atribute nume, culoare si rasa.
Comportamentele cainelui sunt "bark" (adica se afiseaza in consola "woof") si "run" (adica se afiseaza in consola "dog is running").
Creeaza mai multi caini in Main si apeleaza-le comportamentele.

### 2. Creeaza un program care sa simuleze un calculator
Clasa nu are niciun atribut, dar are ca si functionalitati:
* suma a doua numere
* diferenta a doua numere
* factorialul unui numar

Creeaza un calculator in Main si apeleaza-i comportamentele.

### 3. Creeaza un program care sa numere cate pisici se nasc.
Implementeaza o clasa Cat si o metoda getNumberOfCats(), care va returna numarul de pisici create.
Clasa Cat va avea atributele:
* name
* counter - in care vom retine cate pisici s-au creat

Atunci cand o noua pisica se creeaza, counter-ul trebuie sa fie incrementat.

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


### 6. Creeaza un cronometru

Creează o clasă Timer care să gestioneze un cronometru. Clasa Timer va avea următoarele atribute:
* timpul de start
* timpul de stop
* stare cronometru (pornit/oprit)

Funcționalități:
* pornirea cronometrului
* oprirea cronometrului
* resetarea cronometrului
* afișarea timpului scurs

Cauta pe internet ce metode deja existente poti apela pentru a lucra cu timpul (de exemplu, cum poti sa vezi care este timpul prezent - atunci cand pornesti cronometrul)

### 7. Creeaza un mini joc de lupte
Jocul trebuie sa aiba o functie care sa returneze numele castigatorului unei lupte la care participa doi luptatori.
Fiecare lupator ataca pe rand celalalt luptator si cel care il omoara pe celalalt primul, castiga (adica castiga cel care ramane in viata).
Un jucator moare atunci cand health-ul lui este mai mic sau egal cu 0.
Un luptator are urmatoarele atribute:
* health
* damagePerAttack (cat din health i se scade celuilalt jucator, atunci cand jucatorul curent ataca)
* name
Se vor citi de la tastatura atributele celor 2 jucatori, dar si care dintre jucatori va ataca primul.

### 8. Imagineaza-ti ca esti un student cu un ghiozdan.
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
