# Docker Redis VLab
Γιώργος Κούκος 18390054

## Περιγραφή

Αυτό το εικονικό εργαστήριο (VLab) δημιουργεί ένα περιβάλλον Docker
για την εκτέλεση μιας υπηρεσίας Redis.
Το εργαστήριο έχει σχεδιαστεί για να παρέχει έναν εύκολο τρόπο ανάπτυξης
και δοκιμής του Redis σε απομονωμένο περιβάλλον.

### Βασικά Χαρακτηριστικά του Redis

- **In-Memory Storage**: Το Redis αποθηκεύει όλα τα δεδομένα στη μνήμη RAM, πράγμα που το καθιστά εξαιρετικά γρήγορο, 
δεδομένου ότι οι αναγνώσεις και οι εγγραφές στη μνήμη είναι πολύ ταχύτερες από αυτές σε αποθηκευτικούς δίσκους.
- **Snapshots (RDB)**: Περιοδική αποθήκευση της κατάστασης της βάσης δεδομένων σε ένα αρχείο.
- **Append-only File (AOF)**: Καταγραφή κάθε εντολής που τροποποιεί τη βάση δεδομένων, 
η οποία μπορεί να επαναπαιχθεί κατά την επανεκκίνηση για την αποκατάσταση της κατάστασης.
- **Pub/Sub Messaging**: Το Redis υποστηρίζει το μοντέλο publisher/subscriber για την επικοινωνία μηνυμάτων. 
Αυτό επιτρέπει τη δημιουργία εφαρμογών που βασίζονται σε real-time notifications.
- **High Availability**: Το Redis Sentinel προσφέρει λειτουργίες αυτόματης μεταγωγής (failover), παρακολούθησης και ειδοποίησης, εξασφαλίζοντας υψηλή διαθεσιμότητα του συστήματος.


## Χαρακτηριστικά

- **Docker**: Χρησιμοποιείται για την πακετοποίηση της εφαρμογής 
και την εξασφάλιση της φορητότητας και της απομόνωσης.
- **Redis**: Ένας δημοφιλής και ταχύς in-memory key-value store που χρησιμοποιείται 
ευρέως για caching και message brokering.



## Πώς να χρησιμοποιήσετε το VLab

### Προαπαιτούμενα

- Docker εγκατεστημένο στο σύστημά σας. Μπορείτε να το κατεβάσετε από [εδώ](https://docs.docker.com/get-docker/).

### Βήματα

1. **Κλωνοποίηση του αποθετηρίου**:

   
   git clone https://github.com/koukaras1806/my-docker-redis-vlab.git
   cd my-docker-redis-vlab

2. **Κατασκευή της Docker εικόνας**:

docker build -t my-redis .

3. **Εκτέλεση του Docker container**:

sudo docker run -d -p 6379:6379 my-redis


4. **Επιβεβαίωση ότι το container εκτελείται**:

docker ps

5. **Σύνδεση στο Redis**:

docker exec -it 07a76e6a29d2 redis-cli
redis -cli -h 127.0.0.1 -p 6379

