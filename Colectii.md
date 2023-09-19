
# TEME BACK-END 📚

## Colectii (mai puțin confortabil)

### 1. Implementeaza un PhoneBook

#### Atribute: 
- **contacts**: o lista de String-uri reprezentand numere de telefon
- **blackList**: o lista de String-uri reprezentand numere de telefon blocate

#### Metode:

#### filterContacts()
- Metoda statica
- Acceptă ca și parametri:
  - o lista de contacte valide
  - o lista de contacte blocate
- Trebuie să șteargă din lista de contacte valide toate numerele care se regăsesc în lista de contacte blocate
- Returnează lista de contacte valide modificată

#### addToBlackList()
- Metoda non-statică
- Adaugă numărul primit ca parametru în lista de numere blocate și îl șterge din lista de contacte

#### removeFromBlackList()
- Metoda non-statică
- Adaugă numărul primit ca parametru în lista de numere și îl șterge din lista de numere blocate

### 2. Scrie o metoda care:
- primeste ca si parametru o lista de numere si returneaza o alta lista de numere formata din numerele din lista primita ca parametru, ridicate la patrat (puteti folosi Math.pow(2) pentru a ridica la patrat)

#### Exemplu: 
```
Input: {2,3,4,5}
Output: {4,9,16,25}
```

### 3. Scrie o metoda care:
- Gaseste cuvantul cel mai lung dintr-o lista de cuvinte (primita ca parametru), si il returneaza

#### Exemplu:
```
Input: {“ana”, “are”, “mere”}
Output: “mere”
```

### 4. Scrie o metoda care:
- Primeste ca parametru 2 liste de numere si returneaza un set format din numerele pozitive din ambele liste primite ca parametru
  
#### Exemplu:
```
Input: {1, -2, 3, 4, 4, -5}, {1, -7, 2}
Output: {1, 3, 4, 2}
```

### 5. Scrie o metoda care:
- Primeste ca si parametru o lista de cuvinte si returneaza lista de cuvinte inversata, cu mentiunea ca lista inversata nu va include cuvintele care au lungimea mai mica decat 3
- 
#### Exemplu:

```
Input: {“ana”, “nu”, “are”, “mere”}
Output: {“mere”, “are”, “ana”}
```

### 6. Scrie o metoda care:
- Primeste ca parametru doua set-uri si returneaza true daca primul set primit ca parametru este superset al celui de-al doilea set
- Un set “set1” este superset al altui set “set2”, daca “set1” contine toate elementele din “set2”, dar seturile nu sunt egale   - containsAll()

#### Exemple:

```
Input1: {“ana”, “are”, “mere”}, {“ana”, “are”}    
Output1: true
Input2: {“ana”, “are”, “mere”}, {“ana”, “are”, “mere”}
Output2: false
```

### 7. Scrie o metoda care:
- Primeste ca parametru o lista de cuvinte si returneaza de cate ori apare fiecare cuvant in lista

#### Exemplu:
```
Input: {“ana”, “are”, “mere”, “are”}
Output: {ana=1, are=2, mere=1}
```

### 8. Gestiunea angajatilor din companie
O companie multinationala are o lista de angajati, iar fiecare angajat este caracterizat de: varsta, tara, nume.

Scrie urmatoarele metode:
- O metoda care returneaza angajatii care au peste 50 de ani, din companie
- O metoda care returneaza o lista cu angajatii din Romania
- O metoda care sorteaza angajatii dupa tara
- O metoda care sorteaza angajatii dupa nume
- O metoda care returneaza o mapa, in care cheia este tara si valoarea este numarul de angajati din acea tara
- O metoda care returneaza o mapa, in care cheia este tara si valoarea o lista cu toti angajatii din acea tara

### 9. Scrie o aplicatie pentru bursa
O bursa este structurata sub forma unei mape, cu cheia fiind numele companiei si valoarea fiind pretul unei actiuni la acea companie.

Exemplu: {Oracle=56, Google=421, Tesla=950}

Scrie 2 metode:
- O metoda care sa gaseasca compania cu cel mai mare pret al unei actiuni din mapa
- O metoda care sa gaseasca pretul mediu al preturilor actiunilor din mapa

### 10. Gestiunea produselor dintr-un magazin

