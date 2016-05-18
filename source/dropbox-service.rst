Dropbox come servizio
=====================

. warning:: L'installazione di Dropbox come servizio non è più consigliata. Si veda documento installazione dropbox

Per attivare un nuovo progetto, per prima cosa è necessario installare
il programma di sincronizzazione dei file `Dropbox`_ sul server su cui è
installato il gestionale.

Per farlo bisogna registrarsi sul sito di `Dropbox`_ con l’account del
cliente. Ovviamente, se il cliente non ha un account, occorre crearne
uno per lui

.. note:: Dropbox deve essere installato in modalità server. L’installazione server consente l’esecuzione di dropbox come servizio e permette la sincronizzazione dei files anche quando la console di Windows non è attiva.

Dopo aver creato l’account dropbox del cliente, occorre comunicare il
nome dell’account ad WEDO, che attiverà la condivisione della
cartella per l’interscambio dei dati dal server appmanager a quello del
cliente

Installazione come servizio
---------------------------

L’installazione standard di Dropbox, non prevede l’utilizzo del
programma su server Windows. Tuttavia con poche semplici operazioni, è
possibile risolvere il problema. L’installazione come servizio, permette
di eseguire Dropbox senza essere costretti a effettuare il login sul
server. Ci sono due modalitè di installazione, a seconda della versione
installata di Windows Server.

1. Installazione del Resource Kit di Windows (solo per versioni precedenti a Windows 2012)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Installare, prima di tutto, il `Resource Kit di Windows`_ Si tratta di
una utility ufficiale di Microsoft non presente nell’ installazione di
base del sistema operativo Windows server. All’interno del resource kit
è presente un tool che consente di eseguire un eseguibile generico come
servizio di windows.

-  Scaricare `w2003 Resource Kit`_
-  Installarlo cliccando Next ad ogni richiesta. Durante l’installazione
   verrà mostrato un messaggio che informa l’ utente di incompatibilità
   note del programma con sistema operativo in uso. Ignorare questo
   messaggio.

2. Registrazione di un account dropbox
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Collegarsi al sito http://www.dropbox.com e clicccare su **Sign in**
-  Registrare un nuovo account seguendo le indicazioni presenti.
-  Comunicare al supporto WEDO l’utente di dropbox appena creato.

3. Installazione del client Dropbox
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Scaricare il client `Dropbox <https://www.dropbox.com/downloading>`__
   ed eseguire il setup
-  Inserire le credenziali dell’ account dropbox
-  Effettuare l’installazione di **tipo avanzato** e specificare la
   cartella **C:\\**. In questo modo Dropbox verrà installato in **C:\Dropbox**
-  Clicccare col pulsante destro del mouse nell’ icona presente nella
   tray area in basso a destra, andare nelle preferenze e deselezionare
   l’opzione “Avvia dropbox all’avvio del sistema” (figura 1)
-  Uscire da Dropbox

.. figure:: dropbox_properties.png
   :alt:

4. Configurazione di Dropbox come servizio
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Versioni precedenti a Windows Server 2012
-----------------------------------------

Aprire la shell dos e digitare il seguente comando: (fare attenzione al
path e agli spazi)

.. code-block:: bash

  C:> sc create DropBoxService binPath=“C:\Program Files (x86)\Windows Resource\Tools\srvany.exe” DisplayName=“Dropbox Service”


Windows Server 2012 e successive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Scaricare **srvany.exe** da questo `link`_

Copiare il file nella cartella **C:\tmp**

Aprire la shell dos e digitare il seguente comando: (fare attenzione al
path e agli spazi)


Otterremo a questo punto una conferma del tipo

.. code-block:: bash

  [SC] CreateService SUCCESS

Andare nei servizi e modificare le proprietà del servizio chiamato
Dropbox

.. figure:: dropbox_service.png
  :alt:

Terminati questi passaggi **NON AVVIARE IL SERVIZIO**, aprire il
registry e andare in:

::

   HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Dropbox

-  Creare una nuova chiave chiamata ‘’’Parameters’’’
-  Aggiungere una nuova stringa (tipo REG\_SZ) dal nome “Application”
-  Valorizzarla con il path (eseguibile compreso) di esecuzione di
   dropbox, ottenibile dallo shortcut del menu dei programmi, ad esempio

  .. code-block:: bash
    :emphasize-lines: 3,5

    C:\Users\Administrator.XXXXXXXX\AppData\Roaming\Dropbox\bin\Dropbox.exe


-  Chiudere il registry ed avviare il servizio
-  Fare il logoff ed eseguire un test di funzionamento

5. Condivisione della cartella Dropbox
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Dopo aver effettuato l’installazione di Dropbox, occorre comunicare ad
WEDO Srl i dati dell’ account con cui si è appena effettuata
l’installazione.

In seguito a questa, WEDO provvederà ad effettuare la condivisione
di una cartella di progetto che sarà utilizzata dal connettore per
interscambiare i files.

.. _link: /files/srvany.zip


.. _Dropbox: http://www.dropbox.com/
.. _Resource Kit di Windows: http://www.microsoft.com/en-us/download/confirmation.aspx?id=17657
.. _w2003 Resource Kit: http://www.microsoft.com/en-us/download/confirmation.aspx?id=17657
