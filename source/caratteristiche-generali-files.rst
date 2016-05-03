Caratteristiche generali dei files
==================================

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
