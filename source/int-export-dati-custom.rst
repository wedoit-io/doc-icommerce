Esportare dati custom
=====================

Esiste un particolare tracciato, chiamato io_custom_fields.dat, che consente di aggiungere dati personalizzati in alcuni punti  applicativi predefiniti.
Tali dati vengono visualizzati, nell'iPad, in un specifica scheda che appare in vari punti del programma con il nome Altro.

.. figure:: int-export-dati-custom.png
   :alt:

Il tracciato io_custom_fields.dat deve essere creato secondo quanto descritto in :doc:`int-export-dati` è deve essere composto dai seguenti campi:

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
Il campo NOME deve contenere il valore albanumerico che si desidera mostrare come descrizione della label del campo personalizzato.

Campo VALORE
-----------
Questo campo deve contenere il valore da mostrare a destra della label (campo NOME)

Campo TIPO
-----------
Il campo TIPO, deve indicare il tipo di dato che si sta aggiungendo.

Può assumere i seguenti valori:

0. String
1. Date
2. Datatime
3. Integer
4. Decimal

Campo CHIAVE_PADRE
------------------
Campo attualmente NON GESTITO. Consentirà in futuro di gestire una gerarchia di dettagli.

Campo CONTESTO
---------------
Il campo CONTESTO determina il luogo in cui i dati custom devono comparire. I valori possibili sono:

- clienti
- fornitori
- prodotti
- leads

Per fare un esempio, se il tracciato contenesse il valore clienti in questo campo, il dato personalizzato verrebbe mostrato nella scheda Altro che in fondo ai dettagli della scheda clienti (il successivo campo VIS_MASK determina se la visualizzazione deve avvenire solo nel modulo schede, solo nel modulo ordini o in una combinazione dei 2 moduli).

Esempi:

========  =======================================================================
CONTESTO  Luogo in cui viene mostrato
========  =======================================================================
clienti   Modulo SCHEDE o ORDINI (dipende da VIS_MASK), Sottomodulo CLIENTI
leads     Modulo LEADS (dipende da VIS_MASK), Sottomodulo LEADS
========  =======================================================================


Campo COD_EXT
-------------
Il campo COD_EXT (codice esterno) rappresenta il vero e proprio collegamento fra il campo personalizzato e il dato anagrafico a cui esso afferisce, quindi:

- Nel caso in cui il contesto è clienti, COD_EXT deve contenere il codice cliente
- Nel caso in cui il contesto è fornitori, COD_EXT deve contenere il codice fornitore
- Nel caso in cui il contesto è prodotti, COD_EXT deve contenere il codice del prodotto
- Nel caso in cui il contesto è leads, COD_EXT deve contenere il codice del leads

Campo "VISUAL_MASK"
-------------------
Identifica il modulo in cui si dedidera mostrare i dati. Per specificare tale valore, si deve utilizzare una stringa di bit in cui ogni bit indica il modulo in cui il dato deve apparire.

La maschera di bit è la seguente:

::

  +----->   posizione 2 - Modulo Crm
  | +---->  posizione 1 - Modulo Ordini
  | | +---> posizione 0 - Modulo Schede
  | | |
  x x x

Esempi:

========  =============================
VIS_MASK  Modulo in cui viene mostrato
========  =============================
100       CRM
001       SCHEDE
011       SCHEDE e ORDINI
101       CRM e SCHEDE
========  =============================

