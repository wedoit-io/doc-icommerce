Articoli deperibili
===================

La legge italiana 27/2012, più nota con il nome "art. 62", impone che gli articoli classificati come "deperibili"
debbano avere condizioni di pagamenti particolari.

Per far fronte a questa normativa, iCommerce gestisce la problematica in questo modo:

1. Classifica gli articoli deperibili in base al campo del tracciato articoli chiamato COD\_DEPERIBILITA
2. Suddivide gli ordini che contengono articoli deperibili (paragrafo precedente).
3. Modifica il codice di pagamento degli ordini che contengono articoli deperibili

Identificazione degli articoli deperibili
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Quando si estraggono i dati degli articoli occorre classificare con un codice qualunque gli articoli deperibili da quelli che non lo sono.
In realtà per l'AppManager non è importante sapere quale COD\_DEPERIBILITA identifica gli articoli deperibili in quanto tale valore viene usato solo come criterio per raggruppare gli articoli in ordini diversi.

.. warning:: Abilitare il flag per la suddivisione degli ordini in base al codice deperibilita

Modifica del Codice di Pagamento
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
In AppManager, nel menu Gestione, è possibile configurare una tabella di trascodifica per modificare il codice di pagamento di un ordine.
La modifica viene fatta in questo modo:

1. Viene recuperato il codice di pagamente del cliente dell'ordine in esame
2. Viene cercato tale codice di pagamento nella tabella di trascodifica e, se trovato, viene modificato con quello configurato

.. note:: Questa gestione, particolarmente necessaria per la problematica dell'articolo 62, può essere utilizzata anche per cambiare il codice di pagamento a prescindere da tale problema.

