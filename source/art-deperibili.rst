Articoli Deperibili
===================

La legge italiana 27/2012, più nota con il nome "art. 62", impone che gli articoli classificati come "deperibili"
debbano avere condizioni di pagamenti particolari.

Per far fronte a questa normativa, iCommerce gestisce la problematica in questo modo:

1. Innanzitutto classifica gli articoli di questo tipo in base ad un opportuno campo del tracciato articoli chiamato COD\_DEPERIBILITA
2. Utilizza la gestione degli split dei dati per raggruppare gli articoli in ordini diversi.
3. Recupera il codice di pagamente del cliente dell'ordine
4. In base ad una tabella di decodifica predente in AppManager cambia il codice di pagamento in un altro.

Identificazione degli articoli deperibili
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Quando si estraggono i dati degli articoli occorre classificare con un codice qualunque gli articoli deperibili da quelli che non lo sono.
In realtà per l'AppManager non è importante sapere quale COD\_DEPERIBILITA identifica gli articoli deperibili.
Per AppManager tale valore viene usato solo come criterio per raggruppare gli articoli in ordini diversi.
Ovviamente il flag per la suddivisione degli ordini in base a tale codice, deve essere attivata.

Modifica del Codice di Pagamento
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
In AppManager, nel menu Gestione, è possibile configurare una tabella di trascodifica per modificare il codice di pagamento di un ordine.
La modifica viene fatta in questo modo:

1. Viene recuperato il codice di pagamente del cliente dell'ordine in esame
2. Viene cercato tale codice di pagamento nella tabella di trascodifica e, se trovato, viene modificato con quello configurato

.. note:: Questa gestione, particolarmente necessaria per la problematica dell'articolo 62, può essere utilizzata anche per cambiare il codice di pagamento a prescindere da tale problema.

