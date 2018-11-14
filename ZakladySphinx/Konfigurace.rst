Konfigurace
===========

Soubor :file:`conf.py` obsahuje většinu nastavení, která ovlivňují zpracování
vstupů a výstupů. Jak napovídá jeho koncovka, je psán v syntaxi Pythonu,
a je Sphinxem spouštěn na začátku buildu (přes funkci :code:`execfile()`).
Jeho syntaxí se tady ale zabývat nebudeme, protože přesahuje rámec této
publikace, viz např. `Python Tutorial <https://docs.python.org/3/tutorial/>`_.

.. rubric:: Poznámka k Python 2

Pokud v konfiguračním souboru :file:`conf.py` pracujete s řetězci, které
obsahují ne-ASCII znaky (obvykle znaky s diakritikou), musíte tyto řetězce
označit jako unicode řetězce, např.: ``u'Příliš žluťoučký kůň...'``.

---------------

Pro podrobnou referenci konfigurace viz :sphinx:`usage/configuration.html`.

Zde si ukážeme jen, jak jsou organizovány sekce konfiguračního souboru
a pár kouzel s Pythonem.

Sekce
-----

.. rubric:: Path setup

Nastavení cest k rozšířením, dokumentovaným modulům, případně motivům
(HTML theme), a importy knihoven Pythonu.

.. rubric:: Project information

Základní informace o projektu, např. titul, verze, jméno autora, znění
copyrightu.

.. rubric:: General configuration

Základní konfigurace Sphinxu. Část těchto hodnot je vyplněna pomocí skriptu
:program:`sphinx-quickstart`, např. jazyk, rozšíření, koncovky zdrojových
souborů nebo název kořenového souboru.

.. rubric:: Options for HTML output

Volby výstupu do HTML jako motiv a jeho nastavení, titul, logo, favikona,
vlastní styly, nastavení vyhledávače, předání dalších parametrů šablonovacímu
systému (kontext) a mnoho dalších.

.. rubric:: Options for LaTeX output

Volby výstupu do LaTeXu, např. úroveň nadpisů, logo na titulní straně,
zobrazení hypertextových odkazů, čísla stránek místo křížových odkazů,
typografická nastavení jako formát stránky nebo základní velikost písma.



Kouzla s Pythonem
-----------------

.. rubric:: Titul s aktuální verzí

.. code-block:: python

   # -- Project information ---------------------------------------------------
   project = 'Úvod do Sphinxu'
   # The short X.Y version
   version = '0.1'
   # ...
   # -- Options for HTML output -----------------------------------------------
   # Title
   html_title = project + ' v' + version
   # ...

.. rubric:: Aktuální rok v copyrightu

.. code-block:: python

   import time

   copyright = u'2016–{}, CZ.NIC, z.s.p.o.'.format(time.localtime().tm_year)

.. rubric:: Název větve Gitu

.. code-block:: python

   import os

   # Git
   if 'GIT_BRANCH' in os.environ:
       git_branch = os.environ['GIT_BRANCH']
   else:
       git_branch = 'neznámá'

   # Substitutions
   rst_prolog = """
   .. |branch| replace:: {}
   """.format(git_branch)
