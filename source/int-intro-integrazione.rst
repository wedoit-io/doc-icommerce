Introduzione all'integrazione
=============================

L'integrazione con iCommerce, prevede 2 diverse modalità

* Invio dei dati del gestionale agli iPad
* Ricezione dei dati inseriti o modificato dagli utenti

Invio dei dati all'iPad
-----------------------
L'invio dei dati deve essere fatto attraverso l'invio di files ascii in formato delimitato.
Attualmente l'unica modalità supportata prevede che il trasferimento
di dati avvenga attraverso l'installazione di un profilo Dropbox.

I files ascii creati devono essere messi nella cartella [gestionale] presente nella struttura di cartelle condivise.

Ricezione di dati dall'iPad
---------------------------
Nelle prime versioni di iCommerce anche la ricezione dei dati avveniva
leggendo un file delimitato che veniva depositato nella cartella appmanager dal server (AppManager)

Per motivi di affidabilità, questa modalità non è più supportata.

.. warning::

    La ricezione dei dati attraverso l'utilizzo di files delimitati non è più supportata

L'integrazione deve avvenire leggere i dati di ritorno attraverso l'utilizzo delle
di API Rest