Într-un magazin există produse, caracterizate de **nume**, **preț**, **categorie**. Categoria este un enum, care are valorile `LACTATE`, `MEZELURI`, `LEGUME&FRUCTE`. Task-ul este să grupăm produsele după categorii.

Astfel, avem:
- Clasa **Product**
- Enum-ul **Category**

Într-o clasă **Shop**, avem atributul `products`, care este o mapă având cheia **Category** (care este un enum) și valoarea o listă de produse (din acea categorie).

#### Metode:

##### Add product
- Adaugă un produs nou în mapa.
- Dacă categoria produsului există deja, se va adăuga produsul la acea categorie în mapa, altfel se va crea o nouă categorie în care va fi inițial produsul adăugat.

##### getProductByCategory
- Va returna toate produsele dintr-o anumită categorie.

##### getAllCategories
- Va returna toate categoriile din mapa.

##### deleteProduct
- Va șterge un produs din mapa.

### 11. Scrie o metoda care:
- Primeste ca parametru o lista de numere, care are un element duplicat
- Returneaza elementul duplicat
  
**HINT**: (alt mod de rezolvare decat cel clasic): metoda add din interfata Set returneaza false, daca nu poate adauga elementul primit ca parametru in set

### 12. Scrie o metoda care:
- Primeste ca parametru o lista de numere
- Afiseaza cel mai mic si cel mai mare element din lista
  
**HINT**: (alt mod de rezolvare decat cel clasic): adauga toate elementele din lista intr-un treeset, apoi apeleaza metodele first() si last() pe acel treeset

## Colectii (confortabil)

### 13. Implementeaza un spell checker

Cel mai simplu spell checker este bazat pe o lista de cuvinte cunoscute (un dictionar). Daca scrii un text, fiecare cuvant trebuie cautat in lista de cuvinte cunoscute, iar daca nu este gasit, inseamna ca e eronat. Implementeaza un astfel de spell checker.

#### Ce intra in program?

1. Pe prima linie utilizatorul introduce numărul de cuvinte din lista de cuvinte cunoscute.
2. Apoi, pe câte o linie separată introduce fiecare cuvant din lista de cuvinte cunoscute.
3. Apoi, pe o linie, se introduce numărul de linii al textului de verificat.
4. Se introduc exact atâtea linii cu text (cuvinte separate prin spațiu).

#### Ce iese din program?

- Trebuie să afișam acele cuvinte din text care nu se regăsesc în lista de cuvinte cunoscute.
- Trebuie să verificăm fără să ținem cont de literele mici și mari.
- Cuvintele care nu sunt găsite în dicționar nu ar trebui să fie duplicate, dacă le regăsim de mai multe ori în text.

#### Exemplu

##### Input:
```
3
a
bb
cCc
2
a bb aab aba
ccc c bb aaa
```

##### Output:
```
c
aab
aaa
aba
```

### 14. Implementeaza un simulator de joc de carti

#### Scrie clasa **Deck**

##### Atribute:
- **Suit**: o listă cu tipurile de cărți (ex: “trefla”, “rosu”, etc.)
- **Rank**: o listă cu numerele de cărți (ex: “2”, “3”, “as”)
- **DeckCards**: o listă de cărți

##### Metode:

###### GenerateDeck()
- Va popula lista de cărți (`deckCards`) în funcție de `rank` și `suit`, adică va genera String-uri cu toate combinațiile posibile (ex: “2 de trefla”, “as de rosu”, etc.), pe care le va adăuga în `deckCards`.

###### suffleDeck()
- Va amesteca lista de cărți `deckCards` (hint: `Collections.shuffle()`)

#### Scrie clasa **Player**

##### Atribute:
- **name**

##### Metode:

###### dealHand()
- Primește ca parametru un deck și numărul de cărți care se vor genera într-o “mână”.
- De exemplu, dacă numărul de cărți este 4, atunci funcția va returna o listă de genul: “[2 de trefla, 3 de rosu, 5 de negru, as de rosu]”.
- Această listă de fapt este o sublistă cu ultimele 4 cărți din lista de cărți (`deckCards`) a pachetului (`deck`) primit ca parametru. (hint: metoda `subList()`)

#### Scrie clasa **Main**

