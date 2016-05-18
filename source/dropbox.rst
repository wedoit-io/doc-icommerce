Dropbox
=======
Per sincronizzare i dati un progetto, occorre installare `Dropbox`_ sul server su cui è installato il gestionale.
In questo documento, sono riportati i passi per effettuare una corretta installazione.

Registrazione di un account
---------------------------
Per ogni installazione è necessario registrare un account dedicato che deve essere utilizzato per il cliente.
Una singola registrazione può essere usata anche per più aziende.

-  Collegarsi al sito http://www.dropbox.com e clicccare su **Sign in**
-  Registrare un nuovo account seguendo le indicazioni presenti.

Installazione di Dropbox
------------------------

L’installazione di dropbox su un server deve essere fatta seguendo alcuni accorgimenti particolari.
Dropbox nasce per funzionare su ambienti desktop e non prevede che sul computer possano
collegarsi più utenti (ad esempio via terminal server).
Tuttavia, seguendo alcuni piccoli accorgimenti, l'installazione può essere effettuata senza problemi.

-  Scaricare il client `Dropbox <https://www.dropbox.com/downloading>`__
   ed eseguire il setup
-  Inserire le credenziali dell’ account dropbox
-  Effettuare l’installazione di **tipo avanzato** e specificare la
   cartella **C:\\**. In questo modo Dropbox verrà installato in **C:\Dropbox**
-  Cliccare col pulsante destro del mouse nell’icona presente nella
   tray area in basso a destra, andare nelle preferenze e deselezionare
   l’opzione “Avvia dropbox all’avvio del sistema” (figura 1)
-  Uscire da Dropbox

.. figure:: dropbox_properties.png
   :alt:

.. note:: Dopo aver effettuato l'installazione, verificare che il programma Dropbox.exe sia stato installato nella cartella giusta, ovvero: C:\\Program Files(x86)\\Dropbox\\Client\


Condivisione della cartella Dropbox
-----------------------------------

Dopo aver effettuato l’installazione di Dropbox, comunicare a WEDO Srl i dati dell’ account con cui si è appena effettuata
l’installazione.

In seguito a questa richiesta, WEDO Srl provvederà ad effettuare la condivisione di una cartella di progetto che sarà utilizzata dal connettore per
interscambiare i files.

Kill e Restart programma dropbox
--------------------------------
La procedura di estrazione dei dati dal gestionale, dipende dal connettore utilizzato.
Nella maggior parte dei casi, sarà effettuata da un batch di Windows configurato nelle operazioni pianificate.

In corrispondenza del comando che effettua l'esportazione, si suggerisce di effettuare un kill del processo Dropbox.exe
e un successivo restart.

Esempio di batch per l'export con il gestionale Business:

.. code-block:: bash

    taskkill -F -IM "Dropbox.exe"
    "C:\\Bus\\busnet.exe" admin . ACME Business Bnieibus /B D:\bus\asc\Export.bub ACME

    set app="%programfiles(x86)%\Dropbox\Client\Dropbox.exe"
    start "Restart Dropbox" %app% -B
