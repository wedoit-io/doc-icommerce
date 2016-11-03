Incassi
=======

Nel modulo ordini, è presente una funzione che consente di creare un `brogliaccio` degli incassi che l'agente può effettuare presso il cliente.

Selezionando il cliente, il programma mostra un elenco con tutte le sue scadenze aperte.

Nella lista vengono mostrate:

* le fatture (importi positivi che l'agente deve incassare dal cliente)
* le note di credito (importi negativi che il cliente deve ricevere)

L'agente può effettuare l'incasso in 2 diverse modalità.

Incasso multiplo
----------------
Per inserire un incasso multiplo occorre selezionare il cliente e toccare la label `Incassa` 
situata in alto a destra della maschera.

Il programma mostra un form in cui all'agente viene proposto di incassare il totale di tutte le scadenze aperte.
Vengono escluse da questa somma tutte le note di credito (a importo negativo), che sono incassabili ma solo singolarmente con l'incasso singolo.

A questo punto l'agente può confermare il totale proposto dall'applicazione, o può eventualmente inserire solo
una parte dell'incasso.

Nel primo caso tutte le scadenze positive vengono impostate come `Incassate`, nel secondo caso invece 
il programma `spalma` l'incasso su tutte le scadenze fino aal raggiungimento dell'incasso inserito ed inserisce, se neccessario, un incasso parziale su una delle scadenze aperte.

Incasso singolo
---------------
L'incasso singolo viene effettuato toccando la singola scadenza. 
Nel caso di scadenze positiva, si apre una maschera in cui è possibile aggiungere l'incasso che può essere:

1. Completo. Confermando l'importo proposto
2. Parziale. Modificando l'importo proposto con una valore differente.

Nel caso di incassi di note di credito, il programma chiede all'utente se si desidera inserire lo storno 
della nota di credito. 

.. note:: Non è possibile inserire lo storno parziale di una nota di credito.

Registrazione degli incassi
-----------------------------
Gli incassi inseriti nel programma non transitano automaticamente nel gestionale.
Dopo aver inserito gli incassi, l'agente deve effettuare manualmente la stampa degli incassi effettuati e inviarla
alla propria azienda che provvederà a registrare l'incasso nel gestionale.

.. warning:: Gli incassi inseriti nel programma non vengono inviati automaticamente nel gestionale

Se l'incasso è stato registrato dalla azienda, nella successiva sincronizzazione non verrà più visualizzato.