- Aici se va construi array-ul `suit`, array-ul `rank` și se va construi un obiect de tip `Deck` (care va fi inițializat cu `suit` și `rank`).
- Se va genera pachetul.
- Se vor crea niște jucători și se vor adăuga într-o listă.
- Pentru fiecare jucător din listă, se va amesteca pachetul și se va apela metoda `dealHand()`.

### 15. Implementează un cifru (encryption - decryption)

Cel mai simplu cifru este definit de o regulă în care fiecare caracter este codificat prin alt caracter.

De exemplu, dacă un cifru are la dispoziție:
- Caractere valide: {'a', 'e', 'i', 'o', 'u', 'c', 'n', 'd', 'b', 's', 'l', 'm'}
- Codificările caracterelor valide: {'s', 't', 'n', 'f', 'g', 'h', 'j', 'k', 'x', 'y', 'z', 'q'}

Atunci când încercăm să codificăm cuvântul “slab”, vom obține “yzsx”.
Iar atunci când încercăm să decodificăm “qsjs”, vom obține “mana”.

Asigură operațiile de codificare și decodificare pentru un cuvânt, având la dispoziție lista de caractere valide și lista de caractere codificate.

#### Creează clasa Cypher

##### Atribute:
- **inputChars**: (lista de caractere valide)
- **outputChars**: (lista de caractere codificate)

##### Metode:

###### initializeCypher()
- Construiește o mapă în care fiecare cheie este un caracter și fiecare valoare este codificarea caracterului. 
- De exemplu, pentru exemplul de mai sus, mapa va arăta așa: {a=s, b=x, c=h, d=k, e=t, i=n, l=z, m=q, n=j, o=f, s=y, u=g}

###### encrypt()
- Primește ca parametru un cuvânt și returnează cuvântul codificat

###### decrypt()
- Primește ca parametru un cuvânt și returnează cuvântul decodificat

#### Creează clasa Main

- Aici vor fi apelate metodele cifrului

### 16. Implementează o librărie

Librăria va trebui să conțină o colecție de cărți. Fiecare carte are atributele: `year`, `title`, `genre` (gen) și `author`.

Librăria va trebui să implementeze următoarele funcționalități:
- Afișarea cărților ordonate după `year`
- Afișarea cărților ordonate după `autor`
- Gruparea cărților după `genre`	
- Afișarea tuturor cărților dintr-un anumit gen 
- Afișarea tuturor genurilor împreună cu toate cărțile din fiecare gen 
- Afișarea tuturor genurilor 
- Adăugarea unei cărți
- Ștergerea unei cărți

#### Creează clasa Book

##### Atribute:
- **Year**
- **Title**
- **Genre**
- **Author**

##### Metode:

###### compareTo 
(suprascrisă din interfața Comparable)
- Va compara cărțile după `year`

#### Creează clasa AuthorComparator

- Va implementa interfața Comparator
- Va suprascrie metoda `compare()` pentru a compara două cărți după autor (se va apela metoda `compareTo()` pentru String-uri)

#### Creează clasa BookStore

##### Atribute:
- **Books**: va fi un set 

##### Metode:

###### addBook()
- Adaugă o carte primită ca parametru în set-ul `books`

###### deleteBook()
- Șterge cartea primită ca parametru din set-ul `books`

###### getAllBooksOrderedByYear()
- Va returna valoarea atributului `books`

###### getAllGenres()
- Va returna un set cu toate genurile existente în colecția de cărți

###### getAllBooksOrderedByAuthor()
- Va returna un TreeSet care va folosi AuthorComparator pentru a sorta cărțile după autor

###### getAllBooksByGenre()
- Va construi o mapă, în care cheia este un gen, iar valoarea este set-ul de cărți care au acel gen
- Va returna această mapă (toate genurile, cu toate cărțile din fiecare gen)
(HINT: mapă cu cheia `gen`, iar valoarea lista de cărți cu acel gen)

###### getBooksByGenre()
- Va primi ca parametru un gen
- Va returna toate cărțile care au acel gen
(HINT: valoarea de la o anumită cheie din mapă)

### 17. Scrie o metoda care:
- Primeste ca parametrii doua cuvinte si returneaza true, daca cuvintele sunt anagrame.
  
