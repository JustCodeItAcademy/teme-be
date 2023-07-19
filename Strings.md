# TEME BACK-END 📚

## Strings (mai putin confortabil)

### 1. Scrie un program care sa extraga prima jumatate a unui String de lungime para
De exemplu, pentru "programmer", se va afisa in consola "progr".

### 2. Scrie un program care sa concateneze doua String-uri, mai putin primul caracter din fiecare
Pentru  "Java" si "Fundamentals", se va afisa in consola "avaundamentals".

### 3. Scrie un program care citeste de la tastatura un String si il afiseaza in consola consola caracter cu caracter (cate un caracter pe fiecare linie)

### 4. Scrie un program care sa inlocuiasca fiecare animal care incepe cu litera "B" cu "Lion", intr-un array de animale.
Pseudocod: 
```json
Pentru fiecare animal din lista de animale:
   Daca primul caracter al animalului este 'B', atunci la acel index pun valoarea "Lion".
```
De exemplu, array-ul {"Aardvark", "Bear", "Bobcat", "Cheetah", "Dog"} va deveni {"Aardvark", "Lion", "Lion", "Cheetah", "Dog"}

### 5. Scrie un program care sa afiseze toate string-urile care au lungimea para dintr-un array de string-uri
De exemplu, pentru array-ul {“ana”, “home”, “an”} se va afisa: “home”, “an”

### 6. Scrie un program care citeste de la tastatura un String si ii inverseaza caracterele.
De exemplu, String-ul "java" devine "avaj".

### 7.Scrie un program care sa afiseze in consola daca un cuvant este palindrom sau nu.
Un cuvant sau numar este palindrom daca este egal cu inversul lui\
De exemplu, ana este palindrom, dar mama nu este palindrom pt ca mama este diferit de inversul sau (amam)

### 8. Scrie un program care sa inverseze toate cuvintele dintr-un text. Cuvintele sunt separate de spatii.
De exemplu, pentru “This is Java” se va afisa: “Java is This”

### 9. Scrie un program care sa transforme in litera mare prima litera din fiecare cuvant dintr-un String citit de la tastatura.
De exemplu, pentru String-ul "ana are mare", se va afisa "Ana Are Mere"

### 10. Scrie un program care printeaza in consola daca un String are caracterele in ordine alfabetica, sau nu.
HINT: atunci cand compari 2 caractere folosind operatorul "<", afli daca ele sunt in ordinea alfabetica.\
De exemplu, expresia 'a'<'b' va returna true, dar 'b'<'a' va returna false.

### 11. Scrie un program care citeste de la tastatura numele complet al unui om si ii afiseaza initialele.
De exemplu, pentru String-ul "Stefan I. Olimpiu", se va afisa "SIO".\
HINT: foloseste metoda split() pentru a "sparge" string-ul intr-un array a carui elemente sa fie toate numele din numele complet.

### 12. Scrie un program prin care utilizatorul sa introduca de la tastatura hobby-uri ca String-uri, pana cand introduce cuvantul  “stop” sau “exit”.
Utilizatorul poate introduce maxim 10 hobby-uri. Fiecare hobby este adaugat intr-un array de String-uri.\
La sfarsit, cand utilizatorul a introdus “stop” sau “exit”, se vor afisa in consola toate hobby-urile din array.

### 13. Scrie un program care sa numere literele, spatiile, numerele, si celelalte caractere dintr-un String. (folositi metodele String-ului)
De exemplu, pentru “Aa kiu, I swd skieo 2387. GH kiu: sieo?? 25.33”, se va afisa in consola: "23 litere, 9 spatii, 8 numere, 6 alte caractere".\
Foloseste-te de metodele disponibile in lucrul cu caractere: https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Character.html

### 14. Implement a program that prompts the user for the name of a variable in camel case and outputs the corresponding name in snake case.
Scrie un program care sa citeasca un String de la tastatura in format camel case si sa il printeze apoi in format snake case.\
De exemplu, pentru "thisIsAVariabile", se va afisa "this_is_a_variable".\
Presupune ca input-ul citit de la tastatura va fi in format camel case.

### 15. Pe twitter exista moda de a omite vocale atunci cand scrii, ca sa salvezi spatiu.
De exemplu, Twitter a fost numit original Twttr.\
Scrie un program care citeste de la tastatura un String si printeaza acelasi string, fara vocale.

