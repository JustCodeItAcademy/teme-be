
# TEME BACK-END 📚

## Spring projects

### 1. Creeaza un magazin on-line

#### Feature 1 - admin panel

**Magazinul are mai multe categorii de produse**

Avem nevoie sa:

- Cream o categorie
  - Endpoint: `/categories/create`
  - Request Body example:
    ```json
    {
      "categoryName": "watches",
      "description": "best watches",
      "imageUrl": "https://images.unsplash.com/photo-1524805444758-089113d48a6d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80"
    }
    ```

- Vedem lista cu toate categoriile
  - Endpoint: `/categories`

- Editam o categorie
  - Endpoint: `/categories/update/{categoryId}`
  - Request Body example:
    ```json
    {
      "categoryName": "watches",
      "description": "best watches",
      "imageUrl": "https://images.unsplash.com/photo-1524805444758-089113d48a6d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80"
    }
    ```

**Magazinul are mai multe si produse in fiecare categorie**

Avem nevoie sa:

- Adaugam un nou produs
  - Endpoint: `/products/create`
  - Request body example:
    ```json
    {
      "name": "watch 2022",
      "description": "elegant watch",
      "imageUrl": "https://images.unsplash.com/photo-1524805444758-089113d48a6d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
      "price": "250",
      "categoryId": "2"
    }
    ```

- Vad lista cu toate produsele
  - Endpoint: `/products`

- Vad lista cu toate produsele dintr-o categorie
  - Endpoint: `/products/{categoryId}`

- Updatam un anumit produs
  - Endpoint: `/update/{productId}`
  - Request body example:
    ```json
    {
      "name": "watch 2022",
      "description": "very elegant watch",
      "imageUrl": "https://images.unsplash.com/photo-1524805444758-089113d48a6d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
      "price": "270",
      "categoryId": "3"
    }
    ```

#### Feature 2 - wishlist si cos de cumparaturi

**Un utilizator (client al magazinului) poate sa aiba un wishlist, unde sa isi adauge produse**

Avem nevoie sa:

- Adaugam produs in wishlist-ul unui utilizator
  - Endpoint: `/wishlist/add`
  - Request body example:
    ```json
    {
      "productId": "2",
      "userId": "3"
    }
    ```

- Vedem produsele din wishlist-ul unui utilizator
  - Endpoint: `/wishlist/{usedId}`

- Stergem un produs din wishlist-ul unui utilizator
  - Endpoint: `/whishlist/delete`
  - Request body example:
    ```json
    {
      "productId": "2",
      "userId": "3"
    }
    ```

**Indicatii wishlist**

- Creeaza entitatea Wishlist, 
- Creeaza entitatea WishlistItem
- Un user are un wishlist (deci one-to-one intre user si wishlist)
- Un wishlist are mai multe wishlistitems (deci one-to-many intre wishlist si whishlistitem)
- Un produs poate sa faca parte din mai multe wishlisturi (deci one-to-many intre product si wishlistitem)
- In concluzie, intre WishList si Product este o relatie many-to-many cu tabela de legatura WishListItem 
- Adica un wishlist are mai multe produse
- Un produs poate sa faca parte din mai multe wishlist-uri
- Ai nevoie de un WishListController, iar pentru adaugare in wishlist si vizualizare wishlist, va fi ceva asemanator cu adaugare si vizualizare cos de cumparaturi

**Un utilizator (client al magazinului) poate sa aiba mai multe produse in cosul de cumparaturi.**

La randul lor, produsele pot sa faca parte din cosurile de cumparaturi ale mai multor utilizatori

Avem nevoie sa:

- Adaugam produs in cosul de cumparaturi
  - Endpoint: `/cart/add`
  - Request body example:
    ```json
    {
      "productId": "2",
      "userId": "3",
      "quantity": "20"
    }
    ```

- Vad produsele din cosul unui utilizator
  - Endpoint: `/cart/{userId}`

