
# TEME BACK-END 📚

## Spring Data JPA

### 1. Implementeaza aplicatia Twitter

Un utilizator in aplicatia Twitter are un nume. Utilizatorul poate sa aiba, in plus, niste Tweet-uri pe care le creeaza.
Un Tweet are un text, si poate sa aiba mai multe Comment-uri.
Iar un Comment are si el un text.

Vreau ca din aplicatie sa pot sa:
- Updatez un user
- Adaug un user
- Gasesc un user dupa id
- adaug un tweet la un utilizator
- sterg toate tweet-urile de la un user
- sterg un anumit tweet de la un user
- sterg un user (impreuna cu tweet-urile lui)
- adaug un comentariu la un tweet.
- sterg un anumit comnetariu de la un tweet
- sterg toate comentariile de la un tweet
- gasesc toate comentariile de la un tweet
- gasesc toate comentariile unui utilizator (indiferent de tweet)

### 2. Simuleaza o aplicatie de filme
Un film contine mai multe caracatere, iar un caracter poate juca in mai multe filme.
Un film poate apartine unei francize, iar o franciza poate contine mai multe filme.
De exemplu, franciza Marvel contine 23 de filme.

Pe langa operatiile standard, vreau sa pot sa:
- adaug un caracter intr-un film
- adaug un film intr-o franciza.
- Vad toate filmele dintr-o franciza
- Vad toata caracterele dintr-un film

### 3. Aplicație pentru gestiunea unei companii de cursuri

#### Ca și student am nevoie să:
- Vad echipa din care fac parte și lista colegilor mei
- Vad modulele la care voi participa (împreună cu datele și locațiile)
- Îmi vad prezența

#### Ca și trainer, am nevoie să:
- Vad sesiunile la care trebuie să predau (împreună cu datele și locațiile)
- Selectez module (ex: Java fundamentals) la care vreau să predau în viitor
- Setez prezența pentru sesiunile la care predau

#### Ca și admin, am nevoie să:
- CRUD pe useri, echipe, module, locații, subiecte, sesiuni
- Vad lista de prezență pentru toți studenții

##### Exemple:

###### Locații:
- **Name**: Biroul1
- **Street**: Eroilor
- **Number**: 10

###### Module:
- **Name**: Java fundamentals
- **StartDate**: 12.10.2022
- **EndDate**: 25.10.2022
- **Team**: grupa1București

###### Subiecte:
- **Name**: variabile (în modulul Java fundamentals)

###### Echipe:
- **Name**: grupa1București

###### Sesiuni:
- **StartTime**
- **EndTime**
- **Date**
- Exemplu: Modulul JavaFundamentals, pentru echipa grupa1București, între 12.10.2022 și 25.10.2022, va avea 5 sesiuni în date diferite. Prima sesiune este ținută de trainerul Stefan Olimpiu la locația Biroul1.

###### User:
- **Username**
- **Password**
- **Firstname**
- **Lastname**
- **EmailAddress**
- **Role** - enum

###### Prezențe:
- **Status** - enum
- Exemplu: studentul X a fost absent la subiectul variabile, la modulul Java fundamentals, la sesiunea a 3-a

#### Incepe cu urmatoarele operatii de baza:
- CRUD-uri
- Adăugare student în echipă
- Ștergere student din echipă

#### Tips:
- Ține cont de relațiile dintre tabele.
- Exemplu: la adăugarea unui nou student, acesta va fi inclus într-o echipă, , pentru ca asa e relatia (o echipa are mai multi studenti).
- La fel si cand vei vrea sa adaugi un modul, pentru ca un modul trebuie sa fie adaugat la o echipa (din cauza relatiei one-to-many intre team si module)






