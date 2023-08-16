# TEME BACK-END 📚

## Algoritmi 

### 1. Implementează în Java un program astfel încât să simuleze alegeri cu votul majoritar.
#### Clasa Candidat
Ar trebui să creezi o clasă numită `Candidate` care să aibă următoarele proprietăți:
* `name` - Numele candidatului
* `numberOfVotes` - Totalul voturilor primite de candidat

#### Clasa Election
Va avea o lista de candidati si urmatoarele functionalitati:

##### Funcția vote
Creeaza funcția `vote` care:
* Primește un singur argument, `name`, reprezentând numele candidatului pentru care s-a votat.
* Dacă `name` corespunde cu numele unui candidat, actualizează totalul de voturi al candidatului.
  * Funcția ar trebui să returneze `true` pentru un vot valid.
* Dacă `name` nu corespunde, funcția returnează `false`, indicând un vot invalid.

> **Notă**: Poți presupune că nu există doi candidați cu același nume.

##### Funcția declareWinner
Completează funcția `declareWinner`:
* Afișează numele candidatului cu cele mai multe voturi.
* Dacă există un egalitate, afișează numele fiecărui candidat câștigător, fiecare pe o linie nouă.

#### Exemplu, pentru 3 candidati: Alice, Bob si Charlie:
```
Number of voters: 4
Vote: Alice
Vote: Bob
Vote: Charlie
Vote: Alice
Alice is the winner
```
### 2. Scrie un program care citește un șir de numere întregi și două numere n și m. Programul trebuie să verifice că n și m nu apar niciodată unul lângă celălalt (în orice ordine) în șir.

### 3. Scrie un program care citește un șir de numere întregi și afișează numărul de "triplete" din șir. 
Un "triplet" reprezintă trei numere întregi consecutive în ordine crescătoare, care diferă cu 1 (de exemplu, 3,4,5 este un triplet, dar 5,4,3 și 2,4,6 nu sunt).

### 4. Scrie o functie care primeste un string, in care exista mai multe cuvinte separate prin spatiu.
Returneaza cel mai lung cuvant din acel string.

### 5. Scrie o functie care primeste un array si un numar n.
Returneaza decate ori apare numarul n in array.

Acum transforma functia in felul urmator: functia va primi, in plus si un numar k.
Returneaza index-ul celei de-a k aparitii a numarului n in array.
De exemplu, pentru `19 14 17 15 17`, indexul celei de-a 2-a aparitii a lui 17 in array este 5.

### 6. Scrie o functie care accepta 2 numere reprezentand anul si luna.
Functia va returna prima si ultima zi din luna.

De exemplu, pentru anul `2017` si luna `1`, functia va returna "2017-01-01 2017-01-31"
Foloseste-te de functiile deja existente in clasa LocalDate.

### 7. Scrie o functie care accepta un array bidimensional (o matrice) si doua numere: i si j.
Interschimba coloanele cu indicii i si j din matrice.

De exemplu, pentru matricea:

```
11 12 13 14
21 22 23 24
31 32 33 3
```

Daca vrem sa interschimba coloana 0 cu coloana 1, matricea va deveni:

```
12 11 13 14
22 21 23 24
32 31 33 34
```