Exemple:
```
Input1: “race”, “care”
Output1: true, pentru ca care contine aceleasi litere ca si race, si literele apar de acelasi numar de ori
Input2:”race”, “carec”
Output2: false, pentru ca nu contin acelasi litere, de acelasi numar de ori
```
### 18. Implementeaza functionalitatile unui cos de cumparaturi
Intr-un magazin exista produse, caracterizate de nume, pret, categorie. Categoria este un enum, care are valorile “LACTATE”, “MEZELURI”, “LEGUME&FRUCTE”

Astfel, vom avea clasa Product si enum-ul Category.

Clasa ShoppingCart va avea ca atribut o mapa, in care ca si cheie este produsul, iar ca si valoare este cantitatea (cate produse de acel fel) sunt in cosul de cumparaturi.

Implementeaza in ShoppingCart functionalitatile de:
- Adaugare produs in cosul de cumparaturi (in mapa)
- Calcul pret total al produselor cosul de cumparaturi (din mapa)
- Stergerea unui produs cu totul din cosul de cumparaturi (din mapa)
- Stergerea unui anumit numar de bucati al unui produs din cosul de cumparaturi (din mapa)


### 19. Java Adventure Game Challenge:

You are tasked with creating a basic text-based adventure game in which the player can navigate through various locations.

Specifications:

- The game will consist of multiple locations, each having a unique identifier and a description.
- Each location can have exits leading to other locations.
- The program should print the current location's description and available exits.
- Players should be able to move between locations by specifying a direction.
- The player should be able to type commands such as "Go West", "run South", or just "East", and the program should move to the appropriate location if there is one.
- If a player attempts to move in an invalid direction, the program should print a message indicating this and remain in the current location.
- For ease of play, single letter commands like "N", "W", "S", "E", "Q" should still be valid commands for navigating and quitting.
- There should be a vocabulary map that associates full words like "NORTH", "WEST", "SOUTH", "EAST", "QUIT" to their respective single-letter commands.
- Players can use multiple words in their command. The program should recognize the valid direction from the command.
- The game continues until the player reaches the location with ID 0, which will end the game.

Implementation Details:

- Use the Main class for game logic.
- Use the Location class to define locations. Each location should store its ID, a description, and a map of exits (where the key is the direction of exit and the value is the location id of the exit). Every location automatically has a "Q" exit, leading to location ID 0.
- The game starts with the player in the location with ID 1.
- If a player's input has multiple words, split the input and check the vocabulary map to translate full words to their respective single-letter commands. The vocabulary map is a map with entries like this: "SOUTH"="S", "NORTH"="N", etc.

Example of a game session:

```
You are standing at the end of a road before a small brick building.
Available exits are W, E, S, N.

> Go West

You are at the top of a hill.
Available exits are N.

> N

You are in the forest.
Available exits are S, W.

> run South

You are standing at the end of a road before a small brick building.
Available exits are W, E, S, N.

> East

You are inside a building, a well house for a small spring.
Available exits are W.

> Q

You are sitting in front of a computer learning Java.
```

In this session, the player starts at the road (location 1) and chooses to go west to the hill (location 2). From the hill, they proceed north to the forest (location 5). Deciding to head south, they return to the road. Curious about what lies to the east, they explore the building (location 3). Finally, they decide to quit the game, ending up "sitting in front of a computer learning Java."

## Colectii (proiecte finale)
### 19. IMDB clone
Un film este caracterizat de title, releaseYear, genre, cast (lista de actori), type, reviews (lista de review-uri)

Genre poate fi DRAMA, COMEDY, sau ACTION. Type poate fi MOVIE sau TV_SHOW.

Un review poate sa fie ONE_STAR, TWO_STARS, THREE_STARS, FOUR_STARS, FIVE_STARS.

Un actor are nume si prenume.

Un utilizator al aplicatiei are nume, prenume si o lista de filme favorite. Utilizatorul poate fi de doua tipuri: admin sau client.

Creeaza o clasa UserService
- Adaugarea unui review la un film
- Adaugarea unui film la o lista de filme favorite