- Sterg un produs din cosul de cumparaturi al unui utilizator
  - Endpoint: `/cart/delete/{cartItemId}/{userId}`

**Indicatii stergere din cos**

- Trebuie doar sa te folosesti de metoda din repository deleteById pentru a sterge cartItem-ul dupa id

#### Feature 3 - plasarea si gestionarea comenzilor

**Un utilizator (client al magazinului) poate sa aiba mai multe comenzi.**

Fiecare comanda poate avea mai multe produse, si fiecare produs poate face parte din mai multe comenzi.

Avem nevoie sa:

- Plasam o comanda pentru un utilizator (cu produsele pe care le are in cosul de cumparaturi)
  - Endpoint: `/orders/add/{userId}`

- Vad toate comenzile plasate de un utilizator (ordonate desc. dupa data crearii comenzii)
  - Ednpoint: `/orders/{userId}`

- Vad detaliile unei comenzi plasate de utilizator (ce produse, cu ce cantitati si ce preturi sunt in comanda, pret total al comenzii, data crearii)
  - Endpoint: `/orders/{orderId}`

**Indicatii comenzi**

- Creeaza entitatile Order si OrderItem
- Order-ul va avea in plus ca si atribut un totalPrice
- OrderItem va avea in plus ca si atribute quantity si price (pe langa atributele folosite pentru a face legaturile intre tabele)
- Un User poate avea mai multe ordere (deci one-to-many intre user si comenzi)
- Un order poate avea mai multe orderitems( deci one-to-many intre order si orderitem)
- Pentru plasarea unei comenzi, e nevoie sa:
  - Gasesti utilizatorul dupa id
  - Iei toate cartItem-urile utilizatorului din baza de date ( te folosesti de metoda cartRepository.findAllByUser)
  - Construiesti un nou obiect order, calculezi si pretul total si salvezi acest order in baza de date
  - Pentru fiecare cartitem din lista de cartitems ale utilizatorului
    - Creezi un nou orderitem
    - Il legi de order (orderItem.setOrder(newOrder)
    - Salvezi in abza de date acel orderItem
    - Stergi toate cartitems-urile utilizatorului




### 2. Code sharing platform

Vrem să construim o platformă prin care un programator să poată share-ui o bucată de cod cu alt programator (vezi Pastebin). Însă, la Pastebin, fiecare bucată de cod este publică pentru toată lumea. Noi vrem să putem să share-uim și bucăți de cod în secret (pentru companiile care nu pot dezvălui codul public). Fiecare bucată de cod va avea un număr limitat de views (adică de câte ori se poate vedea acea bucată de cod) și o limită pentru timpul în care poate fi văzut. După o anumită perioadă de timp, codul va expira și va fi șters din baza de date.

#### Endpoint-uri:

##### `/api/code/{codeId}`

Acest endpoint va da ca răspuns codul căutat după id (împreună cu celelalte detalii). De fiecare dată când requestul este efectuat, dacă codul este secret, numărul de views va scădea cu 1. Totodată, atunci când request-ul este efectuat, se va verifica dacă timpul a expirat sau dacă numărul de vizualizări este 0, iar dacă este așa, codul se va șterge din baza de date.

##### `/api/code/add`

Acest endpoint va primi în body o bucată de cod, împreună cu timpul (în secunde) în care bucata de cod este valabilă și numărul maxim de vizualizări. Dacă valorile pentru timp și views sunt 0, înseamnă că bucata de cod nu are nicio restricție.

Exemplu:

```json
{
  "code": "SpringApplication.run(CodeSharingPlatform.class, args);",
  "time": 5000,
  "views": 5
}
```

Codul se va salva în baza de date, împreună cu data la care a fost adăugat.

##### `/api/code/latest`

Acest endpoint va da ca răspuns ultimele 5 bucăți de cod publice adăugate (în funcție de data creării), împreună cu celelalte detalii.

### 3. Booking.com clone

Dezvoltă un sistem de rezervări la hotel asemănător cu booking.com. Aplicația va avea 2 tipuri de utilizatori: administratori de hotel și clienți.

#### Structura Aplicației:

- **Camera**: 
  - Număr
  - Preț pe noapte
  - Număr de persoane care pot fi cazate
  - Listă de rezervări

- **Rezervare**: 
  - Poate fi făcută pentru o cameră, de către un client, între două date (check-in și check-out).

- **Utilizator**: 
  - Listă de rezervări
  - Nume
  - Prenume

#### Funcționalități:

##### Administratori de Hotel:

- **Managerierea Camerelor**:
  - Adăugare cameră
  - Ștergere cameră
  - Vizualizare camere
  - Editare preț cameră

- Vizualizarea numărului de camere libere/ocupate pentru o anumită perioadă.
- Vizualizarea veniturilor obținute din toate rezervările dintr-o anumită perioadă.

##### Clienți:

- Vizualizarea disponibilităților (camere libere) pentru o anumită perioadă și un anumit număr de locuri.
- Sortarea disponibilităților (camere libere) după preț pentru o anumită perioadă și un anumit număr de locuri.
- Facerea unei rezervări pentru o anumită cameră.

#### Extensii ale Aplicației:

După ce această versiune a aplicației funcționează, permite ca în aplicație să existe mai multe hoteluri. Administratorul va putea să adauge și hoteluri în aplicație.

### 4. Cinema city clone

#### Ca si admin, vreau sa:

- Adaug o sala de cinema, cu capacitatea de n randuri * m coloane (adica se vor genera n*m locuri), intervalele de randuri intre care vreau sa pun un pret extra.
- Initial toate locurile vor fi disponibile pentru cumparare.

##### Ce se va intampla:

- Se va adauga in baza de date o noua sala de cinema.
- Se vor adauga in baza de date 64 de locuri (legate de aceasta sala de cinema).
- Fiecare loc din acele 64 locuri va avea valoarea true pentru atributul isAvailable.
- Locurile de pe randurile 6 si 7 vor avea valoarea atributului extraPrice egala cu 3.
- Locurile de pe randurile 5 si 6 vor avea valoarea atributului extraPrice egala cu 2.
- Fiecare loc va avea valoarea atributelor “row” si “col” egale cu randul si coloana locului.

###### Exemplu request body:

```json
{
  "numberOfRows": 8,
  "numberOfCols": 8,
  "extraPrices": [
    {
      "startingRow": 6,
      "endingRow": 7,
      "extraPrice": 3
    },
    {
      "startingRow": 5,
      "endingRow": 6,
      "extraPrice": 2
    }
  ]
}
```

- Adaug un nou film, care se va difuza intr-o anumita sala.
  
###### Exemplu request body:

```json
{
  "movieName": "Goodfellas",
  "cinemaRoomId": 2,
  "dates": [
    {
      "startTime": "2016-11-09T11:00:00",
      "endTime": "2016-11-09T13:00:00"
    },
    {
      "startTime": "2016-11-09T15:00:00",
      "endTime": "2016-11-09T17:00:00"
    }
  ]
}
```

Practic fiecare film va avea o sala in care se va difuza si mai multe date in care se va difuza.
Celelalte detalii ale filmului se vor popula printr-un request la un API, care sa ne dea gen, descriere, etc.
In plus, filmul va avea un pret.
Hint: daca in sala respectiva exista deja alte filme care se vor difuza la cel putin una din datele primite in request, se va raspunde cu eroare.

- Vad statisticile cinema-ului:
  
- Care este valoarea tuturor biletelor vandute intr-o anumita zi (la un film sau la toate filmele).
/ticket/totalprice/

- Cate bilete s-au vandut la un anumit film sau la toate filmele.


#### Ca si client, vreau sa:
- Vad lista de locuri disponibile la un film.
Hint - asta numai daca filmul are date la care se va difuza in viitor.

- Cumpar un bilet la un film.
Pretul pentru fiecare loc se va calcula in functie de pretul firmului, la care se va adauga un extraPrice daca acel loc are extraPrice.

###### Exemplu request body:
```json
{
  "movieId": 3,
  "seats": [
    {
      "row": 2,
      "column": 4
    },
    {
      "row": 2,
      "Column": 5
    }
  ]
}
```

- Extra bonus points(optional) - pentru utilizator se va genera un bilet PDF care se va trimite pe mail-ul utilizatorului.
Hint: se poate face o abordare similar ca la aplicatie cu magazin on-line: utilizatorul sa aiba un order, care contine mai multe seats. Automat dupa plasarea comenzii, seat-urile nu vor mai fi disponibile.


### 4. Weather app
Aceasta aplicatie are ca scop ca un utilizator sa poata vedea vremea.

El are o lista de orase favorite. 

Endpoint-uri:
- CRUD utilizator 
- adauga oras favorit in lista utilizatorului
- Stergere oras favorit din lista utilizatorului
- Vizualizare orase favorite pentru un utilizator
- Vizualizare vreme curenta pentru un anumit oras
- Viualizare forecast pe 5 zile pentru un anumit oras

Datele despre vreme se preiau dintr-un api extern

### 5. Price generator

În magazinul tău on-line vrei să faci oferte de preț personalizate pentru clienții tăi, în funcție de produsele pe care doresc să le cumpere, și de alte criterii.
Vom defini oferta de preț sub numele de cotație (quotation).

**Cotația se calculează în funcție de:**
- Vârsta clientului
- Țara din care provine
- Numărul de zile de produse cumpărate

**Condiții:**
- Dacă vârsta clientului este mai mare decât un prag stabilit pentru produsul pe care vrea să îl cumpere, atunci se aplică o reducere de 20% față de prețul de listă al produsului. Dacă nu, cotația rămâne egală cu prețul inițial.
- În plus, clientul primește o reducere în funcție de țara de unde comandă. Pentru România va fi o reducere de 5%, pentru Anglia 2%, etc.
- În plus, clientul primește o reducere de 0.5% per produs, dacă cumpără minim 3 produse. Reducerea se aplică pentru maxim 10 produse cumpărate (De exemplu, reducerea totală va fi de 4,5% pentru produsele 2,3,4,5,6,7,8,9,10, dacă clientul cumpără 15 produse)

**Entități:**
- Un produs va avea:
  - Preț de listă (exemplu: 100 RON)
  - Pragul de vârstă de unde se aplică reducerea (ex: de la 45 de ani în sus ai reducere)
  - Lista de discounturi pentru fiecare țară 
  - Cum modelăm asta în baza de date? Avem nevoie de entități noi? Dacă da, ce relații vor fi între ele?

- Un client va avea:
  - Data nașterii
  - Username
  - Parola

- O cotație va avea:
  - Data de expirare
  - Produsul pentru care a fost generată
  - Clientul pentru care a fost generată

- O comandă va avea:
  - Data creării

**Ca și client vei putea să:**
- Îți vezi cotațiile generate de tine, care încă sunt active
- Faci o comandă pentru una, două… sau toate cotațiile (ofertele de preț) active 
  - Aici se va aplica, după caz, și reducerea pentru numărul de cotații din comandă, care practic este egal cu numărul de produse (pentru că o cotație se generează pentru un produs)
- Vezi reducerea totală pe care ai primit-o pentru o comandă
- Generezi o cotație pentru un produs
- **Bonus:** cotațiile care ajung la data de expirare se șterg automat din baza de date

**Ca și admin vei putea să:**
- CRUD produse
- Vezi reducerea totală care s-a aplicat pentru toate comenzile dintr-o zi




