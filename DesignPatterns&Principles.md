
# TEME BACK-END 📚

## Lambda&Streams (mai puțin confortabil)


### 1. Crează un sistem de notificări
   - Interfața `Notification` are metoda `notifyUser()`.
   - Clasele `EmailNotification` și `SMSNotification` implementează interfața `Notification`.
   - Implementează un factory method care să creeze o notificare, în funcție de tipul notificării primit ca parametru.
   - Folosește factory method în codul client pentru a crea notificări și apoi apelează și metoda `notifyUser()` pentru a trimite notificările.

### 2. Crează o aplicație smart home
   - Aplicația lucrează cu senzori. Un senzor are un nume și o descriere.
     - Un senzor de mișcare, are în plus, o lungime fixă la care se activează (dacă un obiect ajunge mai aproape de senzor decât acea lungime fixă, senzorul se va activa).
     - Un senzor de fum, are în plus, un volum fix la care se activează (dacă senzorul detectează un volum de fum peste acel volum fix, se va activa).
   - Senzorii primesc date constant cu volumul și lungimea curentă, care sunt setate prin setteri.
   - Un `SensorSystem` (sistem centralizat de senzori) va conține o listă cu toți senzorii din casă.
   - Folosește pattern-ul `Observer`, astfel încât de fiecare dată când sistemul de senzori central primește o modificare la unul din senzori, să se afișeze un mesaj, dacă senzorul detectează mișcare sau fum.
   - Folosește și pattern-ul `Singleton`, prin care să implementezi un `Logger` care afișează informații utile pe parcursul programului (adică atunci când senzorii detectează mișcare sau fum).

### 2. Video store kata

Refactorizeaza proiectul format din clasele Customer, Movie si Rental, pentru a respecta cele mai bune practici.

Clasa Customer:

```
public class Customer {

    private String name;
    private List<Rental> rentals = new ArrayList<>();


    public Customer (String name) {
        this.name = name;
    }

    public void addRental (Rental rental) {
        rentals.add (rental);
    }

    public String getName () {
        return name;
    }

    public String statement () {
        double 				totalAmount 			= 0;
        int					frequentRenterPoints 	= 0;
        String 				result 					= "Rental Record for " + getName () + "\n";

        for (Rental rental :rentals) {
            double 		thisAmount = 0;

            // determines the amount for each line
            switch (rental.getMovie ().getPriceCode ()) {
                case Movie.REGULAR:
                    thisAmount += 2;
                    if (rental.getDaysRented () > 2)
                        thisAmount += (rental.getDaysRented () - 2) * 1.5;
                    break;
                case Movie.NEW_RELEASE:
                    thisAmount += rental.getDaysRented () * 3;
                    break;
                case Movie.CHILDRENS:
                    thisAmount += 1.5;
                    if (rental.getDaysRented () > 3)
                        thisAmount += (rental.getDaysRented () - 3) * 1.5;
                    break;
            }

            frequentRenterPoints++;

            if (rental.getMovie ().getPriceCode () == Movie.NEW_RELEASE
                    && rental.getDaysRented () > 1)
                frequentRenterPoints++;

            result += "\t" + rental.getMovie ().getTitle () + "\t"
                    + String.valueOf (thisAmount) + "\n";
            totalAmount += thisAmount;

        }

        result += "You owed " + String.valueOf (totalAmount) + "\n";
        result += "You earned " + String.valueOf (frequentRenterPoints) + " frequent renter points\n";


        return result;
    }
}
```

Clasa Movie:

```
public class Movie {

    public static final int CHILDRENS	= 2;
    public static final int REGULAR 	= 0;
    public static final int NEW_RELEASE = 1;

    private String title;
    private int priceCode;

    public Movie (String title, int priceCode) {
        this.title 		= title;
        this.priceCode 	= priceCode;
    }

    public int getPriceCode () {
        return priceCode;
    }

    public void setPriceCode (int code) {
        priceCode = code;
    }

    public String getTitle () {
        return title;
    }
}
```

Clasa Rental:

```
public class Rental {

    private Movie movie;
    private int daysRented;

    public Rental (Movie movie, int daysRented) {
        this.movie 		= movie;
        this.daysRented = daysRented;
    }

    public int getDaysRented () {
        return daysRented;
    }

    public Movie getMovie () {
        return movie;
    }
}
```





