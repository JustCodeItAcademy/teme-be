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
### 8. Scrie o functie care accepta un numar n si printeaza urmatorul pattern de marime n:
Exemplu, pentru n = 7:

```
Input : 7
Output :

    *******
    **   **
    * * * *
    *  *  *
    * * * *
    **   **
    *******
```

### 9. Un card de credit (sau debit) este, desigur, un card din plastic cu care plătești pentru produse și servicii.
Pe acest card este imprimat un număr care este și într-o bază de date undeva, astfel încât când folosești cardul pentru a cumpăra ceva, creditorul știe pe cine să factureze. Există multe persoane cu carduri de credit în lume, deci aceste numere sunt destul de lungi: American Express folosește numere de 15 cifre, MasterCard folosește numere de 16 cifre, iar Visa folosește numere de 13 și 16 cifre. Și acestea sunt numere zecimale (0 până la 9), nu binare, ceea ce înseamnă, de exemplu, că American Express ar putea tipări până la 10^15 = 1.000.000.000.000.000 de carduri unice! (Adică, mhm, un cadrilion.)

De fapt, acest lucru este puțin exagerat, deoarece numerele de card de credit au o anumită structură. Toate numerele American Express încep cu 34 sau 37; cele mai multe numere MasterCard încep cu 51, 52, 53, 54 sau 55 (au și alte numere de început posibile pe care nu ne vom concentra acum); iar toate numerele Visa încep cu 4. Dar numerele de card de credit au și un "checksum" încorporat, o relație matematică între cel puțin un număr și altele. Acest checksum permite calculatoarelor (sau oamenilor care iubesc matematica) să detecteze erori de tipar (de exemplu, inversări) fără a interoga o bază de date, care poate fi lentă. Desigur, un matematician necinstit ar putea crea un număr fals care respectă această constrângere matematică, așa că verificarea în baza de date este încă necesară pentru verificări mai riguroase.

Așa că care e formula secretă? Ei bine, majoritatea cardurilor folosesc un algoritm inventat de Hans Peter Luhn de la IBM. Conform algoritmului Luhn, poți determina dacă un număr de card de credit este valid astfel:

* Înmulțești fiecare a doua cifră cu 2, începând cu penultima cifră a numărului, și adaugi cifrele acelor produse.
* Adaugi suma la suma cifrelor care nu au fost înmulțite cu 2.
* Dacă ultima cifră a totalului este 0 (sau, mai formal, dacă totalul modulo 10 este congruent cu 0), numărul este valid!
Hai să încercăm un exemplu cu un card Visa cu numarul: 4003600000000014.

Inmulțim fiecare a doua cifra cu 2:

1•2 + 0•2 + 0•2 + 0•2 + 0•2 + 6•2 + 0•2 + 4•2

Asta ne dă:

2 + 0 + 0 + 0 + 0 + 12 + 0 + 8

Acum adăugăm cifrele acelor produse împreună:

2 + 0 + 0 + 0 + 0 + 1 + 2 + 0 + 8 = 13

Acum adăugăm acea sumă (13) la suma cifrelor care nu au fost înmulțite cu 2:

13 + 4 + 0 + 0 + 0 + 0 + 0 + 3 + 0 = 20

Da, ultima cifră din acea sumă (20) este un 0, deci cardul lui David este autentic!

Scrie un program care valideaza un card Visa.

### 10. Avand la dispozitie o lista de litere, gaseste secventa de litere de cea mai mare lungime din lista, care reprezinta un palindrom.
