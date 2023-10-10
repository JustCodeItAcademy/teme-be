
# TEME BACK-END 📚

## Lambda&Streams (mai puțin confortabil)


### 1. Crează un sistem de notificări**
   - Interfața `Notification` are metoda `notifyUser()`.
   - Clasele `EmailNotification` și `SMSNotification` implementează interfața `Notification`.
   - Implementează un factory method care să creeze o notificare, în funcție de tipul notificării primit ca parametru.
   - Folosește factory method în codul client pentru a crea notificări și apoi apelează și metoda `notifyUser()` pentru a trimite notificările.

### 2. Crează o aplicație smart home**
   - Aplicația lucrează cu senzori. Un senzor are un nume și o descriere.
     - Un senzor de mișcare, are în plus, o lungime fixă la care se activează (dacă un obiect ajunge mai aproape de senzor decât acea lungime fixă, senzorul se va activa).
     - Un senzor de fum, are în plus, un volum fix la care se activează (dacă senzorul detectează un volum de fum peste acel volum fix, se va activa).
   - Senzorii primesc date constant cu volumul și lungimea curentă, care sunt setate prin setteri.
   - Un `SensorSystem` (sistem centralizat de senzori) va conține o listă cu toți senzorii din casă.
   - Folosește pattern-ul `Observer`, astfel încât de fiecare dată când sistemul de senzori central primește o modificare la unul din senzori, să se afișeze un mesaj, dacă senzorul detectează mișcare sau fum.
   - Folosește și pattern-ul `Singleton`, prin care să implementezi un `Logger` care afișează informații utile pe parcursul programului (adică atunci când senzorii detectează mișcare sau fum).




