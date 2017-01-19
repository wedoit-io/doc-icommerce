AppManager
===========

L'AppManager è la parte di infrastruttura che si pone fra i dispositivi mobili e il gestionale. 
Tutti i dati che dal gestionale vengono inviati agli iPad e viceversa transitano dall'AppManager.

Moduli
~~~~~~

E' composto dai seguenti moduli:

1. Interfaccia web per l'accesso alle funzioni di consultazione
2. Web Services per l'esposizione dei dati verso gli iPad (es: listini)
3. Web Services per l'esposizione dei dati verso il gesionale (es: ordini)
4. Servizio di caricamento dei dati provenienti dal gestionale (attraverso l'utilizzo di Dropbox)

Funzionalità
~~~~~~~~~~~~

Dall'interfaccia web dell'AppManager è possibile visualizzare:

1. I dati ricevuti dal gestionale (es: listini, anagrafiche generali, ecc.)
2. I dati ricevuti dagli iPad (es: ordini, clienti, note, ecc..)
3. La configurazione su come trattare i dati (es: come suddividere gli ordini)
4. I Log dei caricamenti dati
5. Funzionalità accessorie (es: gestione art. 62 o girivisita)

Web services
~~~~~~~~~~~~
A partire dalla versione 6.14, l'app accetta esclusivamente connessioni criptate verso domìni diversi da *.apexnet.it.
I clienti che hanno una installazione AppManager sui propri server, devono quindi munisti di certificato digitale da installare su IIS.
Il certificato deve rispettare i seguenti criteri:
1. Non deve essere self-signed, ma deve essere rilasciato da un ente certificatore valido.
2. La versione TLS del protocollo deve essere la 1.2. Questa caratteristica non dipende dal certificato ma dalla configurazione di IIS. Occorre quindi verificare se la versione di IIS utilizzata supporta il protocollo TLS 1.2
3) Deve essere attivo il ForwardSecrecy. Anche questa è una configurazione di IIS.

Ecco alcuni riferimenti utili per chi deve configurare il Web Server:

* https://www.hass.de/content/setup-your-iis-ssl-perfect-forward-secrecy-and-tls-12
* http://tecadmin.net/enable-tls-on-windows-server-and-iis/
