Funzionamento dei report
========================
L'applicazione iPad consente, a partire dalla versione 4.1.0, la
generazione, visualizzazione e condivisione di report. I template di
tali report vengono scaricati durante fase la sincronizzazione (sezione
*Generali* - *Modelli report*). I template possono essere modificati
cambiando il sorgente del template memorizzato in AppManager.

Il template è un documento HTML (comprensivo anche di regole di stile)
integrato con alcuni segnaposti. I segnaposti consentono
all'applicazione di popolare il report dinamicamente con valori
opportuni. La loro sintassi è: {{nomesegnaposto}}.

.. warning:: Fare una copia del report prima di modificarli. La modifica errata del report potrebbe causare una errata visualizzazione del report e, in casi particolari, il crash dell'applicazione. Si consiglia di effettuare una copia di backup del template prima di iniziarne l'editing.

Segnaposti di base
------------------

I seguenti segnaposti sono utilizzati dall'app per il rendering della
pagina html:

-  {{#documentHeader}} ... {{/documentHeader}}
-  {{#pageHeader}} ... {{/pageHeader}}
-  {{#pageContent}} ... {{/pageContent}}
-  {{#pageFooter}} ... {{/pageFooter}}
-  {{#pageNumber}} ... {{/pageNumber}}

È possibile modificare il codice contenuto in tali segnaposti, inserendo
direttive html. Si consiglia di non rimuovere tali segnaposti.

Contesti
--------

L'applicazione supporta la generazione di report in vari contesti
applicativi:

+---------------------+--------------------------------------+
| Contesto            | Descrizione                          |
+=====================+======================================+
| Ordini salvati      | Visibile nella form Ordini/salvati   |
+---------------------+--------------------------------------+
| Ordini inviati      | Visibile nella form Ordini/inviato   |
+---------------------+--------------------------------------+
| Incassi             | Visibile nella form Incassi          |
+---------------------+--------------------------------------+
| Ordini veloci       | Visibile nella form Ordini veloci    |
+---------------------+--------------------------------------+
| Copia commissione   | Visibile solo con modulo wTrendy     |
+---------------------+--------------------------------------+

È a discrezione di chi modifica il report la scelta di cosa far
vedere/non far vedere, ed eventualmente la modifica delle regole di
stile/layout html.

Formato e dimensione del Logo
-----------------------------

I report standard prevedono un logo di 512 x 512 pixel con estensione
JPG. Questa è la dimensione prevista dal layout di stampa dei report
standard. Se si effettua una personalizzazione del layout la dimensione
del logo potrebbe variare.

Il logo può essere modificato accedendo in AppManager. Nella form
Progetti selezionare la scheda Dati. Nella colonna **Logo** cliccare
sulla graffetta e caricare il nuovo file.

.. note:: Per rendere effettive le modifiche è indispensabile comunicare ad WEDO Srl, con la procedura di supporto, l'avvenuto caricamento del logo personalizzato
