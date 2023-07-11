# TEME BACK-END 📚

## Loops

### 1. Scrie un program care afiseaza numerele de la 1 la n, n fiind citit de la tastatura

### 2. Scrie un program care afiseaza suma numerelor de la 1 la n, n fiind citit de la tastatura

### 3. Scrie un program care afiseaza numerele pare de la 1 la n.

### 4. Scrie un program care afiseaza suma numerelor divizibile cu 3 din intervalul [1-n], n fiind citit de la tastatura.

### 5. Scrie un program care afiseaza numerele din sirul fibonacci pana la maxim n, n fiind citit de la tastatura.
Sirul fibonacci are urmatoarea regula: fiecare numar din sir este egal cu suma precedentelor doua numere din sir.
Primele doua numere sunt intodeauna 0 si 1.
```json
0, 1, 1, 2, 3, 5, 8, 13, 21, ...
```

### 6. Scrie un program care sa calculeze suma cifrelor unui numar, numarul fiind citit de la tastatura.

### 7. Scrie un program care inverseaza cifrele unui numar, numarul fiind citit de la tastatura.
Bazeaza-te pe faptul ca ultima cifra a oricarui numar este, de fapt, restul impartirii acelui numar la 10.
In plus, catul impartirii acelui numar la 10 este, de fapt, numarul initial, fara ultima cifra.

### 8. Scrie un program care afiseaza daca un numar este, sau nu, palindrom, numarul fiind citit de la tastatura.
Un numar este palindrom daca ramane la fel atunci cand cifrele ii sunt inversate.
De exemplu, numarul 12321 este palindrom deoarece atunci cand e inversat, este tot 12321.

### 9. Scrie un program care afiseaza cel mai mare divizor comun al doua numere, citite de la tastatura.
De exemplu, pentru numerele 21 si 15, cel mai mare divizor comun este 3.\
3 este cel mai mare numar la care si 21 si 15 se impart exact.\

### 10. Scrie un program care sa determine cat timp (in ani) ii ia unei populatii sa ajunga la o anumita marime.
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

### 11. Scrie un program care sa determine in cati ani economiile tale vor creste la target-ul pe care ti l-ai propus.
Sa presupunem ca deschizi un cont de economii cu o suma initiala de bani, la care se adauga in fiecare an o dobanda.\
\
De exemplu, daca deschizi un cont de 1000 de lei cu o dobanda anuala de 10%, dupa primul an vei avea 1000 + 0.1 * 1000 = 1100 de lei.\
Apoi, dupa al doilea an vei avea 1100 + 0.1 * 1100 = 1210\
Si tot asa, in fiecare an.\
\
Citeste de la tastatura suma initiala, procentul de dobanda anual, si suma target la care vrei sa ajungi.\
Apoi calculeaza cati ani e nevoie sa treaca pana ca in cont sa ajungi la suma target.\

### 12. Creeaza un guessing game.
Programul tau trebuie sa genereze un numar random (intre 1 si 100), iar apoi sa ii ceara utilizatorului sa il ghiceasca.
* Daca numarul dat de utilizator este mai mic decat numarul generat, atunci afiseaza mesajul "Prea mic, mai incearca" si da-i posibilitatea utilizatorului sa introduca un nou numar
* Daca numarul dat de utilizator este mai mare decat numarul generat, atunci afiseaza mesajul "Prea mare, mai incearca" si da-i posibilitatea utilizatorului sa introduca un nou numar
* Daca numarul dat de utilizator este egal cu numarul generat, atunci afiseaza mesajul "Ai ghicit"\
\
Imbunatateste apoi programul dandu-i posibilitatea utilizatorului sa faca maxim 5 incercari.\
Daca ghiceste numarul din maxim 5 incercari, afiseaza in consola si din cate incercari a reusit.\
Altfel, afiseaza in consola faptul ca nu a reusit sa ghiceasca si ca jocul s-a terminat.\



