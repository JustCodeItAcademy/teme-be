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

##### Exemplu:
Simbolul `>` reprezinta input-ul oferit de utilizator.

```
> --help
These are all the commands:
config     Get and set a username.
add        Add a file to the index.
log        Show commit logs.
commit     Save changes.
checkout   Restore a file.

> 
These are all the commands:
config     Get and set a username.
add        Add a file to the index.
log        Show commit logs.
commit     Save changes.
checkout   Restore a file.

> config
This command gets and sets a username

> fsgfsdgsg
This command does not exist
```

#### Varianta 2
Acum vrem sa implementam comenzile `config`, `add` si `status`.
Fisierul `index.txt` va stoca username-ul care va fi setat prin comanda config.
Fisierul `config.txt` va stoca numele tuturor fisierelor care vor fi adaugate prin comanda add in "staging area".
Cele doua fisiere vor fi stocate intr-un folder numit `vcs`. La acelasi nivel cu folderul, vor fi fisierele normale din "repository"

Structura ar trebui sa fie urmatoarea:

```
.
├── vcs
│   ├── config.txt
│   └── index.txt
├── file1.txt
└── file2.txt
```
Avem deci un folder care are niste fisiere unde stocam informatii despre repository, iar in rest avem doua fisiere normale din repository.
Unul dintre ele este in staging area, iar unul nu, in exemplul de mai sus.

Comanda `config` va adauga in fisierul `confix.txt` username-ul utilizatorului.
Daca este deja un nume setat, acesta va fi suprascris.

Comanda `add` va adauga numele unui anumit fisier in `index.txt`.
Daca fisierul nu exista, atunci se va trata acest caz exceptional si utilizatorul va fi informat.

Comanda `status` va afisa numele fisierelor care sunt in staging area (adica numele fisierelor care sunt in index.txt) si numele fisierelor care nu sunt in staging area (adica celelalte fisiere).

##### Exemplu:
Simbolul `>` reprezinta input-ul oferit de utilizator.

```
> config john
username set to 'john'

> add file1.txt
'file1.txt' was added to index

> add non_existing_file.txt
can't find 'non_existing_file.txt'

> status
tracked files:
file1.txt
untracked files:
file2.txt

> add file2.txt
'file2.txt' was added to index

> status
tracked files:
file1.txt
file2.txt
untracked files:
no untracked files
```
#### Detalii de implementare
Vei avea nevoie sa creezi o clasa si sa retii calea spre folderul vcs si spre fisierele `config.txt` si `index.txt`
In constructor, putem ca daca folderul nu exista deja, sa il cream noi din cod:

```
    private final String VCS_DIRECTORY = "./vcs";
    private final String CONFIG_FILE = VCS_DIRECTORY + "/config.txt";
    private final String INDEX_FILE = VCS_DIRECTORY + "/index.txt";

    public SVCS() {
        File vcsDir = new File(VCS_DIRECTORY);
        if (!vcsDir.exists()) {
            vcsDir.mkdir();
        }
    }
```
Foloseste aurmatoarea structura de cod pentru a citi, linie cu linie, textul dintr-un fisier.
De exemplu, citim din fisierul index.txt:

```
BufferedReader reader = new BufferedReader(new FileReader(INDEX_FILE));
String line;
while ((line = reader.readLine()) != null) {
    System.out.println(line);
}
reader.close();
```

Foloseste apoi urmatoarea a scrie o linie de text intr-un fisier:
De exemplu, scriem in fisierul index.txt:

```
PrintWriter writer = new PrintWriter(new FileWriter(INDEX_FILE, true));
writer.println("o noua linie in fisier");
writer.close();
```



