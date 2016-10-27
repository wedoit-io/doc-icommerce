rel. 6.6 - 31/03/2016
=====================

Anomalie
--------

**Taglie & Colori : risolto problema con tastierino numerico** - (rif: 11047)

Risolto problema inserimento prezzo con decimali se il device è in inglese

**Cambiata gestione delle note di credito nella sezione Incassi** - (rif: 10746)

Nel modulo incassi, le note di credito non erano visibili nei report.
Inoltre, l'importo della nota di credito veniva decurtato dal totale delle scadenze per un cliente: in questo modo l'agente non poteva incassare tutte le scadenze senza considerare la nota di credito.

La nuova gestione, funziona in questo modo:

- E' possibile stornare una nota di credito singolarmente (quindi sarà visibile un incasso negativo relativo alla nota di credito)
- Il totale incassabile per un cliente, considera solo le scadenze con importo positivo: in questo modo l'agente può chiudere ed incassare tutte le scadenze e decidere in seguito se stornare la nota di credito
- Nel report degli incassi, è visibile "l'incasso" della nota di credito con importo negativo, che verrà sottratto al totale del documento.

In pratica ora le note di credito devono essere stornate singolarmente e non vengono più decurtate dal totale incassabile sul cliente.
La nota di credito è visibile nel report, ed è possibile incassare tutte le scadenze senza stornare eventuali note di credito.

**Codice pagamento non corretto in riga ordine veloce** - (rif: 11114)

Non veniva riportato correttamente il cambio del codice pagamento in testata ordini veloci rispetto a quello proposto da anagrafica cliente

Novità
------

**Taglie & Colori: copiare i dati del nuovo cliente** - (rif: 10868)

Aggiunta possibilità di copiare i dati del nuovo cliente da un'altra testata
