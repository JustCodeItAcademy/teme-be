
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

### 2. Implementeaza un spell checker

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

### 3. Implementeaza un simulator de joc de carti

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
