LaTeX
=====

.. code-block:: python

   # Seskupení dokumentace do "knih". Seznam n-tic
   # (počáteční zdroj, název souboru tex, titul,
   #  autor, documentclass [howto, manual, nebo jiná]).
   ### Lze použít i třídy z LaTeX distribuce, např. book nebo article
   latex_documents = [
       ('ZakladySphinx/index', 'Sphinx1-Zaklady.tex', 'Sphinx - Základy',
         author, 'manual'),
       ('Syntaxe/index', 'Sphinx2-Syntaxe.tex', 'Sphinx - Syntaxe',
         author, 'manual'),
       ('Rozsireni/index', 'Sphinx3-Rozsireni.tex', 'Sphinx - Rozšíření',
         author, 'manual'),
   ]

Tabulky
-------

.. code-block:: rst

   .. tabular-columns:: ...

:sphinx:`usage/restructuredtext/directives.html#directive-tabularcolumns`
