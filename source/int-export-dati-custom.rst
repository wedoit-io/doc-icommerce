Esportare dati custom
=====================

Esiste un particolare tracciato, chiamato io_custom_fields.dat, che consente di aggiungere valori personalizzati in alcuni punti  applicativi predefiniti.

Tale tracciato deve essere creato secondo le specifiche generai è deve essere composto dai seguenti campi:

- CHIAVE
- COD_DITTA  
- NOME 
- VALORE 
- TIPO 
- CHIAVE_PADRE 
- CONTESTO 
- COD_EXT 
- VISUAL_MASK  
- POSIZIONE_VALORE  
- ORDINAMENTO 
- POSIZIONE_NOME 
- TIPO_DATO  
- DAT_ULT_MOD

Vediamo ora nel dettaglio il significato di ogni campo.

Campo CHIAVE
------------
Il campo chiave deve contenere un valore univoco della riga. In questo campo non sono ammessi valori duplicati

Campo COD_DITTA
---------------
Il campo COD_DITTA deve contenere il codice univoco della ditta presente nel gestionale da cui si effettua l'esportazione.
Tutti record devono essere marcati con tale codice.

Campo NOME
----------
Il compo nome deve contenere il valore albanumerico che si desidera mostrare come descrizione della label del campo personalizzato.


Tali contesti riguardano:

1. Articoli
2. Clienti
3. Prodotti


Dove mostrare i dati
---------------------
Il tracciato io_custom_fields.dat prevede 2 campi che consentono di specificare il luogo dell'app in cuisi desidera far comparire i dati personalizzati

### Campo "VISUAL_MASK"

Identifica il modulo in cui si dedidera mostrare i dati.
Per specificare tale valore, si utilizza una stringa di bit.
Ogni bit indica un modulo.

I valori possibili, partendo da destra, sono:

pos. 0 : modulo schede
pos. 1 : modulo ordini
pos. 2 : modulo CRM


```
+----->   crm
| +---->  ordini
| | +---> schede
| | |
x x x
```

Esempi:

VIS_MASK |Modulo in cui viene mostrato
---------|-----------------------------
100      | CRM
001      | SCHEDE
011      | SCHEDE e ORDINI
101      | CRM e SCHEDE


### Campo "CONTESTO"

In campo contesto indica all'applicazione la tipologia di dato
custom che si sta importando.

Può assumere i seguenti valori:

* clienti 
* fornitori
* prodotti
* leads

Esempi:

CONTESTO | Luogo in cui viene mostrato
---------|-----------------------------
clienti  | Modulo SCHEDE o ORDINI (dipende da VIS_MASK), Sottomodulo CLIENTI
leads    | Modulo LEADS (dipende da VIS_MASK), Sottomodulo LEADS


Note sull'esempio:
---
Nell'esempio presente in questa cartella, ipotizziamo di dover esportare un campo custom chiamato xx_note sul cliente.

La creazione del tracciato viene fatta nella procedura Elabora_ExportCustomFieldsClienti.





-------------------



::

    CHIAVE|COD_DITTA|CODICE|DESCRIZIONE   |CAP   |PROVINCIA|DAT_ULT_MOD
    A001  |ACME     |A001  |ABANO TERME   |35031 |PD       |01011900000000
    A002  |ACME     |A002  |ABBADIA       |      |CO       |01011900000000
    A002A |ACME     |A002A |ABBADIA SOPRA |      |CO       |01011900000000
    A003  |ACME     |A003  |ABBADIA       |      |TO       |01011900000000
    A003A |ACME     |A003A |ABBADIA ALPINA|      |TO       |01011900000000
    A004  |ACME     |A004  |ABBADIA CERRE |26834 |LO       |01011900000000
    A005  |ACME     |A005  |ABBADIA LARIAN|23821 |LC       |01011900000000
    A006  |ACME     |A006  |ABBADIA SAN S.|53021 |SI       |01011900000000
    A007  |ACME     |A007  |ABBASANTA     |09071 |OR       |01011900000000


.. note:: E' possibile scaricare i seguenti files di esempio `cliccando qui <http://files.apexnet.it/iOrder/ic.company-name.zip>`_


Specifiche dei tracciati
------------------------

Clicca sul nome del file per vedere il dettaglio. 

.. note:: I tracciati con un asterisco sono quelli minimi (o essenziali) per la raccolta ordini.

Files articoli
~~~~~~~~~~~~~~

