Parametri progetto
==================

TODO

Parametri funzionali
~~~~~~~~~~~~~~~~~~~~

Numero sconti
-------------

Questo parametro indica il numero massimo di sconti che devono essere
visualizzato nel tablet. Se un cliente gestisce o desidera gestire solo
2 sconti, mettere il numero 2 in questo campo. Il valore predefinito, se
non impostato, è 6

Il prezzo minimo di vendita deve bloccare l'ordine
--------------------------------------------------

E' possibile definire un prezzo minimo per articolo sotto il quale non è
possible prendere ordini. Per impostare questa soglia è necessario agire
sulla personalizzazione del tracciato di esportazione dei dati
dell'articolo (**io\_art.dat**). Il campo da valorizzare è
**PREZZO\_MIN\_VEN**

Aggiungi questo numero di giorni alla data di consegna
------------------------------------------------------

Per rendere più rapida la raccolta degli ordini, è possibile aggiungere
un numero fisso di giorni alla proposta della data di consegna in fase
di inserimento dell'ordine. Se, ad esempio, si imposta questo campo a 2,
significa che se prendo l'ordine martedì, la data di consegna
che propone il programma sarà quella di giovedì (dopo 2 giorni) 
Il valore predefinito, se non impostato, è 0

Decimali da usare nelle quantità
--------------------------------

Inserire in questo campo il numero massimo di decimali che si vuole gestire.
Il valore predefinito, se non impostato, è 2

Numero di decimali per i prezzi
-------------------------------

Inserire in questo campo il numero massimo di decimali da usare per i prezzi.
Il valore predefinito, se non impostato, è 2

Lo sconto massimo di vendita deve bloccare l'ordine
---------------------------------------------------

Questo parametro attiva un controllo sul tablet che impedisce ad un
agente di inserire un ordine con uno sconto superiore ad una determinata
soglia. L'impostazione di tale soglia va effettuata nel tracciato di
estrazione dei dati, valorizzando opportunamente il campo
SCONTO\_MAX\_VEN del tracciato io\_art.dat

La quantità minima ordinabile deve bloccare l'ordine
----------------------------------------------------

Come per il prezzo minimo di vendita, anche in questo caso è possibile
definire una quantita minima sotto la quale non è possibile prendere
l'ordine. Il tracciato da personalizzare è quello degli articoli
(**io\_art.dat**) e il campo è **QTA\_MIN\_VEND**

Parametri di visualizzazione
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mostra la giacenza
------------------

Se impostato mostra il valore della giacenza nella lista dei prodotti

Mostra tutti i dati anche se sono agente
----------------------------------------

Nel license manager è possibile impostare, per ogni utente, il codice
agente definito nel gestionale. Nel caso in cui venga fatta questa
associazione, nell'iPad verranno mostrati ovunque solo i clienti
associati a quello specifico codice agente. Questo avviene sia nel
modulo Schede che nel modulo Ordini.

Nel modulo Schede, tuttavia, è possibile mostrare anche i dati dei
clienti associati ad altri agenti. Per fare questo bisogna attivare
questo flag.

Questa impostazione viene effettuata di solito per super-utenti che, pur
essendo profilati come agenti perchè raccolgono anche loro ordini,
vogliono vedere nel modulo schede anche i dati anche di altri agenti.

.. note:: Per consentire la visualizzazione di tutti i clienti anche nel modulo Ordini, bisogna togliere il codice agente dalla configurazione dell'utente.


Mostra UM secondaria invece della primaria in storico ordini
------------------------------------------------------------

Lo storico degli ordini mostra in lista l'unità di misura con sui è
stato preso l'ordine l'ultima volta. Impostando questo flag a true,
viene mostrata l'unita di misura secondaria.

Consenti modifica del prezzo in inserimento ordine
--------------------------------------------------

Se impostato a false, il prezzo in fase di inserimento ordine non è
modificabile

Verifica quantità ordinabile in colli
-------------------------------------

Se impostato a true, in fase di inserimento ordine viene effettuato un
controllo per l'eventuale ordine di un quantitativo di pezzi minore a
quello multiplo della confezione.

Mostra la disponibilità
-----------------------

Se impostato mostra il valore della disponibilità nella lista dei
prodotti

Mostra ultimo prezzo di acquisto in inserimento ordine
------------------------------------------------------

Se impostato a true, nello storico ordini viene mostrato l'ultimo prezzo
di acquisto.

Mostra ultimo prezzo rilevato
-----------------------------

Se impostato a true, viene mostrato il prezzo dell'ultimo documento di
trasporto (DDT)

Conenti modifica sconti in fase di inserimento ordine
-----------------------------------------------------

Se impostato a false impedisce la modifica degli sconti in fase di
inserimento ordine
