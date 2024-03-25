# TEME BACK-END 📚

## While loops (mai putin confortabil)

### 1. Scrie un program care afiseaza numerele de la 1 la n, n fiind citit de la tastatura

### 2. Scrie un program care afiseaza suma numerelor de la 1 la n

### 3. Scrie un program care afiseaza numerele pare din intervalul [1-n].

### 4. Scrie un program care afiseaza suma numerelor pare din intervalul [1-n].

### 5. Scrie un program care afiseaza cate numere pare sunt in intervalul [1-n].

### 6. Scrie un program care afiseaza numerele divizibile cu 3 din intervalul [1-n].

### 7. Scrie un program care afiseaza suma numerelor divizibile cu 3 din intervalul [1-n]

### 8. Scrie un program care afiseaza cate numere divizibile cu 3 sunt in intervalul [1-n]

### 9. Scrie un program care afiseaza numerele din sirul fibonacci pana la maxim n, n fiind citit de la tastatura.
Sirul fibonacci are urmatoarea regula: fiecare numar din sir este egal cu suma precedentelor doua numere din sir.
Primele doua numere sunt intodeauna 0 si 1.
```json
0, 1, 1, 2, 3, 5, 8, 13, 21, ...
```

### 10. Scrie un program care calculeaza factorialul unui numar n, n fiind citit de la tastatura
De exemplu, factorialul numarului 3 este 1 * 2 * 3 = 6\
Factorialul numarului 4 este 1 * 2 * 3 * 4 = 24\
Factorialul numarului 5 este 1 * 2 * 3 * 4 * 5 = 120\
Practic trebuie inmultite toate numerele consecutive pana la numarul citit de la tastatura.

### 11. Scrie un program care sa calculeze suma cifrelor unui numar, numarul fiind citit de la tastatura.

## While loops (normal)

### 12. Scrie un program care inverseaza cifrele unui numar, numarul fiind citit de la tastatura.
Bazeaza-te pe faptul ca ultima cifra a oricarui numar este, de fapt, restul impartirii acelui numar la 10.
In plus, catul impartirii acelui numar la 10 este, de fapt, numarul initial, fara ultima cifra.

### 13. Scrie un program care afiseaza daca un numar este, sau nu, palindrom, numarul fiind citit de la tastatura.
Un numar este palindrom daca ramane la fel atunci cand cifrele ii sunt inversate.
De exemplu, numarul 12321 este palindrom deoarece atunci cand e inversat, este tot 12321.

### 14. Scrie un program care afiseaza cel mai mare divizor comun al doua numere, citite de la tastatura.
De exemplu, pentru numerele 21 si 15, cel mai mare divizor comun este 3.\
3 este cel mai mare numar la care si 21 si 15 se impart exact.\

### 15. Scrie un program care sa determine cat timp (in ani) ii ia unei populatii sa ajunga la o anumita marime.
Initial, pornim cu o populatie de n oi. In fiecare an, n/3 oi noi se nasc, si n/4 oi mor.\
\
De exemplu, daca am pornit cu o populatie de n = 1200 de oi, in primul an 1200/3=400 de oi se nasca si 1200/4=300 de oi mor.\
Asa ca la sfarsitul anului vom avea 1200 + 400 - 300 = 1300 oi
\
Citeste de la tastatura populatia initiala (startSize) si populatia la care vrei sa ajungi (endSize)\
* Daca utilizatorul introduce un startSize mai mic decat 9, cere-i sa introduca valori in continuare pana cand introduce minim numarul 9
* Daca utilizatorul introduce un endSize mai mic decat startSize-ul introdus enterior, cere-i sa introduca valori in continuare pana cand introduce o valoare mai mare decat startSize
\
Programul trebuie sa calcueze numarul de ani necesari ca populatia sa creasca la valoarea endSize

