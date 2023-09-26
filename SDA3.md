# TEME BACK-END 📚

## Algoritmi array-uri

### 1. Determina castigatorul unui turneu.

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


## Algoritmi liste inlantuite



