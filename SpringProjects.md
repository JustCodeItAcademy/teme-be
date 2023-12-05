
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
}```

Codul se va salva în baza de date, împreună cu data la care a fost adăugat.

##### `/api/code/latest`

Acest endpoint va da ca răspuns ultimele 5 bucăți de cod publice adăugate (în funcție de data creării), împreună cu celelalte detalii.

