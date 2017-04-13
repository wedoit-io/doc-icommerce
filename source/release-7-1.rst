rel. 7.1 - 13/04/2017
=====================

Anomalie
--------

**Problema sul report ordini per le righe omaggio** - (rif: 12022)

Risolto problema sul report degli ordini che conteggiava gli importi delle righe omaggio (allienata alla funzionalità ordini salvati)

**Problema nel range di prezzi visualizzato nel form di raccolta ordine** - (rif: 12034)

E' stato risolto un problema nella visualizzazione dei range di prezzi recuperati dai listini. Venivano mostrati prezzi errati perchè non veniva considerato il catalogo come elemento discriminante.

**Problema con versioni obsolete di iB** - (rif: 11908)

Nel caso in cui una app risultasse obsoleta, veniva invitava l'utente ad aggiornare l'applicazione, indirizzandolo sull'AppStore. Veniva tuttavia proposta l'installazione di una App non corretta.

**Gestito funzionamento sotto https dell'appamanager** - (rif: 11929)

Ora l'infrastruttura server di iCommerce puo' gestire connessioni https

**wTrendy: Crash su report** - (rif: 12033)

E' stato risolto un problema di crash che si verificava durante la stama di un qualunque report in cui un codice pagamento non era presente nella tabella dei pagamenti, ma solo sull'anagrafica del cliente.

Novità
------

**wTrenty: Destinazione diversa su copia commissione** - (rif: 12030)

E' stata gestita una nuova variabile utilizzabile nel report copia commissione per visualizzaziare correttamente la destinazione diversa
