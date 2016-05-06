Ordini su nuovi clienti
=======================

Domanda
-------
A volte capitita di dover raccogliere un ordine su un nuovo cliente che ancora non è presente in anagrafica.
Come posso fare ?

Risposta
--------
La raccolta ordini può essere effettuata anche su nuovi clienti (non presenti nelle anagrafiche dell'iPad).

Per attivare questa funzione, è sufficiente inserire, nel gestionale, uno o più clienti con partita iva ``99999999999`` (undici volte 9).

.. note::

    Impostando il codice ``99999999999`` nella partita iva, il programma di estrazione imposta il campo
    `FLG_NEW_CLIFOR <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_gen.cs#L152>`_ del
    tracciato clienti a -1. E' questo flag che marca il cliente come cliente template

Questi clienti, detti **clienti template**, nell'iPad vengono visualizzati e trattati in modo speciale.

In particolar modo, nell'iPad:

1. Non vengono mostrati fra gli altri clienti presenti in anagrafica
2. Sono visibili solo in una apposita funzione utilizzabile durante
   l'inserimento di un nuovo ordine.
3. I dati anagrafici di tali clienti non vengono visualizzati e non sono
   utilizzabili come valori di default. Infatti, in fase di inserimento
   ordine, è l'utente che deve specificarli.
4. Possono essere associati sconti e listini. In questo modo è possibile
   differenziare i prezzi anche su clienti nuovi creando più clienti
   template.

In fase si inserimento di un nuovo ordine, quando si apre la finestra di
selezione del cliente, in alto a sinistra è presente una icona che
consente di mostrare gli utenti template in alternativa a quelli
codificati in anagrafica.

La visualizzazione dei clienti template segue la logica
dell'associazione cliente / agente, quindi:

1. Se ad un cliente template viene associato il codice agente X, solo
   tale agente potrà usare quel cliente template
2. Se ad un cliente template non viene associato alcun agente, tutti gli
   agenti potranno utilizzarlo per inserire ordini su nuovi clienti
