# Iris-recognition-with-image-comparison
Progetto di "Principi e modelli della percezione", inerente al riconoscimento biometrico dell'iride.
Il progetto mira a implementare un sistema di riconoscimento dell'iride attraverso l'uso di tecniche di visione artificiale. Utilizzando OpenCV, NumPy e altri strumenti, il programma segmenta, normalizza e confronta due immagini di iridi, calcolando la loro somiglianza, attraverso la distanza di Hamming, per l'autenticazione biometrica.

Funzionalità
- Segmentazione dell'iride: Estrazione dell'iride da un'immagine usando thresholding.
- Normalizzazione dell'iride (unwrapping): Conversione dell'immagine dell'iride in una rappresentazione piana.
- Estrazione delle caratteristiche: Creazione di un vettore che rappresenta l'iride in modo unico.
- Confronto tra iridi: Calcolo della distanza tra due iridi per determinare la somiglianza.

0. Prerequisiti
 Prima di aver eseguito il codice bisogna assicurarsi di aver installato i seguenti pacchetti e    strumenti:

 1. INSTALLARE IL SITEMA PYTHON COMPATIBILE CON IL NOSTRO OS (versione 3.10 al momento della creazione del progetto)

 Questo progetto richiede l'installazione dei seguenti pacchetti e librerie di sistema: build-  essential, cmake, libgtk-3-dev, liblapack-dev, libx11-dev, python3-dev, che possono essere installati con il comando:
sudo apt install build-essential cmake libgtk-3-dev liblapack-dev libx11-dev python3-dev
Inoltre, è necessario installare pip, il gestore di pacchetti Python, con il comando:
sudo apt install python3-pip

2. INSTALLARE I PACCHETTI PYTHON NECESSARI
   
Il progetto utilizza le seguenti librerie Python:
- opencv-python per l'elaborazione delle immagini.
- numpy per le operazioni matematiche.
  Installa i pacchetti con:
  pip install opencv-python numpy

3. IMMAGINI DI IRIDI
   
  Il codice utilizza due immagini di iridi. Assicurati di avere due file di immagini (ad esempio iris1.jpg e iris2.jpg) nella stessa cartella del progetto o di specificare il percorso corretto nel codice.

STRUTTURA DEL CODICE 

confrontoiride.py è il file principale che contiene il codice per la segmentazione, normalizzazione, estrazione delle caratteristiche e confronto delle immagini delle iridi.

Funzioni principali:
- segment_iris(image): Segmenta l'iride da un'immagine utilizzando il thresholding.
- normalize_iris(iris_image): Normalizza l'immagine dell'iride in una rappresentazione piana.
- extract_iris_features(image): Estrae un vettore di caratteristiche (hash) unico per l'iride.
- compare_irises(iris1_features, iris2_features): Calcola la distanza tra le caratteristiche di due iridi utilizzando la distanza euclidea.

Esecuzione del codice:
Una volta installati tutti i prerequisiti, puoi eseguire il codice tramite:
pip install opencv-python

Se il file confrontoiride.py si trova nella stessa directory del terminale, lo script elaborerà le due immagini e calcolerà la somiglianza tra le iridi.
Struttura del Codice
Durante l'esecuzione, il programma caricherà le immagini, segmenterà l'iride, la normalizzerà, estrarrà le caratteristiche e calcolerà la somiglianza tra le due iridi, restituendo una distanza numerica. 


POSSIBILI PROBLEMI E SOLUZIONI

Errore: ImportError: No module named cv2
Assicurati di aver installato OpenCV correttamente con il comando:
pip install opencv-python

Errore: FileNotFoundError: No such file or directory: 'iris1.jpg'
Verifica che le immagini iris1.jpg e iris2.jpg si trovino nella stessa cartella dello script. In caso contrario, aggiorna i percorsi nel codice.

Errore: OpenCV Error: Unable to read image
Verifica che le immagini non siano corrotte e siano nel formato giusto (ad esempio, JPG o PNG).


Test.py

Questo è un semplice programma Python che verifica la corretta installazione delle librerie. Una volta eseguito, importa le librerie necessarie e stampa le versioni per confermare che tutto sia configurato correttamente. Utile prima di eseguire lo script principale.
 

