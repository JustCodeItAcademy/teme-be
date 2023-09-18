
# TEME BACK-END 📚

## Lambda&Streams (mai puțin confortabil)

### 1. Sorteaza o o lista de persoane dupa nume, utilizand un comparator
Comparatorul nu va fi definit printr-o clasa care sa implementeze interfata Comparator

### 2. Sterge persoanele care nu pot vota
Avand o lista de persoane, sterge din lista persoanele care au varsta mai mica decat 18 ani, folosind expresii lambda.

### 3. Suma numerelor pare
Calculeaza suma numerelor pare dintr-o lista de Integer-uri.
`HINT`: foloseste filter si sum sau foloseste reduce

Rezolva problema si fara expresii lambda.

### 4. Suma numerelor divizibile cu x sau cu y
Scrie o metoda care sa calculeze suma numerelor divizibile cu x sau y (unde x si y sunt primiti ca parametri), dintr-o lista de Integer-uri.
`HINT`: foloseste filter si sum sau foloseste reduce

Rezolva problema si fara expresii lambda.

### 5. Sorteaza numerele dintr-un array
Scrie o metoda care sa sorteze numerele dintr-o lista de Integer-uri, dar inainte de asta sa le transforme in valori pozitive

Ex: 

```Input: [-1,2,-3,4,-5]
Output:[1,2,3,4,5]
````

(`HINT`: map pentru a transforma fiecare numar din negativ in pozitiv, apoi sorted() ca si operatie finala. Foloseste Math.abs() pentru a transforma un numar din negativ in pozitiv)

Rezolva problema si fara expresii lambda

Rezolva problema si fara expresii lambda. 
(`HINT`: foloseste metoda sort din arraylist)



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

