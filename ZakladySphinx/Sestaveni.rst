.. index:: builder

Sestavení (build)
=================

Na sestavení výstupních formátů se používá program :program:`sphinx-build`,
kterému se předá vstupní a výstupní adresář, typ *builder*\ u a případně další
argumenty.

Obvykle se ale nespouští přímo, nýbrž přes :program:`make`, kterému se zadá jen
typ *builder*\ u a build je dále řízen přes :file:`Makefile` [#bat]_.
Tím se příkaz buildu zkrátí na následující:

.. code-block:: shell
   :caption: Příklady spuštění buildu

   # Sestavení vícestránkového HTML
   make html
   # Sestavení LaTeXu a následné automatické spuštění pdflatex
   make latexpdf

Typy *builder*\ ů si můžete vypsat příkazem :code:`make help`.

.. [#bat] Na Windows je toto chování simulováno dávkovým souborem
   :program:`make.bat`.

.. todo:: příklady argumentů pro buildery, případně rozepsat