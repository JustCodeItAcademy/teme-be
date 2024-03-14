# TEME BACK-END 📚

## Metode (functii)

### 1. Creeaza o metoda numita hasEqualSum(), care primeste 3 parametri reprezentand numere intregi.
Metoda va returna true daca suma primilor 2 parametri este egala cu cel de-al 3-lea.
De exemplu:

```json
apelul de metoda cu parametri 1,1,1, adica hasEqualSum(1, 1, 1) va returna  fals2 pentru ca 1 + 1 (suma primilor 2 parametri) nu este egal cu 1 (al 3-lea parametru)
apelul de metoda cu parametri 1,1,2, adica hasEqualSum(1, 1, 1) va returna  true pentru ca 1 + 1 (suma primilor 2 parametri) este egal cu 2 (al 3-lea parametru)
```

Defineste metoda (impreuna cu parametri necesari), implementeaz-o, si apoi apeleaz-o in main().

### 2. Creeaza o metoda numita getAge(), care primeste ca parametru anul nasterii unei persoane
Metoda va returna varsta persoanei.
De exemplu:
```json
apelul de metoda cu parametrul 2000, adica getAge(2000) va returna valoarea 24 pentru "anul curent - 2000 = 24"
```

### 3. Creeaza o metoda numita shouldWakeUp(), care sa returneze true sau false.
Metoda va returna true daca primeste informatia ca latra cainele si daca ora este inainte de 8, sau dupa 22.
De exemplu:
```json
apelul de metoda cu parametrii true si 1 (cainele latra si este ora 1) adica shouldWakeUp(true, 1), va returna valoarea true pentru ca ambele conditii din enunt sunt indeplinite
apelul de metoda cu parametrii false si 2 (cainele nu latra si este ora 2) adica shouldWakeUp(false, 2), va returna valoarea false pentru ca doar a doua conditie este indeplinita (dar cainele nu latra)
apelul de metoda cu parametrii true si 8 (cainele latra si este ora 1) adica shouldWakeUp(true, 8), va returna valoarea false pentru ca doar prima conditia este indeplinita (ora nu este inainte de 8)
```
Defineste metoda (impreuna cu parametri necesari), implementeaz-o, si apoi apeleaz-o in main().

### 4. Creeaza o metoda numita displayBytesConversions(), care sa accepte un parametru de tip int, care va reprezenta numarul de kilobytes.
Metoda nu trebuie sa returneze nimic, doar sa calculeze cati megabytes si cati kilobytes reprezinta numarul primit ca parametru.
De exemplu, daca parametrul are valoarea 2500, metoda va printa: ""2500 KB = 2 MB and 452 KB".

HINT: Ca sa afli numarul de megabytes, trebuie sa imparti numarul primit ca parametru la 1024 folosind operatorul clasic de impartire, adica "/".
Iar ca sa afli numarul de kilobytes, trebuie sa imparti numarul primit ca parametru la 1024 folosind operatorul de impartire cu rest, adica "%".
Defineste metoda (impreuna cu parametri necesari), implementeaz-o, si apoi apeleaz-o in main().

### 5. Scrie un program care sa citeasca de la tastatura 3 numere si care sa determine daca cel putin unul dintre numere este un numar "perfect".
Un numar perfect este un numar din intervalul [13-19].
Exemplu:
```json
metoda hasTeen(9, 99, 19);  va returna true, pentru ca 19 este in interval

metoda hasTeen(23, 15, 10);  va returna true, pentru ca 15 si 10 sunt in interval

metoda hasTeen(22, 23, 34);  va returna fals pentru ca nu exista cel putin un parametru care sa fie in interval
```
HINT: foloseste-te de o alta metoda isPerfect() care sa returneze true daca un anumit numar este "perfect"

### 6. Scrie un program care sa construiasca o adresa de e-mail. Citeste de la tastatura numele si domeniul.
Defineste o metoda. De exemplu, pentru numele "stefan.olimpiu" si domeniul "gmail", metoda va returna "stefan.olimpiu@gmail.com"

### 7. Scrie un program care sa citeasca de la tastatura un mesaj, iar apoi sa afiseze mesajul cu litere mari.

### 8. Scrie un program care sa "puna pauza intre cuvinte". Citeste de la tastatura un mesaj si inlocuieste toate spatiile cu "...".
De exemplu, pentru mesajul introdus "aceasta e o functie", se va afisa in consola "aceasta...e...o...functie".\
Cauta pe Google o metoda deja implementata care sa faca inlocuirea.

### 9. Scrie un program care sa adauge emoticoane. Citeste de la tastatura un mesaj si inlocuieste toate secventele ":)" cu 🙂 si toate secventele
":(" cu 🙁
De exemplu, pentru mesajul introdus "Hello :) Goodbye :(", se va afisa in consola Hello 🙂 Goodbye 🙁.\
Cauta pe Google o metoda deja implementata care sa faca inlocuirea.



