Import ordini da tracciato
==========================

:: warning:: L'import dei dati con questa modalità è deprecato. Utilizzare l'integrazione attraverso web services

I files di import (verso gli ipad), vengono creati dall'appmanager e
depositati nella cartella **C:\\Dropbox\\[nomeazienda]\\appmanager**.
Devono seguire le seguenti specifiche:

-  Il separatore dei campi e' il pipe
-  I files NON hanno l'intestazione di colonna
-  Le date hanno il formato ddmmyyyy (es: per 10 gennaio 2013, 10012013)
-  Il separatore decimale è la virgola
-  Le righe terminano senza separatore (es: FILLER20, no FILLER20\|)
-  I testi NON contengono MAI il carattere separatore \| (pipe).
-  Eventuali newline chr(10) + char(13), presenti nei testi sono
   sostituiti con il carattere speciale §
-  I testi non superano MAI i 4000 caratteri

Lista dei campi
---------------

+--------------------------+
| Campo                    |
+==========================+
| COD\_DITTA               |
+--------------------------+
| COD\_EXT\_ORD            |
+--------------------------+
| T\_DAT\_ORDINE           |
+--------------------------+
| NR\_ORD\_ORIG            |
+--------------------------+
| T\_COD\_CLIFOR           |
+--------------------------+
| T\_COD\_AGENTE           |
+--------------------------+
| T\_DAT\_CONS\_TES        |
+--------------------------+
| R\_DES\_NOTE             |
+--------------------------+
| T\_COD\_DEST             |
+--------------------------+
| R\_IND\_TIPO\_RIGA       |
+--------------------------+
| R\_COD\_ART              |
+--------------------------+
| R\_DES\_RIGA\_ORD        |
+--------------------------+
| R\_CDA\_UM1              |
+--------------------------+
| R\_CDA\_UM2              |
+--------------------------+
| R\_QTA\_1                |
+--------------------------+
| R\_QTA\_2                |
+--------------------------+
| R\_PREZZO\_1             |
+--------------------------+
| R\_PREZZO\_2             |
+--------------------------+
| TIPO\_UM                 |
+--------------------------+
| R\_IND\_TIPO\_OM         |
+--------------------------+
| R\_SCONTO\_1             |
+--------------------------+
| R\_SCONTO\_2             |
+--------------------------+
| R\_SCONTO\_3             |
+--------------------------+
| R\_SCONTO\_4             |
+--------------------------+
| R\_SCONTO\_5             |
+--------------------------+
| R\_SCONTO\_6             |
+--------------------------+
| R\_SCONTO\_IMP           |
+--------------------------+
| R\_MAG\_PERC1            |
+--------------------------+
| R\_MAG\_PERC2            |
+--------------------------+
| R\_MAG\_IMP              |
+--------------------------+
| R\_COD\_CONF             |
+--------------------------+
| R\_QTA\_COLLI            |
+--------------------------+
| T\_COD\_COND\_PAG        |
+--------------------------+
| T\_COD\_COND\_PAG\_DEP   |
+--------------------------+
| T\_COD\_OPERATORE        |
+--------------------------+
| T\_DAT\_CONS\_RIG        |
+--------------------------+
| FILLER5                  |
+--------------------------+
| FILLER6                  |
+--------------------------+
| FILLER7                  |
+--------------------------+
| FILLER8                  |
+--------------------------+
| FILLER9                  |
+--------------------------+
| FILLER10                 |
+--------------------------+
| FILLER11                 |
+--------------------------+
| FILLER12                 |
+--------------------------+
| FILLER13                 |
+--------------------------+
| FILLER14                 |
+--------------------------+
| FILLER15                 |
+--------------------------+
| FILLER16                 |
+--------------------------+
| FILLER17                 |
+--------------------------+
| FILLER18                 |
+--------------------------+
| FILLER19                 |
+--------------------------+
| FILLER20                 |
+--------------------------+
