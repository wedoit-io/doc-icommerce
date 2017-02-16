Cataloghi agente
================

E' possibile configurare iCommerce per mostrare solo un predefinito insieme
di articoli per uno specifico agente.
Per fare questo occorre utilizzare la gestione dei ``cataloghi per agente``,
che si attiva automaticamente creando i seguenti tracciati:

=========================  ============================================
Nome tracciato             Descrizione                 
=========================  ============================================
io_cataloghi.dat           Anagrafica dei cataloghi
io_cataloghi_agente.dat    Associazione agenti per catalogo
io_cataloghi_art.dat       Associazione degli articoli al catalogo
=========================  ============================================

L'applicazione determina quali articoli un agente può vedere, attraverso
l'associazione di 2 entità associative (io_cataloghi_art.dat e io_cataloghi_agente.dat).

In pratica:

- Un set di prodotti deve essere associato ad uno o più cataloghi
- Un set di cataloghi deve essere associato a uno o più agenti

Dopo aver creato questa associazione, i dati scaricati dall'agente sull'iPad verranno filtrati
in modo che un agente potrà veder solo gli articoli associati ai cataloghi che afferiscono a lui.

.. _io_cataloghi.dat: https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi.cs
.. _io_cataloghi_art.dat: https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi_art.cs
.. _io_cataloghi_agente.dat: https://github.com/wedoit-io/AMHelper/blob/master/src/net20/AMHelper/CSV/imp/rec_cataloghi_agente.cs
