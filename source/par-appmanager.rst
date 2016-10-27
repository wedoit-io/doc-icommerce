Parametri AppManager
===================

.. figure:: par-appmanager.png
   :alt:
   
Raggruppamento delle righe in ordini
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sotto il menu Anagrafiche / Parametri, è presente una videata in cui è possibile impostare:

1. Raggruppamento dell'ordine per codice famiglia
2. Raggruppamento dell'ordine per data consegna
3. Raggruppamento dell'ordine per codice destinazione
4. Raggruppamento dell'ordine per codice deperibilità articolo

Queste 4 opzioni possono essere configurate a piacimento per determinare in che modo gli acquisti effettuati dagli agenti devono essere raggruppati.

La Raccolta ordini è concepita per raccogliere gli articoli in una modalità molto simile a quella di un sito di e-commerce.
Di fatto quindi, l'agente raccoglie una lista di articoli che ha venduto ma non sa, o comunque può non dover sapere, come questa lista deve comporre l'ordine.

Agendo su questi flag, gli articoli venduti vengono raggruppati in base alle impostazioni configurate.

Immaginiamo per esempio, di aver attivato il flag di suddivisione per "data di consegna".
L'agente prende gli ordini su 4 articoli ma in uno di questi imposta una data di consegna diversa.
In questo caso AppManager crea 2 ordini. Uno con i primi 3 articoli e uno con quello con data consegna differente.

Ordinamento righe ordine
~~~~~~~~~~~~~~~~~~~~~~~

Se si desidera cambiare l'ordine con il quale gli articoli devono essere aggiunti all'ordine, è possibile agire su ```Ordinamento righe```.

L'ordinamento può essere configurato nel seguente modo:

- In base all'inserimento originale (Come da presa ordine)
- Ordinamento per descrizione


Validazione dati device
~~~~~~~~~~~~~~~~~~~~~~~

I dati che un utente può modificare sull'ipad sono:

1. Ordini
2. Clienti
3. Note dei clienti
4. Leads
5. Note dei leads

Per ognuna di queste categorie, è possibile attivare la validazione del dato da interfaccia utente.

Tale impostazione blocca di fatto l'esportazione ```automatica``` del dato per il gestionale fino a quando un operatore ```manualmente``` non effettua la validazione da interfaccia.

Con questa funzione è possibile quindi fare in modo che gli ordini, prima di essere resi disponibili per il gestionale, subiscano una verifica da parte di un operatore.



