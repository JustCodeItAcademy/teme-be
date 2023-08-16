# TEME BACK-END 📚

## Exceptii 

### 1. Citeste de la tastatura un string care reprezinta un array.
De exemplu, vei citi string-ul "1 7 10 2 6 5", adica un string format din numere separate de cate un spatiu.

Defineste o functie care extrage numerele din string si returneaza un array de numere intregi (format din acele numere extrase)

Foloseste metoda parseInt() pentru a converti din string in numar si trateaza cazul exceptional in care nu se poate converti. De exemplu, pentru "1 abc 10 2 6 5", abc nu se va putea converti in numar, si atunci se va renunta cu totul la generarea array-ului.

### 2. Scrie o functie care sa retuneze ziua din saptamana in functie de un numar primit ca input.
De exemplu, 1 este Luni, 2 este Marti, etc.
Trateaza cazul exceptional in care ce primeste functia ca input este nu numar in afara intervalului 1-7.

Ar trebui să creezi o clasă numită `Candidate` care să aibă următoarele proprietăți:
* `name` - Numele candidatului
* `numberOfVotes` - Totalul voturilor primite de candidat

### 3. Creaza propriul tau GIT
Un sistem de control al versiunilor este un software care poate urmări modificările implementate într-un program. Un sistem de control al versiunilor își amintește cine a modificat fișierul, când și de ce. Acesta iti permite sa revii si la versiunile anterioare.

În acest proiect, trebuie să implementezi un sistem simplu de control al versiunilor. 

Aruncă o privire la comenzile pe care va trebui să le implementezi în acest proiect:

```
config setează sau afișează numele autorului unui commit;
--help afișează pagina de ajutor;
add adaugă un fișier la lista fișierelor urmărite sau afișează această listă;
log arată toate commit-urile;
commit salvează modificările fișierului și numele autorului;
checkout vă permite să comutați între commit-uri și să restaurați o stare anterioară a fișierului.
```
#### Varianta 1
În această etapă, programul tau ar trebui să poată accepta o singura comanda și, în funcție de ea, să afișeze informații de ajutor.
* Daca comanda este un string vid ("") sau --help, atunci se va afisa un help page cu descrierea tuturor comenzilor
* Daca comanda este una valida, atunci se va afisa o descriere a comenzii
* Daca comanda nu exista, atunci se va afisa "comanda inexistenta"

Nu au nevoie de o bucla care sa afiseze in mod repetat un meniu. Programul porneste, utilizatorul introduce o comanda, si programul se opreste apoi.


* `numberOfVotes` - Totalul voturilor primite de candida