Creeaza o clasa IMDBService, care sa aiba o lista de filme si care sa implementeze urmatoarele operatii:
- Gruparea tuturor filmelor dupa gen
- Gasirea tuturor filmelor in care joaca un anumit actor
- Ordonarea filmelor dupa anul aparitiei
- Ordonarea filmelor dupa review-uri, descrescator (de la media de review-uri cea mai buna in jos)
- Gasirea tuturor actorilor care au jucat in filme de un anumit tip si gen
- Gasirea celui mai apreciat film de un anumit tip si gen
- Gasirea autorului care a jucat in cele mai multe filme
- Cele mai populare n filme (bazat pe cat de des apar acele filme apar in listele de filme favorite ale utilizatorilor)

### 20. Budget Manager	
Aplicatia le va permite utilizatorilor sa isi gestioneze bugetul.

O cheltuiala (purchase) este caracterizata de nume, pret si categorie

Categoriile pot fi: mancare, distractie, haine, utilitati, altele. 

Un utilizator va avea o lista de cheltuieli si un buget maxim.

Ca si utilizator in aplicatie, vei avea acces la mai multe functionalitati:
- Vizualizarea tututor cheltuielilor
- Vizualizarea cheltuielilor dintr-o anumita categorie
- Vizualizarea cheltuielilor grupate pe categorii
- Vizualizarea categoriei in care a cheltuil cel mai mult/mai putin
- Vizualizarea tuturor cheltuielilor dintr-un interval de pret
- Sortarea tuturor cheltuielilor dupa pret
- Sortarea cheltuielilor dintr-o anumita categorie dupa pret
- Salvarea tuturor cheltuielilor intr-un fisier
- Incarcarea in aplicatie a tuturor cheltuielilor dintr-un fisier
- Setarea unui buget
- Vizualizarea bugetului disponibil
- Adaugarea unei cheltuieli
- Stergerea unei cheltuieli

### 21. Booking system (booking.com clone)
Dezvolta un sistem de rezervari la hotel asemanator cu booking.com

Aplicatia va avea 2 tipuri de utilizatori: administratori de hotel si clienti.

O camera are numar, pret pe noapte, numar de persoane care pot fi cazate si o lista de rezervari

O rezervare poate fi facuta pentru o camera, de catre un client, intre doua date (check in si check out).

Un utilizator are o lista de rezervari, nume, prenume.

Administratorii de hotel vor putea sa:
- Managerieze camerele 
- Adaugare camera
- Stergere camera
- Vizualizare camere
- Editare pret camera
- Sa vada cate camere sunt libere/ocupate pentru o anumita perioada
- Sa vada care este pretul obtinut din toate rezervarile dintr-o anumita perioada

Clinetii vor putea sa:
- Vada disponibilitatile (camerele libere) pentru o anumita perioada si un anumit numar de locuri
- Adica sa vada care camere sunt disponibile intr-o anumita perioada
- Sorteze disponibilitatile (camerele libere) dupa pret pentru o anumita perioada si un anumit numar de locuri
- Faca o rezervare pentru o anumita camera

Dupa ce aceasta versiune a aplicatiei functioneaza, permite ca in aplicatie sa existe mai multe hoteluri. Administratorul va putea adauga si hotel in aplicatie.

### 22. Joc de carti
Dezvoltati o aplicatie Java pentru simularea jocurilor de carti: 
- BlackJack
- Poker
Pentru a juca este nevoie de jucatori(Player) care sunt caracterizati de nume.

Pentru tipurile de joc, mai este nevoie de un set de carti(Card) care sunt caracterizate de: 
- numar(1-15) 
- simbol(rosu - hearts, negru - spades, romb - diamonds, trefla - clubs). 

Un joc este caraterizat de:
- Nr. de jucatori (BlackJack - maxim 6, Poker - maxim 4)
- setul de carti
- lista de jucatori

Ambele jocuri au casi comporttamente comune:
- a juca (play) 
- a imparti cartile(deal).
 Fiecare joc implementeaza diferit metodele play, deal. 

La impartirea cartilor(deal) se distribuie fiecarui jucator  un subset de carti din setul predefinit al jocului curent astfel ca se genereaza pentru fiecare player(cheie) un set de carti aleator(valoare). 

Pentru jocul de BlackJack se distribuie cate 5 carti fiecarui jucator si castiga jucatorul care are suma cartilor cea mai apropiata de 21.

Pentru Poker se distribuie cate 8 carti fiecarui jucator si castiga  jucatorul cu cea mai mare carte. 

