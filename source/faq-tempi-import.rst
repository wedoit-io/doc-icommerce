Import dati in ritardo
======================

Domanda
-------
Attualmente, nella schedulazione presente nel nostro gestionale, esportiamo i dati 2 volte al giorno. Alle 13.00 e alle 22.00.
Di per se ci mette poco a creare i file da esportare, ma non sappiamo quanto tempo passa prima che l'AppManager li riceva.


Risposta
--------
L'import dei dati sui nostri server è pianificato ogni 30 minuti.
Questo vuol dire che ogni 30 minuti viene effettuato un controllo sulle cartelle dropbox.
I tempi di acquisizione tuttavia possono dipendere da molti fattori, fra i quali l'eventuali aggiornamento di immagini del catalogo oppure code di elaborazione di altri clienti.
Per questi motivi non è possibile darantire un orario preciso per l'acquisizione dei files.
Nell'AppManager puoi comunque consultare il log delle importazioni e cercare la stringa *** FINE IMPORT ***
In corrispondenza di tale stringa puoi vedere l'orario e lo stato dell'acquisizione.
