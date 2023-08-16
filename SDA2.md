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