### 16. Scrie un program care sa determine in cati ani economiile tale vor creste la target-ul pe care ti l-ai propus.
Sa presupunem ca deschizi un cont de economii cu o suma initiala de bani, la care se adauga in fiecare an o dobanda.\
\
De exemplu, daca deschizi un cont de 1000 de lei cu o dobanda anuala de 10%, dupa primul an vei avea 1000 + 0.1 * 1000 = 1100 de lei.\
Apoi, dupa al doilea an vei avea 1100 + 0.1 * 1100 = 1210\
Si tot asa, in fiecare an.\
\
Citeste de la tastatura suma initiala, procentul de dobanda anual, si suma target la care vrei sa ajungi.\
Apoi calculeaza cati ani e nevoie sa treaca pana ca in cont sa ajungi la suma target.\

### 17. Creeaza un guessing game.
Programul tau trebuie sa genereze un numar random (intre 1 si 100), iar apoi sa ii ceara utilizatorului sa il ghiceasca.
* Daca numarul dat de utilizator este mai mic decat numarul generat, atunci afiseaza mesajul "Prea mic, mai incearca" si da-i posibilitatea utilizatorului sa introduca un nou numar.
* Daca numarul dat de utilizator este mai mare decat numarul generat, atunci afiseaza mesajul "Prea mare, mai incearca" si da-i posibilitatea utilizatorului sa introduca un nou numar.
* Daca numarul dat de utilizator este egal cu numarul generat, atunci afiseaza mesajul "Ai ghicit".\

Pentru a genera un numar random intre 1 si 100, si a-l introduce intr-o variabila, foloseste:
```json
Random random = new Random(); 
int numberToGuess = random.nextInt(100) + 1;
```

HINT: s-ar putea ca "do while" sa se potriveasca mai bine aici.

Imbunatateste apoi programul dandu-i posibilitatea utilizatorului sa faca maxim 5 incercari.\
Daca ghiceste numarul din maxim 5 incercari, afiseaza in consola si din cate incercari a reusit.\
Altfel, afiseaza in consola faptul ca nu a reusit sa ghiceasca si ca jocul s-a terminat.\

### 18. Creeaza un sistem de verificare a PIN-ului.
Defineste in cadrul programului o variabila care sa contina un PIN, format din 4 cifre, care va reprezenta PIN-ul corect.\
Un utilizator are maxim 3 incercari sa introduca de la tastatura PIN-ul corect.\
Daca reuseste sa faca asta, se va afisa in consola "PIN corect" si programul se va opri.\
Daca nu reuseste sa faca asta, se va afisa in consola "PIN incorect" si programul se va opri.\

## While loops (confortabil)

### 19. Creeaza un automat de Coca Cola.
Presupunem ca o masina vinde sticle de cola care costa 50 de centi si accepta doar urmatoarele monede: 25 de centi, 10 centi si 5 centi.\
Implementeaza un program care ii cere utilizatorului sa introduca cate o moneda pe rand, si de fiecare data il informeaza cat mai are de platit pana la cei 50 de centi.\
O data ce utilizatorul a introdus minim 50 de centi, afiseaza cati centi trebuie sa primeasca rest.\
Ca si simulam introducerea monedelor, vom citi de la tastatura numere reprezetand valoarea monedelor.\

### 20. Creeaza un sistem automat de dat rest.
Atunci cand dai rest pentru un produs, vrei sa minimizezi numarul de monede pe care le dai ca rest.\
Daca ai de ales ca pentru suma de 50 de centi sa dai rest 2 monede de 25 de centi, sau 5 monede de 10 centi, vei alege prima varianta.\
Avem la dispozitie monede de 25 centi, 10 centi, 5 centi, 1 cent.\
Sa luam inca un exemplu:
* Daca restul este de 41 de centi, vrei sa ii dai o moneda de 25 de centi.
* Mai raman 16 centi, asa ca ii mai dai o moneda de 10 centi (cea mai mare ca valoare pe care poti sa i-o dai)
* Mai raman 6 centi, asa ca ii mai dai o moneda de 5 centi
* Mai ramane 1 cent, asa ca ii mai dai o moneda de 1 cent
In total 4 monede.

