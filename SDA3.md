# TEME BACK-END 📚

## Algoritmi array-uri

### 1. Determina castigatorul unui turneu (tournament winner)

**Input:**
	
    Competitions = [ [“HTML”, “C#”], [“C#”, “Python”], [“Python”, “HTML”]]
    Results = [0,0,1]

**Output:** “Python”

In acest exemplu, avem un array de array-uri denumit `competitions`, ca input. 
In fiecare sub-array, avem 2 echipe.
Practic, fiecare echipa joaca cu fiecare echipa, o singura data.
Prima echipa din subarray este echipa care joaca acasa, de ex: `HTML`, iar a doua este echipa care joaca in deplasare, de exemplu `C#`, din perechea [‘HTML’,’C#’]
Nu poate avea loc un rezultat de egalitate. O echipa primeste 3 puncte daca castiga si 0 puncte daca pierde.
Castigatorea turneului este echipa cu cele mai multe puncte.

Mai avem un input, si anume array-ul `results`. Fiecare element din results specifica cine a castigat fiecare meci din `competitions`.
In `results`, valoarea 0 inseamna ca a castigat echipa care joaca in deplasare, iar valoarea 1 inseamna ca a castigat echipa care joaca acasa.

De exemplu, `results[0]` are valoarea 0, asta inseamna ca ne uitam in `competitions[0]` si ne dam seama ca ‘C#’ a castigat, pentru ca ea este echipa in deplasare.
Rezultatul turneului din exemplu este ca: 
- C# invinge HTML 
- Python invinge C#
- Python invinge HTML.

    HTML - 0 puncte
    C# - 3 puncte
    Python - 6 puncte.

Avand la dispozitie un astfel de input, scrie un algoritm care sa determine castigatorul turneului.

**HINT**: foloseste un array de array-uri pentru a stoca competitiile venite ca input, si o mapa (in care cheia este echipa si valoarea este scorul obtinut) pentru output

### 2. Subsir al unui array (validate subsequence)

Avand la dispoizitie doua array-uri, verifica daca al doilea este subsir al primului.
De exemplu, daca array-ul [1,3,4] este subsir al array-ului [1,2,3,4]
Dar si [2,4] este subsir al array-ului [1,2,3,4].
E nevoie sa se pastreze ordinea, dar elementele nu trebuie sa fie neaparat consecutive.

**Input**:
```
array1: [5,1,2,,25,5,-1,8,10]
array2: [1,6,-1,10]
```

**Output**: 
```
true (array2 este subsir al lui array1)
```

**HINT**: Parcurge array-ul cu 2 pointeri

### 3. Gaseste primul element duplicat dintr-un array (first duplicate value)
**Input**: 
```
[2,1,5,2,3,3,4]
```
**Output**: 
```
2 - este primul element care se repeta (al doilea 3 apare dupa al doilea 2)
```
**HINT**: Varianta "brute force" va lua fiecare element cu fiecare, iar varianta mai eficienta va folosit un Set

### 4. Subsir de suma 0 (zero sum subarray)
Scrie o functie care sa determina daca exista un subsir cum suma 0 intr-un array.

**Input**: 
```
[-5,-5,2,3,-1]
```
**Output**: 
```
true - subsitul [-5,2,3] are suma 0
```
**HINT**: 

Suma de la fiecare index este suma pana acolo + elementul de la acel index. 

De exemplu, suma pana la elementul -1 este suma pana la elementul 4 (adica 7), la care adunam -1 (si obtinem 6)

Array-ul de sume pana la fiecare element ar arata asa: [4  1  3  7  6  1  8]

Exista un array de suma 0, daca suma de la inceput pana la un index mai este regasita si pana la alt index.

De la 4 la -5 suma este 1, dar si de la 4 la -3 suma este 1. Deci suma de la 2 la -5 nu are cum sa fie alta decat 0.

### 5. Cea mai mica diferenta dintre 2 array-uri (smallest difference)
Daca ai 2 array-uri, gaseste elementele (unul din primul si celalalt din al doilea) care sa dea suma minima

**Input**:
```
Arr1: [-1,5,10,20,28,3]
Arr2: [26,134,135,15,17]
```
**Output**: 
```
[28,26]
```
**Hint**:
Cea mai simpla solutie este sa generezi toate perechile de numere si sa gasesti diferenta minima.

Alta solutie este sa sortezi inainte cele 2 array-uri, si apoi apoi sa parcurgi cu 2 pointeri (cate unul pentru fiecare array)

### 6. Elementele cu o anumita suma (two number sum)
Avand un array, gaseste 2 elemente a caror suma este egala cu n.
**Input**:
```
Arr1: [3,5,-4,,8,11,1,-1,6]
n: 10
```
**Output**: 
```
un posibil output este: [11,-1]
```

### 7. Doua perechi cu aceeasi suma (two pairs of same sum)
Avand un array, gaseste 2 perechi de elemente astfel incat a+b = c+d

**Input**:
```
arr = {3, 4, 7, 1, 12, 9}
```
**Output**: 
```
"{4,12}{7,9}", pentru ca 4+12=7+9
```
**Hint**:
Pentru output, genereaza o mapa in care cheia este suma, si valoarea este o pereche care are acea suma

### 8. Gaseste 2 perechi simetrice (find symetric pairs)
Avand o matrice (un array de array-uri de 2 elemente, adica un array de perechi), gaseste doua perechi simetrice.
**Input**:
```
arr[][] = [{1, 2}, {3, 4}, {5, 9}, {4, 3}, {9, 5}]
```
**Output**: 
```
"{3,4}{4,3}" este un posibil output, pentru ca cele doua perechi au aceleasi elemente in ordine inversa
```
**Hint**:
Pentru output, genereaza o mapa in care cheia va fi primul element din pereche, iar valoarea al doilea element din pereche

### 9. Gaseste timpul minim de executare a task-urilor (minimum waiting time)
Ai un array care reprezinta indicii reprezinta task-urile pe care le ai de facut, iar elementele de la fiecare index reprezinta cat dureaza sa faci fiecare task.

De exemplu, pentru [3,2,1,2,6], primul task dureaza 0 secunde, al doilea task dureaza 3 secunde (adica al doilea task asteapta sa se termine primul, ca mai apoi sa se execute).

Al treilea task dureaza 3+2=5 secunde (adica asteapta dupa primele 2 sa se execute)

Care este timpul minim de executare a task-urilor? Poti sa modifici ordinea in care se executa si apoi sa calculezi timpul.

**Hint**:
Tot timpul vei cauta sa executi task-ul care dureaza cel mai putin prima data.

Astfel ca daca sortezi array-ul, vei obtine [1,2,2,3,6].

Atentie: toate task-urile de dupa un anumit task vor astepta dupa acel task.

De exemplu, dupa primul task (de la indicele 0) vor astepta o secunda toate celelalte task-uri (de la indicele 1 pana la final)

## Algoritmi liste inlantuite



