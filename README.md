# Docker Redis VLab

## Περιγραφή

Αυτό το εικονικό εργαστήριο (VLab) δημιουργεί ένα περιβάλλον Docker
για την εκτέλεση μιας υπηρεσίας Redis.
Το εργαστήριο έχει σχεδιαστεί για να παρέχει έναν εύκολο τρόπο ανάπτυξης
και δοκιμής του Redis σε απομονωμένο περιβάλλον.

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

sudo docker build -t my-redis .

3. **Εκτέλεση του Docker container**:

sudo docker run -d -p 6379:6379 my-redis

4. **Επιβεβαίωση ότι το container εκτελείται**:

sudo docker ps

5. **Σύνδεση στο Redis**:

sudo docker exec -it 07a76e6a29d2 redis-cli
