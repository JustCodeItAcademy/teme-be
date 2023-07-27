# TEME BACK-END 📚

Tocmai ce te-ai angajat intr-un startup si faci parte dintr-o echipa de programatori pe partea de back-end. CEO-ul este o persoana non-tehnica, care doreste sa faca o aplicatie concurenta pentru MyFitnessPal.
MyFitnessPal este o aplicatie din domeniul health care iti permite sa tii evidenta nutritiei tale si sa stii tot timpul cate calorii ai mancat ca sa iti pastrezi sanatatea.

Proiectul este la inceput, iar CEO-ul a venit cu primele cerinte functionale.


## CERINTE FUNCTIONALE:
* Ca si utilizator al aplicatiei, doresc sa pot calcula numarul de calorii ale unui produs, in functie de cantitatea a 3 macronutrienti: proteine, carbohidrati si grasimi.
* Ca si utilizator al aplicatiei, doresc sa pot salva un produs dupa ce ii calculez caloriile
* Ca si utilizator al aplicatiei, doresc sa pot vedea lista de produse pe care le-am salvat
* Ca si utilizator al aplicatiei, doresc sa caut un produs dupa nume si sa ii vad detaliile.
* Ca si utilizator al aplicatiei, doresc sa pot sterge un produs din lista de produse.

Cu aceste cerinte functionale venite de la CEO, a avut loc un meeting de planificare cu colegii si cu team-leader-ul echipei, in care aceste cerinte funcitonale au fost transformate in task-uri concrete de programare.
In urmatoarele 2 saptamani, echipa trebuie sa vina cu primul livrabil (prima versiune a aplicatiei).

## TASK-URI:

### 1. Creeaza clasa Product
Clasa Product va incapsula atributele unui produs:
* Numele produsului
* Numarul de grame de grasimi
* Numarul de grame de carbohidrati
* Numarul de grame de proteine
* Numarul total de calorii
Clasa Product va contine si operatiile pentru un produs
* Metoda computeCalories care tine de clasa 
* Metoda accepta ca si parametrii numarul de grame de grasimi, numarul de grame de carbohidrati si numarul de grame de proteine
* Metoda returneaza numarul total de calorii
Creaza clasa ProductCatalog
Clasa ProductCatalog va avea urmatoarele atribute:
* O lista de produse (maxim 100 de produse sunt acceptate in lista)
* Numar maxim de produse = 100 (constanta)
* Numarul de produse adaugate in lista
Clasa ProductCatalog va contine si urmatoarele operatii:
* Metoda printProducts
  - Metoda nu accepta niciun parametru
  - Metoda nu returneaza nimic, doar printeaza in consola lista de produse
* Metoda addProduct
* Metoda primeste ca parametru un produs
+ Daca produsul se afla deja in lista sau daca lista e deja plina,  se va returna false (adica operatia a esuat)
+ Daca nu se afla deja in lista, se va aduga produsul in lista si se va returna true (adica operatia s-a efectuat cu success)
* Metoda getProductByName
+ Metoda primeste ca parametru numele unui produs
+ Metoda returneaza produsul din lista care are numele egal cu numele primit ca parametru
+ Daca produsul nu a fost gasit, se va returna null
+ Sugestie: pentru compararea stringurilor folositi metoda equals in loc de == (Ex: string1.equals(string2) )
* Metoda deleteProduct
+ Metoda primeste ca parametru numele unui produs
+ Se va cauta produsul in lista de produse dupa nume.
+ Daca produsul nu a fost gasit se va returna  false (adica operatia a esuat)
+ Altfel, produsul va fi sters din lista de produse si se va returna true  (adica operatia s-a efectuat cu success)
+ Sugestie: operatia de cautare a unui produs dupa nume se foloseste in 2 locuri astfel ca se poate crea o metoda privata pentru a cauta produsul dupa nume in lista, care sa returneze indexul din array la care se afla produsul sau -1 daca nu a fost gasit 



### 1. Scrie un program care sa caute un numar de telefon intr-o lista de numere. Programul va printa “numarul a fost gasit” sau “numarul nu a fost gasit”

### 2. Scrie un program care sa adune toate preturile dintr-o lista (ca mai apoi sa fie afisata suma totala in cosul de cumparaturi):
De exemplu, pentru {1, 7, 3, 10, 9}, se va afisa in consola valoarea 30.

### 3. Scrie un program care sa afiseze de cate ori apare un anumit numar n (citit de la tastatura) intr-un array.
De exemplu, pentru {1, 2, 2, 3, 3, 3, 4, 4, 4, 4} si n=3, se va afisa "3 apare de 3 ori".

### 4. Construieste un array bazat pe input-ul utilizatorului.
Cat timp utilizatorul introduce numere de la tastatura (maxim 100 de numere), adauga-le intr-un array si apoi afiseaza elementele array-ului.

### 5. Scrie un program care sa afiseze pretul mediu pe metru patrat, dintr-o lista de preturi ale unor proprietati imobiliare:
De exempu, pentru {1, 7, 3, 10, 9}, se va afisa in consola valoarea 6

### 6. Scrie un program care sa calculeze produsul numerelor impare din intervalul x si y, unde numerele x si y sunt introduse de la tastatura

### 7. Vrei sa pui un discount de n lei (n fiind citit de la tastatura), pentru fiecare produs.
De exemplu, pentru n = 2 si lista de preturi {3, 7, 3, 10, 9}, lista de preturi va deveni {1, 5, 1, 8, 7}

### 8. Vrei sa vezi cat studiezi saptamanal pentru programare
Citeste de la tastatura numarul de zile pe care le-ai petrecut invatand programare.\
Citeste apoi cate ore ai invatat in fiecare din aceste zile.\
Calculeaza media de studiu pe zi.

### 9. Scrie un program care sa afiseze cel mai mare si cel mai mic pret dintr-o lista de preturi.
De exemplu, pentru {1, 7, 3, 10, 9}, se vor afisa in consola valorile 1 si 10

### 10. Scrie un program care sa inverseze elementele unui array. Adica vrei ca utilizatorul sa poata vedea o lista de preturi de la coada la cap: 
De exemplu, pentru {1, 7, 3, 10, 9}, sa va afisa in consola "9, 10, 3, 7, 1"

### 11.Scrie un program care sa afiseze cate numere pare si cate numere impare se afla intr-un array:
De exemplu, pentru {1, 7, 3, 10, 9}, sa va afisa in consola Odd=4; Even=1

### 12. Scrie un program care sa verifica daca un array este sortat crescator

### 13. Scrie un program care verifică dacă un array este palindrom.
Un array este palindrom daca ordinea elementelor este aceeași dacă o parcurgem de la început la sfârșit, sau de la sfârșit la început.

### 14. Scrie un program care afiseaza produsul a cate 2 numere consecutive din array. 
Daca numarul de elemente este impar, ultimul produs va fi numarul insusi.\
De exemplu, pentru {1, 7, 3, 10, 9}, se va afisa in consola 7, 30, 9.\
Explicatie: (7 = 1 * 7, 30 = 3 * 10, 9 = 1 * 9)\

## Arrays (normal)

### 15. Scrie un program care sa evalueze automat raspunsurile date de un student la un quiz.
Ca si input (pe care il poti hardcoda initial) vei avea raspunsurile corecte si raspunsurile date de student.
/De exemplu, pentru:
```json
studentAnswers : {"C", "D", "D", "B", "A", "C", "B"}
teachersAnswers : {"A", "D", "D", "B", "B", "C", "B"}
```
functia va returna 5, deoarece sunt 5 raspunsuri care corespund, la indecsii 1,2,3,5,6.
