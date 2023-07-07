# TEME BACK-END 📚

## Metode (functii)

### 1. Scrie un program care sa citeasca de la tastatura un mesaj, iar apoi sa afiseze mesajul cu litere mari.

### 2. Scrie un program care sa "puna pauza intre cuvinte". Citeste de la tastatura un mesaj si inlocuieste toate spatiile cu "...".
De exemplu, pentru mesajul introdus "aceasta e o functie", se va afisa in consola "aceasta...e...o...functie".\
Cauta pe Google o metoda deja implementata care sa faca inlocuirea.

### 3. Scrie un program care sa adauge emoticoane. Citeste de la tastatura un mesaj si inlocuieste toate secventele ":)" cu 🙂 si toate secventele
":(" cu 🙁
De exemplu, pentru mesajul introdus "Hello :) Goodbye :(", se va afisa in consola Hello 🙂 Goodbye 🙁.\
Cauta pe Google o metoda deja implementata care sa faca inlocuirea.

### 4. Scrie un program care sa construiasca o adresa de e-mail. Citeste de la tastatura numele si domeniul.
Defineste o metoda. De exemplu, pentru numele "stefan.olimpiu" si domeniul "gmail", metoda va returna "stefan.olimpiu@gmail.com"

### 5. Scrie un program care sa verifice daca un cuvant este intr-un text. 
Citeste de la tastatura un String reprezetand un text si cuvantul pe care doresti sa il cauti.\
De exempluu, pentru textul "eu sunt aici" si cuvantul "sunt", metoda va returna true pentru ca a gasit cuvantul "sunt" in text.\
Cauta pe Google o metoda deja implementata care sa faca verificarea pentru tine.

### 6. Scrie scheletul unui program care sa trimita notificari text sau prin e-mail.
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

### 7. Creaza un sistem de tracking pentru colete.
Un colet poate fi in 4 etape inainte de a ajunge la destinatie: preluare, procesare, trimitere, livrare.\
Citeste de la tastatura numarul de identificare al coletului.\
Creeaza cate o metoda pentru fiecare dintre etape, care sa returneze un mesaj cu starea pachetului.\
De exemplu, metoda pentru etapa de preluare ar putea returna urmatorul mesaj: "Coletul cu numarul 32445 a fost preluat".

### 8. Creeaza o aplicatie pentru impartirea automata a notei de plata
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



