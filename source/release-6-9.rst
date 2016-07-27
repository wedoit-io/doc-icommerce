rel. 6.9 - 27/07/2016
=====================

Anomalie
-----------

**Fix per il problema in fase di ricerca** - (rif: 11270)

Risolto un problema che, dopo aver effettuato una ricerca ed aver aggiornato i dati, a volte mandava l'app in crash

**Risolto il problema di visualizzazione del pagamento nel report degli ordini veloci** - (rif: 11205)

Risolto il problema di visualizzazione della modalità di pagamento nei report.

**Proposta destinazione in testata ordine** - (rif: 11355)

Su ordine veloce, in testata ordine, ora la proposta delle destinazioni avviene come su form ordine.

**Default quantità su Ordini da Storico** - (rif: 11360)

Il default (al tap sulla spunta a sinistra) della quantità proposta per ordine da storico viene cercato su entrambe le quantità dell'archivio storico prodotti.
L'unità di misura ricercata deve coincidere con quella di vendita. 


**Allineato comportamento ricalcolo prezzo in Storico** - (rif: 11361)

Ora sia dalla lista principale dello storico che nel dettaglio del form ordine il prezzo viene sempre ricalcolato al variare della quantità

Novità
------

**Aggiunta gestione 'fasce sconto'** - (rif: 11163)

Aggiunta la possibilità di visualizzare l'importo della singola riga ordine e del totale dell'ordine, con colori diversi.
Il colore si basa sulla % di sconto applicato alla riga/ordine e alla configurazione delle due diverse fasce sconto sul license manager.
La funzionalità è disabilitata di default.

**Modifiche ordini veloci per Piacentina** - (rif: 10830)

In fase di creazione della testata negli ordini veloci, è possibile selezionare una o più sorgenti (storico cliente e listino specifico per cliente). In questo modo ,vengono recuperati gli articoli che corrispondono al criterio selezionato e creata una riga ordine per ogni articolo, già compreso di prezzi e sconti. La visibilità delle sorgenti dati e la possibilità di modificarne lo stato, sono guidate da appositi parametri attivabili solo su richiesta.


