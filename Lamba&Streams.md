
# TEME BACK-END 📚

## Lambda&Streams (mai puțin confortabil)


### 1. Rescrie urmatoarea metoda ca o expresie lambda:
```
public static String everySecondChar(String source) {
            StringBuilder returnVal = new StringBuilder();
            for (int i = 0; i < source.length(); i++) {
                if (i % 2 == 1) {
                    returnVal.append(source.charAt(i));
                }
            }
            return returnVal.toString();
        }
```
In primul rand, cauta pe Google si/sau ChatGPT si/sau in documentatia din IntelliJ ce face StringBuilder si metoda append.

Apoi rescrie functia clasica ca o functie lambda.

Apoi executa acea functie lambda si paseaza-i ca parametru: "1234567890".

Apoi creeaza o noua functie clasica numita everySecondCharacter() care accepta ca si parametru o functie lambda si un alt String.
Executa functia lamba in cadrul metodei everySecondCharacter(), si apeleaza everySecondCharacter() pasandu-i functia lambda creata ca prim parametru si string-ul "1234567890" ca al doilea parametru.


### 2. Sorteaza o o lista de persoane dupa nume, utilizand un comparator
Comparatorul nu va fi definit printr-o clasa care sa implementeze interfata Comparator

### 3. Scrie o functie lambda care sa returneze string-ul "Imi place Java".

Functia lambda va implementa interfata functionala Supplier si va fi asignata unei variabile.

Executa apoi functia lambda scrisa.

### 4. Proceseaza urmatoarea lista de nume:

Scrie codul astfel incat sa sortezi lista si astfel incat fiecare nume sa inceapa cu litera mare.

De exemplu, numele "harry" va deveni "Harry" si va fi intre "Emily" si "Isla".

```
List<String> topNames2015 = Arrays.asList(
                "Amelia",
                "Olivia",
                "emily",
                "Isla",
                "Ava",
                "oliver",
                "Jack",
                "Charlie",
                "harry",
                "Jacob"
        );
```

Apoi, in loc sa sortezi lista, afla de cate nume care incep cu 'A' sunt in lista.

### 5. Sterge persoanele care nu pot vota
Avand o lista de persoane, sterge din lista persoanele care au varsta mai mica decat 18 ani, folosind expresii lambda.

### 6. Suma numerelor pare
Calculeaza suma numerelor pare dintr-o lista de Integer-uri.
`HINT`: foloseste filter si sum sau foloseste reduce

Rezolva problema si fara expresii lambda.

### 7. Suma numerelor divizibile cu x sau cu y
Scrie o metoda care sa calculeze suma numerelor divizibile cu x sau y (unde x si y sunt primiti ca parametri), dintr-o lista de Integer-uri.
`HINT`: foloseste filter si sum sau foloseste reduce

Rezolva problema si fara expresii lambda.

### 8. Sorteaza numerele dintr-un array
Scrie o metoda care sa sorteze numerele dintr-o lista de Integer-uri, dar inainte de asta sa le transforme in valori pozitive

Exemplu: 

```
Input: [-1,2,-3,4,-5]
Output:[1,2,3,4,5]
````

(`HINT`: map pentru a transforma fiecare numar din negativ in pozitiv, apoi sorted() ca si operatie finala. Foloseste Math.abs() pentru a transforma un numar din negativ in pozitiv)

Rezolva problema si fara expresii lambda

Rezolva problema si fara expresii lambda. 
(`HINT`: foloseste metoda sort din arraylist)

### 9. Filtreaza persoanele care pot vota
O persoana este caracterizata de nume si varsta.
Scrie o metoda statica numita isPersonEligibleForVoting(), care accepta ca parametru o lista de persoane si returneaza o lista cu persoanele care pot vota. 

Scrie apoi metoda si fara expresii lambda.

### 10. Spell checker 2
Avand intr-un main un String, in care se stocheaza un text si o lista de cuvinte gresite, scrie o functie care accepta acesti 2 parametrii si returneaza lista cu cuvintele gresite care se regasesc in text
Exemplu: 

```
Input: String text = “acesta etse nu text”
      List<String> badWords = [“etse”, “nu”, “acetsa”, “extt”]
Output: [“etse”, “nu”], pentru ca acestea sunt cuvintele din badWords care se regasesc in text
```

(`HINT`: stream pe lista badWords, apoi filtram doar cuvintele care sunt continute in text (folosind metoda contains()) )

Rezolva problema si fara expresii lambda

### 11. Gestiunea tranzactiilor
O tranzactie este caracterizata de id, amount si de contul din care s-a facut tranzactia 

(`HINT`: atribute: id, sum, account - care este de tip Account)

Un cont este caracterizat de balance (sold) si un account number (numar de cont)
(`HINT` - aceasta va fi clasa Account).

Avand o lista de tranzactii intr-un main, scrie o metoda care primeste aceasta lista de tranzactii si genereaza o mapa in care cheia sa fie numarul de cont, iar valoarea sa fie suma amount-urilor tututor tranzactiilor care au avut loc din acel cont.

(`HINT`) - Collectors.summingLong.

Rezolva apoi problema si fara expresii lambda.

### 12. Gestiunea angajatilor
Un angajat este caracterizat de nume si salariu.
Un departament este caracterizat de nume, cod, si o lista de angajati. Codul este un String

Avand o lista de departamente intr-un main, care are fiecare o lista de angajati, scrie o metoda care primeste lista de departamente si un salariu minim.

Metoda va returna cati angajati din toate departamentele au salariul mai mare decat salariul minim primit ca parametru.

(`HINT`: stream pe departamente si apoi flatMap pentru a ajunge la angajati, apoi filter pentru a filtra pe cei cu salariul mai mare decat salariul minim si count la final pentru a-i numara)

Rezolva problema si fara expresii lambda

### 13. Gestiunea tranzactiilor 2
O tranzactie este caracterizata de id, state si amount. 
(`HINT`: atribute: id, state si amount)

Starea tranzactiei (state) este un enum care poate avea valorile FINISHED, CANCELED, PROCESSING.

Un cont (account) este caracterizat de balance (sold) si un account number (numar de cont) si de o lista de tranzactii
(`HINT`: atribute: number, balance, transactions - care este o lista)

Avand intr-un main o lista de conturi, care au fiecare lista lor de tranzactii, scrie o metoda care sa returneze suma tranzactiilor cu starea CANCELED din conturile care au soldul mai mare decat 0.

(`HINT`: stream pe lista de conturi si filter pentru a filtra conturile cu balanta mai mare decat 0, apoi flatMap pentru a ajunge la tranzactiile conturilor si filter pentru a filtra tranzactiile CANCELED)

Rezolva apoi problema si fara expresii lambda.

### 14. Event planner
Un eveniment are un nume si o data.

Avand o lista de evenimente, scrie o functi care sa returneze numele tuturor evenimentelor care au loc intre 2 data care vin ca parametru.