* `Articoli(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art.cs>`_
* `Articoli in lingua <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_lang.cs>`__
* `Unità di misura(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_um.cs>`__
* `Listini(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_listini_full.cs>`__
* `Sconti(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_sconti.cs>`__
* `Storico articoli(*)  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_stoart.cs>`__
* `Ultimi articoli acquistati  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_ultacq.cs>`__
* `Ultimi articoli venduti  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_ultven.cs>`__
* `Giacenze articoli <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_giacenze.cs>`__


Files clienti
~~~~~~~~~~~~~

* `Clienti e Fornitori(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_gen.cs>`_
* `Agenti cliente(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_age.cs>`_
* `Blocchi(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_blo.cs>`_
* `Calendario girovisita <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_girovisita.cs>`_
* `Destinazioni(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_dest.cs>`_
* `Categorie <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_cate.cs>`_
* `Contatti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_detcon.cs>`_
* `Note <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_note.cs>`_
* `Testate documenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_testdoc.cs>`_
* `Righe documenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_righdoc.cs>`_
* `Scadenze(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_scadoc.cs>`_
* `Fatturato <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_fatt.cs>`_

Files leads
~~~~~~~~~~~

* `Anagrafica leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_leads.cs>`_
* `Permessi operatori CRM <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_acccrm.cs>`_
* `Associazione operatori leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_accessi.cs>`_
* `Dettagli contatti leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_detcon.cs>`_
* `Note leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_note.cs>`_
* `Testate offerte leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_testoff.cs>`_
* `Righe offerte leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_rigoff.cs>`_
* `Sconti leads <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_lead_sconti.cs>`_
* `Campagne <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_campagne.cs>`_
* `Canali di vendita <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_canali_vendita.cs>`_

Files tabelle di base
~~~~~~~~~~~~~~~~~~~~~

* `Città(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_citta.cs>`_
* `Condizioni di pagamento(*) <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_condpag.cs>`_
* `Condizioni di pagamento in lingua <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_condpag_lang.cs>`_
* `Nazioni <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_nazioni.cs>`_
* `Porti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_porto.cs>`_


Files wTrendy
~~~~~~~~~~~~~

.. warning::

    I tracciati wTrendy sono utilizzati solo dall'applicazione
    specifica per il settore calzaturiero chiamata
    `wTrendy <https://itunes.apple.com/it/app/wtrendy/id642932906?mt=8>`_

* `Modalità di spedizione <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_mod_sped.cs>`_
* `Assortimenti per articolo <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_articoli_assortimenti.cs>`_
* `Lista assortimenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_assortimenti.cs>`_
* `Taglie assortimenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_taglie_assortimenti.cs>`_
* `Taglie cataloghi <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi.cs>`_
* `Taglie cataloghi articolo <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi_art.cs>`_
* `Taglie estensioni <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_taglie_estensioni.cs>`_
* `Taglie sviluppi <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_taglie_sviluppi.cs>`_
* `Taglie sviluppi articolo <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_taglie_sviluppi_art.cs>`_
* `Combinazioni <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_var_combinazioni.cs>`_
* `Liste colori <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_liste_colori.cs>`_
* `Liste materiali <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_liste_materiali.cs>`_
* `Regole <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_regole.cs>`_
* `Classi di sconto <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_classi_sconto.cs>`_
* `Assortimenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_assortimenti.cs>`_


Files speciali
~~~~~~~~~~~~~~

* `Tracciato per campi custom <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_custom_fields.cs>`_
* `Catalogo multimediale <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_multimedia.cs>`_
* `Reports <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_reports.cs>`_

Visibilità articoli per agente
------------------------------

E' possibile definire un set di articoli da associare a uno o più agenti. Per fare questo sono stati predisposti 3 tracciati specifici:

* `Cataloghi <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi.cs>`_
* `Cataloghi Articolo <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi_art.cs>`_
* `Cataloghi Agente <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi_agente.cs>`_

Cataloghi
~~~~~~~~~
Il tracciato dei cataloghi deve contenere l'elenco anagrafico di tutti i cataloghi disponibili. 
Può essere usato ad esempio per una promozione o una collezione di prodotti.

Cataloghi Articolo
~~~~~~~~~~~~~~~~~~
Il tracciato cataloghi articolo contiene l'associazione fra il catalogo e gli agenti che lo possono utilizzare. 
Ggenti associati ad un catalogo vedono solo gli articoli in esso contenuti.

Cataloghi Agente
~~~~~~~~~~~~~~~~
Questo tracciato contiene l'associazione fra l'agente e i suoi cataloghi.
Un Agente può vedere tutti gli articoli dei cataloghi a cui è associto









 
