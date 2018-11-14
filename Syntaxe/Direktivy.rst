Direktivy
=========

.. code-block:: rest
   :caption: Obecná syntaxe direktivy

   .. nazev:: [argumenty...]
      [:volba:]
      [:volba2: hodnota]

      tělo direktivy

      i víceblokové tělo

Složitější struktura -- osnova (S)
----------------------------------

Propojení více souborů do jednoho celku zajišťuje direktiva :code:`toctree`.

.. code-block:: rst

   .. toctree::
      :caption: Obsah
      :maxdepth: 2
      :numbered:
      :glob:

      UvodniKapitola
      SlozenaKapitola/index
      DalsiKapitola/index
      Moduly/*

Na místě, kde je uvedena direktiva, bude vygenerovaný obsah až do hloubky
podnadpisů definovaný volbou ``maxdepth``. Pokud není uvedena, budou zahrnuty
všechny úrovně.

Obrázky (r)
-----------

image / figure

.. _dir-kotva:

Kotva
-----

Kotva umožňuje použití :ref:`explicitní reference <role-ref>` na libovolný
oddíl nebo blokový prvek, který je kotvou označen.

Kotva funguje jako identifikátor oddílu nebo bloku napříč celým projektem,
tudíž musí být v rámci projektu unikátní.

Kotvu lze použít na jakýkoli blok vč. jednoduchého odstavce.

.. code-block:: rst

   .. _identifikator-kotvy:

   <blok nebo nadpis>



.. _dir-zdrojaky:

Ukázka kódu (r/S)
-----------------

.. code-block:: Python

   print("Hello World!")

.. code-block:: rst

   .. code-block:: Python

      print("Hello World!)

.. _dir-tabulky:

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

.. index::
   pair: index; entry

Tvorba rejstříku (S)
--------------------

Odkaz z rejstříku na oddíl nebo blok:

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

Include (r)
-----------

Vložení obsahu z jiného souboru
