Role
====

.. code-block:: rest

   :nazev:`interpretovaný text`



Kompletní reference rST rolí viz :rstrole:`contents`.

.. _role-ref:

Explicitní reference
--------------------

Pomocí explicitní reference se lze odkázat na kterýkoli oddíl nebo blok
s :ref:`kotvou <dir-kotva>` v kterémkoli souboru v rámci projektu (globálně).

V případě odkazů na bloky, které nemají titulek, je potřeba v referenci uvést
popisek.

.. code-block:: rst

   .. vlastní popisek

   :ref:`popisek <identifikator-kotvy>`

   .. nebo automatický popisek z titulku bloku

   :ref:`identifikator-kotvy`

Pokud má blok titulek, doplní se automaticky na místo popisku.

Např. viz také :ref:`dir-kotva` (automatický popisek)
nebo :ref:`definice kotvy <dir-kotva>` (vlastní popisek).

.. _role-doc:

Reference na dokument
----------------------

Pomocí této reference se lze odkázat na kterýkoli zdrojový dokument v rámci
projektu.

.. code-block:: rst

   .. vlastní popisek

   :doc:`popisek </Cesta/k/dokumentu>`

   .. nebo automatický popisek

   :doc:`/Cesta/k/dokumentu`

Pokud neuvedeme popisek, doplní se automaticky na místo popisku hlavní nadpis,
případně titul dokumentu.

Např. :doc:`/Syntaxe/ZdrojoveSoubory`

Sémantické role
---------------

:abbr:`LIFO (last-in, first-out)`

... is installed in :file:`/usr/lib/python2.{x}/site-packages` ...

:guilabel:`Odeslat`

:menuselection:`Menu --> Submenu --> Item`

Viz :sphinx:`Sphinx Doc: Other semantic markup
<usage/restructuredtext/roles.html#other-semantic-markup>`

Definice vlastních rolí
-----------------------

Rozpozná volbu class

:rstdir:`role`
