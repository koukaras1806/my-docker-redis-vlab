# Οδηγίες Εγκατάστασης για το Docker Redis VLab

## Προαπαιτούμενα

- Εγκατεστημένο Docker στο σύστημά σας. Μπορείτε να το κατεβάσετε και να το εγκαταστήσετε από [εδώ](https://docs.docker.com/get-docker/).

## Βήματα Εγκατάστασης

1. **Κλωνοποίηση του αποθετηρίου**:

   Πρώτα, κλωνοποιήστε το αποθετήριο από το GitHub:

   git clone https://github.com/koukaras1806/my-docker-redis-vlab.git
   cd my-docker-redis-vlab
2. **Κατασκευή της Docker εικόνας**:
   sudo docker build -t my-redis .

3. **Εκτέλεση του Docker container**:
   sudo docker run -d -p 6379:6379 my-redis

4. **Επιβεβαίωση ότι το container εκτελείται**:
   sudo docker ps

5. **Σύνδεση στο Redis**:
   sudo docker exec -it <container_id> redis-cli

