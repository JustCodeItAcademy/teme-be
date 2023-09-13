
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
- 
#### Exemplu:
```
Input: {“ana”, “are”, “mere”, “are”}
Output: {ana=1, are=2, mere=1}
```


## Colectii (confortabil)

### 8. Implementeaza un spell checker

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

### 9. Implementeaza un simulator de joc de carti

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

### 10. Implementează un cifru (encryption - decryption)

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
