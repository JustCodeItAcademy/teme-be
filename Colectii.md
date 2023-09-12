
# TEME BACK-END 📚

## Colectii (mai puțin confortabil)

### 1. Implementeaza un PhoneBook

#### Atribute: 
- **contacts**: o lista de String-uri reprezentand numere de telefon
- **blackList**: o lista de String-uri reprezentand numere de telefon blocate

#### Metode:

#### filterContacts()
- Metoda statica
- Acceptă ca și parametri:
  - o lista de contacte valide
  - o lista de contacte blocate
- Trebuie să șteargă din lista de contacte valide toate numerele care se regăsesc în lista de contacte blocate
- Returnează lista de contacte valide modificată

#### addToBlackList()
- Metoda non-statică
- Adaugă numărul primit ca parametru în lista de numere blocate și îl șterge din lista de contacte

#### removeFromBlackList()
- Metoda non-statică
- Adaugă numărul primit ca parametru în lista de numere și îl șterge din lista de numere blocate

### 2. Implementeaza un spell checker

Cel mai simplu spell checker este bazat pe o lista de cuvinte cunoscute (un dictionar). Daca scrii un text, fiecare cuvant trebuie cautat in lista de cuvinte cunoscute, iar daca nu este gasit, inseamna ca e eronat. Implementeaza un astfel de spell checker.

#### Ce intra in program?

1. Pe prima linie utilizatorul introduce numărul de cuvinte din lista de cuvinte cunoscute.
2. Apoi, pe câte o linie separată introduce fiecare cuvant din lista de cuvinte cunoscute.
3. Apoi, pe o linie, se introduce numărul de linii al textului de verificat.
4. Se introduc exact atâtea linii cu text (cuvinte separate prin spațiu).

#### Ce iese din program?

- Trebuie să afișam acele cuvinte din text care nu se regăsesc în lista de cuvinte cunoscute.
- Trebuie să verificăm fără să ținem cont de literele mici și mari.
- Cuvintele care nu sunt găsite în dicționar nu ar trebui să fie duplicate, dacă le regăsim de mai multe ori în text.

#### Exemplu

##### Input:
```
3
a
bb
cCc
2
a bb aab aba
ccc c bb aaa
```

##### Output:
```
c
aab
aaa
aba
```
