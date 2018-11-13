Direktivy
=========

.. code-block:: rest
   :caption: Obecná syntaxe

   .. nazev:: [argumenty...]
      [:volba:]
      [:volba2: hodnota]

      tělo direktivy

      i víceblokové tělo

Obsahový strom / osnova (S)
---------------------------

.. code-block:: rst

   .. toctree:: Obsah

      :numbered:

      UvodniKapitola
      SlozenaKapitola/index
      DalsiKapitola/index
      Moduly/*

.. _dir-zdrojaky:

Ukázka kódu (r/S)
-----------------

.. code-block:: Python

   print("Hello World!")

.. code-block:: rst

   .. code-block:: Python

      print("Hello World!)

Zjednodušené tabulky (r)
------------------------

Podrobně viz :rstref:`tables`

.. rubric:: CSV table

.. csv-table:: Popisek tabulky
   :header: "Jméno", "Věk", "Komentář"
   :widths: 15, 10, 30

   "Pepa Nový", 26, "Je to v pohodě"
   "Gandalf Šedý", 213, "Neprojdeš!"
   "John Lennon", 78, "Imagine there's no heaven.
   It's easy if you try..."

.. rubric:: List table

.. list-table:: Popisek tabulky
   :header-rows: 1
   :widths: 15, 10, 30

   * - Jméno
     - Věk
     - Komentář
   * - Pepa Nový
     - 26
     - Je to v pohodě
   * - Gandalf Šedý
     - 213
     - Neprojdeš!
   * - John Lennon
     - 78
     - Imagine there's no heaven.
       It's easy if you try...

Slovník pojmů (glosář) (r)
--------------------------

.. code-block:: rst

   .. glossary::

      pojem 1
      pojem 2
         Definice obou pojmů.

      pojem 3
         Definice pojmu 3.

         Definice pokračuje dalším odstavcem.

V textu se pak můžeme odkazát na definici pojmu pomocí role :rst:role:`term`
a Sphinx do výstupu vygeneruje křížový odkaz do slovníku pojmů, např.
``:term:`slovník``` -> :term:`slovník`.

Tvorba rejstříku (S)
--------------------

Odkaz z rejstříku na blok:

.. code-block:: rst

   .. index::
      pair: index; entry

   Nadpis
   ------

Odkaz z rejstříku na řádek:

.. code-block:: rst

   This is a normal reST :index:`paragraph` that contains several
   :index:`index entries <pair: index; entry>`.

Substituce (r)
--------------

Podrobně viz :rstdir:`directives-for-substitution-definitions`

.. code-block:: rst

   .. jednoduché nahrazení

   .. |rST| replace:: reStructuredText

   .. surový výstup

   .. |br| raw:: html

      <br/>

   .. |lbr| raw:: latex

      \\

Obrázky (r)
-----------

image / figure


Include (r)
-----------

Vložení obsahu z jiného souboru
