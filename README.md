# iCommerce doc source

Questo repository contiene il sorgente della documentazione tecnica pubblicata su http://www.readthedocs.org.

La documentazione è scritta in reStructured text, un linguaggio simile al markdown ma creato specificatamente per generare documentazione.

E' un po più ostico, ma la maggior parte dei tag usati sono identici a quelli del markdown.

Readthedocs è un servizio di hosting utilizza un generatore di documentazione statica chiamato sphinx.

Ogni modifica effettuata sui files (che hanno estensione .rst) fa scattare un webhook verso readthedocs.
Quest'ultimo scarica l'ultima versione pubblicata sul master e la ricompila.

Installazione sphinx in locale
====
E' possibile installare sphinx in locale e generare la documentazione nel proprio computer.
Per farlo basta installare sphinx con la seguente sintassi:

    pip install sphinx sphinx-autobuild sphinx-autobuild

Compilare la documentazione
===

Clonare il repo in locale

    git clone https://github.com/wedoit-io/ic.wedoit.io
    
Andare nella cartella ic.wedoit.io ed eseguire il make

    make html
    

Attivare refresh automatico del sito
=====================================
Per fare in modo che il sito si autoaggiorni senza dove rieseguire make html quando cambiano i sorgenti, operare come segue:

Installare sphinx-autobuild

	pip install sphinx-autobuild

Aprire il file Makefile e in cima aggiungere:

	SPHINXAUTOBUILD = sphinx-autobuild

Nella parte sotto html aggiungere:

	.PHONY: livehtml
	livehtml:
		$(SPHINXAUTOBUILD) -b html $(ALLSPHINXOPTS) $(BUILDDIR)/html
		@echo
		@echo "Autobuild finished. The HTML pages are in $(BUILDDIR)/html."

A questo punto basta eseguire:

	make livehtml


Riferimenti
===
* Sphinx: http://www.sphinx-doc.org/
* ReadTheDocs: http://docs.readthedocs.io/en/latest/getting_started.html