Pentru pornirea jocurilor se creeaza o clasa GameStarter care contine metoda de start in interiorul careia se fac declararile si initializarile pentru un anumit joc. 

Daca se incearca inceperea unui joc u un numar mai mare de jucatori decat cel suportat de jocul respectiv, se genereaza o exceptie NoOfPlayersNotSuportedException 

Totodata sa se creeze o clasa de test pentru diferite scenarii ale metodei play.

## Algoritmica (rezolvari folosind colectii)

### 1. Afla profitul maxim pe care il poti face cumparand si vanzand actiuni.
Ca si input ai un array cu preturile unei actiuni in fiecare zi. Va trebui sa determini in ce zi trebuie sa cumperi si in ce zi trebuie sa vinzi ca sa obtii profitul maxim

Exemplu:
```
Input: [100, 180, 260, 310, 40, 535, 695]
Output: Cumpara in ziua 5 (la pretul de 40) si vinde in ziua 7 (la pretul de 695), adica profit maxim 695-40=655
Input2: [2, 3, 10, 6, 4, 8, 1]
Output: Cumpara in ziau 0 (la pretul de 2) si vinde in ziua 2 (la pretul de 10), adica profit maxim 10-2=8
```

### 2. Inlocuieste fiecare element dintr-un array cu produsul tuturor celorlalte elemente
Exemplu: 
```
Input: { 1, 2, 3, 4, 5 }
Output: { 120, 60, 40, 30, 24 }
```
(hint: foloseste un alt array in care sa pui rezultatul)

### 3.Sa se verifice daca un array contine duplicate
Exemplu:
```
Input: [6,5,6,2,3,1]
Output: true, pentru ca 6 apare de doua ori
```
(hint: construieste o mapa care sa numere de cate ori apare fiecare element din lista)

### 4. Sunt afisate n-1 numere dintr-un interval de la 1 la n. Sa se gaseasca numarul care lipseste.
Exemplu:
```
Input: n=7, a=[3,2,1,6,5,7]
Output: 4 - lipseste doar 4 din array.
```
(hint: sorteaza array-ul si verifica daca gasesti o diferenta de 2 intre 2 elemente consecutive. Un gasesti diferenta, acolo va fi si numarul care lipseste. Gandeste-te apoi si la alta metoda de rezolvare)

### 5. Grupeaza elementele dintr-un array astfel incat elementele duplicate sa fie unul langa altul
Exemplu:
```
Input: { 1, 2, 3, 1, 2, 1 }
Output: { 1, 1, 1, 2, 2, 3 }
```
(hint: construieste o mapa in care cheia este elementul, iar valoarea de cate ori apare. Apoi construieste rezultatul parcurgand mapa si adaugand elementele unul dupa altul intr-un nou array, in functie de mumarul de aparitii al fiecarui element)


### 6. Gaseste diferenta maxima intre 2 numere dintr-o lista, astfel incat elementul mai mic sa apara inaintea elementului mai mare
Exemplu: 
```
Input: [2,7,9,5,1,3,5]
Output: 7 (perechea de numere care indeplineste conditia este (2,9)
```

### 7. Muta toate zero-urile dintr-un array la final
Exemplu: 
```
Input: [6,0,8,2,3,0,4,0,1]
Output: [6,8,2,3,4,1,0,0,0]
```

### 8. Gaseste un subarray dintr-un array,  care sa aiba o anumita suma 
Un subarray are capatul din stanga inaintea capatului din dreapta in array-ul original.
Array-ul original poate avea doar numere pozitive

Exemplu: 
```
Input: [1,4,20,3,10,5], sum=33
Ouput:suma a fost gasita intre indicii 2 si 4 (20+3+10=33)
Input: [1,4], sum = 0
Output: niciun subarray nu a fost gasit
```

### 9. Roteste un array la stanga cu o pozitie
Exemplu: 
```
Input: [1,2,3,4,5]
Output: [5,1,2,3,4]
```
Rezolva apoi problema in mod general, adica roteste un array la stanga cu n pozitii
Exemplu: 
```
Input: [1,2,3,4,5] , n=2
Output: [3,4,5,1,2] - array-ul s-a rotit cu 2 pozitii
```

### 10. Inverseaza un array fara sa folosesti un alt array

