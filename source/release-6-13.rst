rel. 6.13 - 20/12/2016
=====================

Anomalie
--------
**Visualizzazione prezzo in riga documento delle schede** - (rif: 11703)

In alcuni casi la visualizzazione del prezzo della riga documento risultava troncato

**Schermata bianca in navigazione schede su iPhone** - (rif: 11767)

In alcune visualizzioni delle schede (solo su iphone) talvolta poteva comparire una pagina intermedia bianca durante la navigazione

**Risolto Crash App in fase di aggiornamento Catalogo e  Reports** - (rif: 11702)

Risolto Crash che si verificava sistematicamente per l'app scaricata dallo store Apple.
Tale malfunzionamento si è verificato a causa di un cambiamento del comportamento di iOS nei confronti di una libreria di terze parti utilizzata da iOrder. La regressione era comparsa con la versione 6.11.

**Risolto problema su aggiornamento Catalogo con molti elementi** - (rif: 11828)

Talvolta, nel caso di cataloghi con moltissimi elementi, poteva avvenire un crash dell'applicazione.
Ora è stata ottimizzata la gestione della cache interna del catalogo e la gestione della memoria del dispositivo durante il download dei files.

**Errato Warning alla conferma dell'incasso mutiplo** - (rif: 11696)

Il messaggio di warning "L'importo incassato è maggiore di..." a volte veniva mostrato anche quando non serviva. Il calcolo del totale incasso multiplo non considerava correttamente gli arrotondamenti.

Novità
------

**Implementazione Gestione Attività** - (rif: 11714)

Nel dettaglio dei Leads è stata aggiunta la scheda di dettaglio delle attività. In questa scheda l'operatore può:

1. Consultare attività assegnate ad altri operatori (in sola lettura)
2. Modificare lo stato di una attività esistente a lui associata
3. Inserire nuove attività sul lead 

Le nuove attività confluiscono in AppManager e vengono esposte al gestionale attraverso specifici web services.


