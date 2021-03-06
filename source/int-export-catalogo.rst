Esportare il catalogo
=====================
L' esportazione delle immagini per la creazione del catalogo, può essere
effettuata in 2 diverse modalità:

-  Modalità basata su tracciato record
-  Modalità basata su struttura file system

In entrambi i casi, i file da esportare devono essere copiati nella
cartella multimedia di `dropbox <https://www.dropbox.com>`__.

.. note:: L'impostazione di una delle 2 modalità descritte è determinata dall'esistenza del file io\_catalogo.dat nella cartella multimedia.

Esportazione basata su tracciato
--------------------------------

Questa modalità prevede che tutti i files vengano copiati nella cartella
principale multimedia. Non devono essere create sottocartelle.

Nell' iPad, per rappresentare le immagini in una struttura a cartelle,
viene utilizzato un apposito tracciato record in cui, per ogni immagine,
può essere associata una specifica gerarchia di cartelle.

Il numero massimo di livelli disponibili è 4.

Un stesso file può essere presente più volte in cartelle differenti
senza necessariamente essere presente più volte nella cartella. E'
sufficiente che venga inserito più volte nel tracciato record.

Creare il tracciato io\_catalogo.dat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il tracciato `io\_catalogo.dat <../io_catalogo>`__ deve essere creato
nella cartella principale in cui vengono messi i files multimediali.

La gerarchia con cui vengono mostrati i dati è definita dai campi L1,
L2, L3, L4.

Il catalogo risultante nel dispositivo rispecchierà la struttura
inserita nel tracciato tramite i nomi dei file e i livelli di
appartenenza.

Esempio:

Il seguente tracciato, mostra 2 cartelle (Detersivi e Prodotti casa).
All' interno della cartella Detersivi viene mostrata la cartella
Naturale. ALl' interno della cartella Prodotti casa vengono mostrate 3
immagini. Sotto la cartella Naturale vengono mostrate 2 immagini.

::

    NOMEFILE     | TITOLO    | COD_ART | L1        | L2       | L3 | L4 | ORDINAMENTO | DAT_ULT_MOD
    Listino1.pdf | Listino 1 | COD001  | Detersivi | Naturale |    |    |           1 | 01012010
    Listino2.pdf | Listino 2 | COD002  | Detersivi | Naturale |    |    |           2 | 01012010
    Listino3.pdf | Listino 3 | COD003  | Prodotti  |          |    |    |           3 | 01012010
    Listino4.pdf | Listino 4 | COD004  | Prodotti  |          |    |    |           4 | 01012010

.. warning:: L'ordinamento viene applicato all'interno del suo livello.

Visualizzazione risultante:

::

  -  Cartella Detersivi
  -  Cartella Naturale
  -

     -  File Listino 1

  -

     -  File Listino 2

  -  Cartella Prodotti casa
  -  File Listino 3
  -  File Listino 4
  -  File Listino 5


.. warning:: Nell' esempio riportato, per comodità di lettura le colonne sono state allineate. Il file che deve essere creato NON DEVE contenere questi spazi.


Esportazione basata su filesystem
---------------------------------

L' export da filesystem, prevede che i file vengano copiati ed
eventualmente raggruppati in cartelle e sottocartelle, all'interno della
sopracitata cartella **multimedia**.

Il catalogo risultante nel dispositivo rispecchierà fedelmente la
struttura dei file e cartelle desiderata.

.. warning:: Quando si utilizza l'esportazione dei dati basata su filesystem, il file io\_catalogo non deve essere esistere.

Un stesso file può essere presente più volte però ovviamente in cartelle
differenti. I nomi delle cartelle si visualizzeranno anche nel
dispositivo. I nomi dei file devono seguire le regole di nomenclatura
descritte di seguito:

Nomenclatura di file e cartelle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Per collegare i files agli articoli, e poter aprire il form dell' ordine
toccando l' immagine, non potendo utizzare (in questa modalità) un
tracciato che descive il contenuto della cartella, l'unico modo è quello
di riportare il codice articolo nella descrizione del file.

I nomi dei file e delle cartelle, devono soddisfare quindi le seguenti
regole:

::

    nome[CodiceArticolo]{ordinamento}.estensione

Questo vuol dire che è possibile specificare un nome al file e
associarlo ad un articolo mettendo il rispettivo codice tra parentesi
quadre. E' possibile specificare inoltre un eventuale ordinamento tra i
file mettendo un numero tra parentesi graffe.

Esempi:

+-----------------------------+
| Nome file                   |
+=============================+
| Listino.pdf                 |
+-----------------------------+
| Libreria Kwaba [kw07].jpg   |
+-----------------------------+
| Foresta {1}.png             |
+-----------------------------+
| Depliant [0567] {2}.avi     |
+-----------------------------+
| 123[123].jpg                |
+-----------------------------+

Tipi di file supportati
-----------------------

I files supportati dal modulo catalogo sono:

* Immagini
* Video


.. note::

    Alcuni codec (es.xvid, divx), non sono nativamente supportati su iOs


Dimensione delle immagini
-------------------------

Tenendo in considerazione che le immagini devono essere visualizzate nei
dispositivi mobile, occorre prestare attenzione anche alla dimensione
delle immagini stesse.

Una dimensione molto elevata implica una mole maggiore di dati da
spostare (quindi maggiore lentezza nella sincronizzazione).

Nei dispositivi (es. ipad) una dimensione in pixel maggiore della
risoluzione gestita dal dispositivo farà si che l'immagine venga
adattata automaticamente ridimensionandola perdendo qualche dettaglio
(che verrà recuperato effettuando lo zoom). Nel caso in cui invece la
dimensione in pixel della foto risulti inferiore alla risoluzione
gestita dal dispositivo, l'immagina viene lasciata invariata e quindi
non si vedrà a schermo intero.

In fase di importazione del catalogo, dentro l'appmanager viene eseguito
un ridimensionamento delle immagini che superano una determinata
dimensione, esso si può modificare a piacimento entrando in appmanager e
andando sul progetto (campo Max Pixel Foto).

Il default di tale parametro è 1028 (risoluzione ipad 2) ma è possibile
cambiarlo ad esempio a 2048 (dimensione ipad retina, air, etc.).

Ogni immagine con larghezza o altezza massima superiore a questo valore
verrà ridimensionata in base al valore del parametro.

Anteprime cartelle
------------------

Le anteprime delle cartelle che contengono le immagini, vengono
visualizzate secondo criteri casuali.
Viene cioè mostrata una immagine a caso fra quelle contenute
all' interno della cartella.
