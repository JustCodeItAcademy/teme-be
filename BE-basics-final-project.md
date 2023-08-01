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
* Metoda computeCalories() care tine de clasa 
  - Metoda accepta ca si parametrii numarul de grame de grasimi, numarul de grame de carbohidrati si numarul de grame de proteine
  - Metoda returneaza numarul total de calorii

### 2. Creaza clasa ProductCatalog
Clasa ProductCatalog va avea urmatoarele atribute:
* O lista de produse (maxim 100 de produse sunt acceptate in lista)
* Numar maxim de produse = 100 (constanta)
* Numarul curent de produse adaugate in lista

Clasa ProductCatalog va contine si urmatoarele operatii:
* Metoda printProducts()
  - Metoda nu accepta niciun parametru
  - Metoda nu returneaza nimic, doar printeaza in consola lista de produse
* Metoda addProduct()
  - Metoda primeste ca parametru un produs
  - Daca produsul se afla deja in lista sau daca lista e deja plina,  se va returna false (adica operatia a esuat)
  - Daca nu se afla deja in lista, se va aduga produsul in lista si se va returna true (adica operatia s-a efectuat cu success)
* Metoda getProductByName()
  - Metoda primeste ca parametru numele unui produs
  - Metoda returneaza produsul din lista care are numele egal cu numele primit ca parametru
  - Daca produsul nu a fost gasit, se va returna null
  - Sugestie: pentru compararea stringurilor folositi metoda equals in loc de == (Ex: string1.equals(string2) )
* Metoda deleteProduct()
  - Metoda primeste ca parametru numele unui produs
  - Se va cauta produsul in lista de produse dupa nume.
  - Daca produsul nu a fost gasit se va returna  false (adica operatia a esuat)
  - Altfel, produsul va fi sters din lista de produse si se va returna true  (adica operatia s-a efectuat cu success)
  - Sugestie: operatia de cautare a unui produs dupa nume se foloseste in 2 locuri astfel ca se poate crea o metoda privata pentru a cauta produsul dupa nume in lista, care sa returneze indexul din array la care se afla produsul sau -1 daca nu a fost gasit

### 3. Creeaza clasa CaloriesCounter
Clasa CalorieCounter nu va avea field-uri, ci va contine metoda main (punctul de intrare in aplicatie)
* In main se va afisa un meniu de optiuni pentru utilizator care se va reafisa dupa fiecare alegere efectuata pana cand utilizatorul alege optiunea de a iesii din aplicatie (EXIT)
Pentru afisarea meniului se va creea o alta metoda: printMenu (care va fi apelata in main) 
* Va afisa in consola meniul pentru utilizator
```json
MENIU: 
"1. Adauga produs in calculator si calculeaza-i caloriile"
"2. Calculeaza caloriile pentru un produs fara a fi adaugat in catalog"
"3. Afiseaza toate produsele din catalog si caloriile pentru fiecare"
 "4. Sterge un produs din catalog"
 "5. Gaseste produs dupa nume"
 "6. Iesi din aplicatie"
 "----------------------------------------------------------------”
"Alege actiunea cu numarul:" ;
```
Dupa afisarea meniului se va citi numarul corespunzator optiunii, introdus de utilizator in consola si se va efectua operatia specifiica optiunii alese.\

Pe baza inputului (numarul citit de la consola) se va decide ce operatie trebuie efectuata folosind instructiunea switch. Acest bloc de cod se va incadra intr-o metoda performSelectedAction (care va fi apelata in main dupa citirea inputului) (primeste ca parametru numarul citit din colosa, specific optiunii alese de utilizator si nu returneaza nimic, doar efectueaza operatia specifica numarului introdus). Pe fiecare ramura case din instructiunea switch se va apela pe obiectul de tip ProductCatalog, metoda corespunzatoare optiunii alese.\

Pentru efectuarea operatiilor 1,3,4,5 este nevoie de o instanta a clasei ProductCatalog. Aceasta instanta (obiect) se creeaza in metoda  main inainte de orice linie de cod si se paseaza ca si parametru metodei performSelectedAction (impreuna cu inputul de la consola) pentru a putea fi folosita in efectuarea operatiilor necesare.\

Rezumat Metoda main:
* In metoda main va trebui instantia unui obiect de tip ProductCatalog
* Atat timp cat utilizatorul nu introduce de la consola optiunea 6 (optiunea de iesire din aplicatie), va trebui sa:
  - Se apeleze metoda printMenu - pentru a afisa meniul utilizatorului
  - Sa se citeasca numarul introdus de utilizator (optiunea aleasa)
  - Se apeleze metoda performSelectedAction - pentru a face actiunea aleasa de utilizator
  - Sugestie: orice declarari de variabile (sau obiecte) se vor face in afara intructiunilor repetitive (in interiorul instr. repetitive doar se vor folosi sau se vor initializa)
* Atentie: Toate metodele create in clasa CalorieCounter care se apeleaza in metoda main, trebuie sa contina in semnatura, cuvantul cheie( keyword-ul) static (inaintea tipului returnat)
* Sugestie: Pentru fiecare operatie e nevoie ca inputurile operatiei respective sa fie citite de la tastatura, apoi se va efectua operatia propriu zisa, si apoi se va afisa un mesaj corespunzator (dupa efectuarea operatiei).
Astfel ca, pentru fiecare actiune selectata se poate face cate o metoda separata care incorporeaza toate aceste actiuni (citire, efectuare operatie, afisare mesaj rezultat) care va fi apelata conform optiunii selectate in case-ul instructiunii switch
