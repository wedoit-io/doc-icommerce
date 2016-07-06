AppManager
===========

L'AppManager è la parte di infrastruttura che si pone fra i dispositivi mobili e il gestionale. 
Tutti dati che dal gestionale vengono inviati agli iPad e viceversa transitano dall'AppManager.

L'AppManager è composto da vari moduli applicativi:

1. Interfaccia web per l'accesso alle funzioni di consultazione
2. Web Services per l'esposizione dei dati verso gli iPad (es: listini)
3. Web Services per l'esposizione dei dati verso il gesionale (es: ordini)
4. Servizio di caricamento dei dati provenienti dal gestionale (attraverso l'utilizzo di Dropbox)

Dall'interfaccia web dell'AppManager (http://am.apexnet.it) è possibile visualizzare, per ogni progetto:

1. I dati ricevuti dal gestionale (es: listini, anagrafiche generali, ecc.)
2. I dati ricevuti dagli iPad (es: ordini, clienti, note, ecc..)
3. La configurazione su come trattare i dati (es: come suddividere gli ordini)
3. I Log dei caricamenti dati
4. Funzionalità accessorie (es: gestione art. 62 o girivisita)