Programul trebuie sa citeasca de la tastatura valoarea restului si sa afiseze de cate monede este nevoie pentru a da rest, respectand algoritmul din exemplu.\
Programul nu trebuie sa afiseze de cate monede de fiecare tip este nevoie, ci de cate monede in total (chiar daca vor fi monede de tipuri diferite).\

HINT: porneste cu un pseudocod, care poate arata asa:
```json
// citesc de la tastatura valoarea restului, in centi
// calculez cate monede de 25 pot sa ii dau si le adun la numarul total de monede
// scad valoarea monedelor de 25 din valoarea restului
// calculez cate monede de 10 pot sa ii dau si le adun la numarul total de monede
// scad valoarea monedelor de 10 din centii ramasi de dat ca rest
// calculez cate monede de 5 pot sa ii dau si le adun la numarul total de monede
// scad valoarea monedelor de 5 din centii ramasi de dat ca rest
// calculez cate monede de 1 pot sa ii dau si le adun la numarul total de monede
// scad valoarea monedelor de 1 din centii ramasi de dat ca rest
// afisez numarul total de monede
```

Testeaza codul la final:
* pentru input -1, programul iti cere sa introduci din nou o valoare?
* pentru input 0, afiseaza programul 0?
* pentru input 4, afiseaza programul 4?
* pentru input 5, afiseaza programul 1?
* pentru input 24, afiseaza programul 6?
* pentru input 25, afiseaza programul 1?
* pentru input 26, afiseaza programul 2?
* pentru input 99, afiseaza programul 9?

## For loops (mai putin confortabil)

### 1. Scrie un program care sa afiseze numerele de la 1 la n, n fiind citit de la tastatura.

### 2. Scrie un program care sa printeze urmatorul pattern, in functie de numar n citit de la tastatura.
De exemplu, pentru n = 400 se va afisa:
```json
0
moo
2
moo
[si tot asa in continuare…]
398
moo
400
moo
```

### 3. Scrie un program care sa afiseze suma numerelor de la 1 la n, n fiind citit de la tastatura.

### 4. Scrie un program care sa afiseze numerele pare de la 1 la n, n fiind citit de la tastatura.

### 5. Scrie un program care sa faca media tuturor numerelor consecutive de la x la y, unde x si y sunt citite de la tastatura.

### 6. Scrie un program care sa afiseze suma numerelor divizibile cu 3 de la 1 la n, n fiind citit de la tastatura.

### 7. Scrie un program care sa afiseze factorialul unui numar.

### 8. Scrie un program care sa afiseze numerele prime din intervalul 1 - n, n fiind citit de la tastatura.

### 9. Scrie un program care calculeaza x la puterea y, unde x si y sunt citite de la tastatura.

## For loops (confortabil)

### 10. Printeaza jumatate de piramida, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
#
##
###
####
#####
```

### 11. Printeaza aceeasi jumatate de piramida (doar ca acum formata din numere), in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
0
01
012
0123
01234
```

### 12. Printeaza jumatate de piramida rasturnata, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
#####
####
###
##
#
```

### 13. Printeaza jumatate de piramida rasturnata, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
12345
1234
123
12
1
```

### 14. Printeaza jumatate de piramida rasturnata, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
54321
5432
543
54
5
```

### 15. Printeaza jumatate de piramida rasturnata, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
1
22
333
4444
55555
```

### 16. Printeaza cealalta jumatate de piramida, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
       #
      ##
     ###
    ####
   #####
```

> De aici incolo creste dificultatea destul de mult.

### 17. Printeaza o piramida, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
    #
   # #
  # # #
 # # # #
# # # # #
```

### 18. Afiseaza laturile unui partrat forma din "*", cu latura de lunigime n, n fiind citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
* * * * *
*       *
*       *
*       *
* * * * *
```

### 19. Printeaza o piramida cu un spatiu in mijloc, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 5, se va printa:
```json
       # #
      ## ##
     ### ###
    #### ####
   ##### #####
```


### 20. Printeaza o piramida din numere, in functie de un numar n citit de la tastatura.
De exemplu, pentru n = 4, se va printa:
```json
   4
  333
 22222
1111111
```


