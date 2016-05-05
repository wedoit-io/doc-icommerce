Esportare i dati
================

Caratteristiche generali dei files
----------------------------------

I files delimitati di export devono seguire rigidamente le le seguenti caratteristiche:

1. Il separatore dei campi e' il pipe (simbolo \|)

esempio:
::

  CAMPO1|CAMPO2|CAMPO3

2. I files devono avere le intestazioni di colonna

esempio:
::

  COD_DITTA|CHIAVE|... ecc.

3. Nelle intestazioni di colonna non devono essere presenti spazi

esempio:
::

  COD_DITTA|CHIAVE   -> OK
  COD_DITTA | CHIAVE -> KO

4. Le date devono avere il formato ddmmyyyy con riempimento a sinistra con zeri

esempio:
::

  per 2 gennaio 2013, 02012013

5. Il separatore decimale è la virgola

esempio:
::

  Un euro e mezzo: 1,50

6. La data di ultima modifica (DAT\_ULT\_MOD) è un dato obsoleto, ma va sempre riempito a 01011900000000 per motivi di compatibilità.

7. Le righe non devono concludersi con un separatore

esempio:
::

  DAT_ULT_MOD     -> OK
  DAT_ULT_MOD\| -> KO

8.  I testi NON devono MAI contenere il carattere separatore \| (pipe). Se presente sostituirlo in fase di export.

9.  Eventuali newline chr(10) + char(13), presenti nei testi devono essere sostituiti con il carattere speciale §

10. I testi non devono mai superare i 4000 caratteri

.. warning:: Nell' esempio riportato, per comodità di lettura le colonne sono state allineate per favorire la leggibilità. Il file che deve essere creato NON DEVE contenere questi spazi.

Esempio tracciato città (file io\_citta.dat):

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

Clicca sul nome del file per vedere il dettaglio

Files articoli
~~~~~~~~~~~~~~

* `Articoli <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art.cs>`_
* `Articoli in lingua <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_lang.cs>`__
* `Unità di misura <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_um.cs>`__
* `Listini <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_listini_full.cs>`__
* `Sconti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_sconti.cs>`__
* `Storico articoli  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_stoart.cs>`__
* `Ultimi articoli acquistati  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_ultacq.cs>`__
* `Ultimi articoli venduti  <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_art_ultven.cs>`__
* `Giacenze articoli <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_giacenze.cs>`__


Files clienti
~~~~~~~~~~~~~

* `Clienti e Fornitori <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_gen.cs>`_
* `Agenti cliente <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_age.cs>`_
* `Blocchi <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_blo.cs>`_
* `Calendario girovisita <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_girovisita.cs>`_
* `Destinazioni <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_dest.cs>`_
* `Categorie <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_cate.cs>`_
* `Contatti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_detcon.cs>`_
* `Note <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_note.cs>`_
* `Testate documenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_testdoc.cs>`_
* `Righe documenti <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_righdoc.cs>`_
* `Scadenze <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_clifor_scadoc.cs>`_
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

* `Città <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_citta.cs>`_
* `Condizioni di pagamento <https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_condpag.cs>`_
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