### 10. Scrie un program care sa verifice daca un cuvant este intr-un text. 
Citeste de la tastatura un String reprezetand un text si cuvantul pe care doresti sa il cauti.\
De exempluu, pentru textul "eu sunt aici" si cuvantul "sunt", metoda va returna true pentru ca a gasit cuvantul "sunt" in text.\
Cauta pe Google o metoda deja implementata care sa faca verificarea pentru tine.

### 11. Scrie scheletul unui program care sa trimita notificari text sau prin e-mail.
Defineste o metoda cu numele "createNotification", care sa accepte ca si parametri mesajul notificarii, cine a trimis notificarea, si cine va primi notificare.
Metoda ar trebui sa returneze textul notificarii.\
\
Defineste o metoda cu numele sendNotificationText, care sa accepte ca si parametri mesajul notificarii, cine a trimis notificarea, si cine va primi notificare.
Metoda ar trebui sa creeze notificarea in functie de parametri, apoi sa afiseze la consola: "notificarea a fost trimisa prin mesaj", urmat de textul notificarii.\
\
Defineste o metoda cu numele sendNotificationEmail, care sa accepte ca si parametri mesajul notificarii, cine a trimis notificarea, si cine va primi notificare.
Metoda ar trebui sa creeze notificarea in functie de parametri, apoi sa afiseze la consola: "notificarea a fost trimisa prin e-mail", urmat de textul notificarii.\
\
Apeleaza apoi metodele sendNotificationText si sendNotificationEmail din metoda main. 
Atunci cand le apelezi, paseaza-le ca parametri niste valori citite de la tastatura (mesajele notificarilor, cine le primeste si cine le trimite).

### 12. Creaza un sistem de tracking pentru colete.
Un colet poate fi in 4 etape inainte de a ajunge la destinatie: preluare, procesare, trimitere, livrare.\
Citeste de la tastatura numarul de identificare al coletului.\
Creeaza cate o metoda pentru fiecare dintre etape, care sa returneze un mesaj cu starea pachetului.\
De exemplu, metoda pentru etapa de preluare ar putea returna urmatorul mesaj: "Coletul cu numarul 32445 a fost preluat".

### 13. Creeaza o aplicatie pentru impartirea automata a notei de plata
Aplicatia va trebui sa imparta nota pentru 2 oameni, in functie de valoarea notei de plata, taxele adaugate, si bacsis.\
Se va citi de tastatura valoarea notei de plata, valoarea taxelor, si valoarea bacsisului.\
Valoarea notei de plata va reprezenta cati lei costa, insa valoarea taxelor si a bacsisului vor fi introduse ca procente.\
Taxele trebuie adaugate la suma totala inainte sa fie adaugat bacsisul.\
Trebuie sa calculezi jumatate din suma totala, incluzand valoarea notei, taxele si bacsisul.\
Creeaza o metoda pentru a face acest calcul.\
\
**HINT:** Pentru a calcula spre exemplu valoarea taxei, in functie de procentaj, trebuie sa inmultesti valoarea notei cu valoarea procentului taxei, apoi sa imparti la 100.
De exemplu, pentru datele de intrare:
```json
Bill before tax and tip: 12.50
Sale Tax Percent: 8.875
Tip percent: 20
```
se va afisa in consola: 
```json
Fiecare trebuie sa contribuie cu 8.17 lei
```

### 14. Creeaza o aplicatie pentru un smart home
Aplicatia va fi folosita pentru a controla remote difuzoarele wireless, luminile, securitatea casei, incuietorile usilor si diversi roboti care se afla in casa.\
Pentru inceput, vrem sa putem face urmatoarele actiuni:
* pornim sau oprim muzica
* pornim sau oprim lumina
* incuiem sau descuiem usa

Algoritmul cu care am putea descrie un program pentru este urmatorul:
```json
1. cere parola utilizatorului
2. verifica daca este corecta
3. intreba utilizatorul ce actiune vrea sa faca
4. citeste actiunea si daca este suportata, execut-o
```
Sa zicem ca avem deja codul aplicatiei (scheletul), doar ca am folosit o singura metoda:

```json
        // ...
        int password = 76543210;
        String speakersState;
        String lampState;
        String doorState;

        // reading the password
        System.out.println("Enter password: ");
        int passwordInput = scanner.nextInt();

        // checking if the password is correct
        if (passwordInput != password) {
            System.out.println("Incorrect password!");
        } else {
            // asking the user what they want to do
            System.out.println("Choose the object: 1 – speakers, 2 – lamp, 3 – door");
            String action = scanner.next();
            
            switch (action) {
                case "1":
                    // asking the user about speakers
                    switch (speakersState) {
                        case "on":
                            // ...
                        case "off":
                            // ...
                        default:
                            // ...
                    }
                    break;
                case "2":
                    // asking the user about lights...
                case "3":
                    // asking the user about the door...
                }
        }
```
Dar daca vrem sa adaugam mai multe actiuni? Codul ar deveni complex. Pentru a-l face flexibil, extrage in metode codul original.\
Apoi adauga o functionalitate noua, acceea de a porni sau opri un aspirator robot.\
