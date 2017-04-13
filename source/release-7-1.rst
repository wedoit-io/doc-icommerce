rel. 7.1 - 13/04/2017
=====================

Anomalie
--------

**Problema sul report ordini per righe di tipo omaggio** - (rif: 12022)

Nel report ordini, veniva erroneamente conteggiato negli importi, anche le righe di tipo omaggio. Questo generava una inconsistenza nel totale del report rispetto ai dati mostrati nel gestionale.

**Problema con versioni obsolete** - (rif: 11908)

Nel caso in cui una app risultasse obsoleta, veniva chiesto all'utente ad aggiornare l'applicazione, indirizzandolo sull'AppStore. Tuttavia veniva proposta l'installazione di una App non corretta.

**Gestito funzionamento sotto https dell'AppManager** - (rif: 11929)

Ora l'infrastruttura server di iCommerce puo' gestire connessioni https

**wTrendy: Crash su report** - (rif: 12033)

E' stato risolto un problema di crash che si verificava durante la stama di un qualunque report in cui un codice pagamento non era presente nella tabella dei pagamenti, ma solo sull'anagrafica del cliente.


**wTrendy: Problema nella visualizzazione del range prezzi in raccolta ordine** - (rif: 12034)

E' stato risolto un problema nella visualizzazione dei range di prezzi recuperati dai listini. Venivano mostrati prezzi errati perchè non veniva considerato il catalogo come elemento discriminante nel calcolo del prezzo minimo e massimo.

Novità
------

**wTrendy: Destinazione diversa su copia commissione** - (rif: 12030)

E' stata gestita una nuova variabile utilizzabile nel report copia commissione per visualizzaziare correttamente la destinazione diversa
