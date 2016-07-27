rel. 6.9 - 27/07/2016
=====================

## Anomalie

**_Fix per il problema in fase di ricerca_** - (rif: 11270)

Risolto un problema che, dopo aver effettuato una ricerca ed aver aggiornato i dati, a volte mandava l'app in crash

**_Risolto il problema di visualizzazione del pagamento nel report degli ordini veloci_** - (rif: 11205)

Risolto il problema di visualizzazione della modalità di pagamento nei report.

**_Proposta destinazione in testata ordine_** - (rif: 11355)

Su ordine veloce, in testata ordine, ora la proposta delle destinazioni avviene come su form ordine.

**_Default quantità su Ordini da Storico_** - (rif: 11360)

Il default (al tap sulla spunta a sinistra) della quantità proposta per ordine da storico viene cercato su entrambe le quantità dell'archivio storico prodotti.
L'unità di misura ricercata deve coincidere con quella di vendita. 


**_Allineato comportamento ricalcolo prezzo in Storico_** - (rif: 11361)

Ora sia dalla lista principale dello storico che nel dettaglio del form ordine il prezzo viene sempre ricalcolato al variare della quantità

### Novità

**_Aggiunta gestione 'fasce sconto'_** - (rif: 11163)

Aggiunta la possibilità di visualizzare l'importo della singola riga ordine e del totale dell'ordine, con colori diversi.
Il colore si basa sulla % di sconto applicato alla riga/ordine e alla configurazione delle due diverse fasce sconto sul license manager.
La funzionalità è disabilitata di default.

**_Modifiche ordini veloci per Piacentina_** - (rif: 10830)

In fase di creazione della testata negli ordini veloci, è possibile selezionare una o più sorgenti (storico cliente e listino specifico per cliente). In questo modo ,vengono recuperati gli articoli che corrispondono al criterio selezionato e creata una riga ordine per ogni articolo, già compreso di prezzi e sconti. La visibilità delle sorgenti dati e la possibilità di modificarne lo stato, sono guidate da appositi parametri attivabili solo su richiesta.


