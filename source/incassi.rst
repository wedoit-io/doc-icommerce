Incassi
=======

Nel modulo ordini, se attivato, è disponibile una funzionalità per l'inserimento degli incassi.
Tale modulo, dopo aver selezionato un cliente, elenca tutte le scadenze aperte per il cliente selezionato.

Nella lista vengono mostrate:

* le fatture (importi positivi che l'agente deve incassare dal cliente)
* le note di credito (importi negativi che il cliente deve ricevere)

In questa lista, l'agente può inserire l'incasso in 2 diverse modalità.

Incasso multiplo
----------------
Per inserire un incasso multiplo occorre selezionare il cliente e toccare la label `Incassa` 
situata in alto a destra della maschera.

Si aprira un form in cui l'agente viene proposto il totale di tutte le scadenze positive.
Vengono infatti escluse da questa somma tutte le note di credito che sono incassabili solo singolarmente (si veda incasso singolo).

A questo punto l'agente può confermare il totale proposto dall'applicazione, o può eventualmente inserire solo
una parte dell'incasso.

Nel primo caso tutte le scadenze positive vengono impostate come `Incassate`, nel secondo caso invece 
il programma `spalma` l'incasso su tutte le scadenze fino ad inserire un eventuale incasso parziale su una delle scadenze aperte.


Incasso singolo
---------------
L'incasso singolo viene evvettuato toccando la singola scadenza. Nel caso di scadenze positiva, si apre
una maschera in cui è possibile aggiungere l'incasso che può essere:

1. Completo, confermando l'importo proposto
2. Parziale. Modificando l'importo proposto con una valore differente.

Nel caso di incassi di note di credito, il programma chiede all'utente se si desidera inserire lo storno 
della nota di credito. 

..note: Non è possibile inserire lo storno parziale di una nota di credito.

Registrazione degli incassi
-----------------------------
Gli incassi inseriti nel programma non transitano automaticamente nel gestionale.
Dopo aver inserito gli incassi, l'agente deve effettuare la stampa degli incassi effettuati e inviarla
alla propria azienda.

..note: Gli incassi non vengono inseriti automaticamente nel gestionale

Se l'incasso è stato registrato dalla azienda, nella successiva sincronizzazione non verrà più visualizzato.