### 16. Scrie un program care sa valideze o parola
O parola (citita de la tastatura) este valida daca contine cel putin o litera mare, cel putin o litera mica, cel putin un numar, si cel putin un simbol.\
Simbolul inseamna ca nu este litera sau cifra, cum ar fi "!", "$", etc.\
Printeaza apoi un mesaj corepsunzator, si da-i posibilitatea utilizatorului sa introduca din noua o parola, pana cand introuce una care sa fie valida.\
Foloseste-te de metodele disponibile in lucrul cu caractere: https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Character.html

### 17. Ai posibilitatea sa iti pui la masina numar de inmatriculare "de smecher".
Un numar de smecher trebuie sa inceapa cu cel putin doua litere.\
Un numar de smecher poate sa contina maxim 6 caractere (litere sau numere) si minim 2 caractere.\
Nu poti sa folosesti cifre in mijlocul unui numar de smecher. De exemplu, "AAA222" este valid, dar "AAA22A" nu este valid.\
In plus, nu sunt acceptate virgule, spatii, sau alte semne de punctuatie.

### 18. Scrie un program care sa codifice vocalele din cuvinte prin cifre.
Regula este ca litera a (indiferent daca este mica sau mare) se codifica cu cifra 4, e cu 3, i cu 1, o cu 0 si u cu 7.\
De exemplu, pentru "antrenor" se va afisa "4ntr3n0r".

### 19. Implementeaza o parte din jocul Scrabble.
In scrabble, fiecare cuvant are un punctaj bazat pe suma punctelor echivalente fiecarei litere din cuvant.\
De exemplu, cuvantul "code" are 7 puncte (c valoreaza 3 puncte, o -> 1 punct, d -> 2 puncte, e -> 1 punct).\
Citeste de la tastatura 2 cuvinte si afiseaza-l pe cel care are mai multe puncte (cuvantul castigator).\
Foloseste-te de acest array care reprezinta scorul fiecarei litere in alfabet, de la A la Z.\
```json
int[] letterScores = {1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 1, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10};
```

### 20. Implementeaza jocul Spanzuratoarea
Tu, ca jucator, ai posibilitatea sa incerci sa ghicesti cuvinte intre 5 si 8 litere.\
Jocul va avea o lista cu cuvinte predefinite pe care le poti ghici, atat cu 5, cat si cu 6-7-8 litere.\
De la tastatura se va citi numarul de litere - adica din cate litere sa fie cuvantul pe care sa il ghiceasca utilizatoul.\
\
Creeaza o functie chooseWord() care alege din lista de cuvinte predefinite un cuvant care sa aiba numarul de litere egal cu numarul citit de la tastatura.\
Acesta va fi cuvantul secret, care trebuie ghicit.

Utilizatorul are 6 incercari sa ghiceasca cuvantul secret. Aceste incercari se vor citi de la tastatura. La fiecare incercare, va primi un hint (afisat in consola).\
Creeaza o functie getHint() care returneaza un hint in functie de incercarea utilizatorului.\
Hint-ul va fi un cuvant format din dublul numarului de caractere ale incercarii utilizatorului.\
Pentru fiecare litera din incercarea data de utilizator, se va mai alatura o un nou caracter imediat dupa:
* Daca litera din incercare este aceeasi cu litera din cuvantul secret, de la aceeasi pozitie, atunci in hint se va pune litera din incercare urmata de caracterul "#".\
Asta semnifica faptul ca utilizatorul a ghicit acea litera. Este exact in locul potrivit.
* Daca litera din incercare exista in cuvantul secret, doar ca in alta pozitie, atunci in hint se va pune litera din incercare urmata de caracterul "?".\
Asta semnifica faptul ca utilizatorul a ghicit litera, doar ca este la alta pozitie.
* Daca litera din incercare nu exista in cuvantul secret, atunci in hint se va pune litera din incercare urmata de caracterul "_".\
Asta semnifica faptul ca utilizatorul nu a ghicit deloc litera.\

Exemplu (pentru cuvantul secret since)
* Daca utilizatorul introduce in prima incercare cuvantul crash, i se va printa ca hint : c?r_a_s?h_
* Daca utilizatorul introduce in a doua incercare cuvantul scone, i se va printa ca hint : s#c?o_n?e#
* Daca utilizatorul intrduca in a 3-a incercare cuvantul science, i se va printa ca hint: s#i#n#c#e si jocul va lua sfarsit.





