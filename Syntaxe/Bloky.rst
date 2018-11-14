Blokové prvky
=============

Podíváme se na několik základních implicitních blokových prvků jazyka rST.

Více viz `rST Markup Specification - Body Elements
<http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html>`_.

Odstavce
--------

Odstavec.

Další odstavec.
Odstavce nezachovávají zalomení řádků.

Odstavce mohou obsahovat :doc:`řádkové prvky <Inline>`.

Citáty
------

   Bloková citát. (~ odsazený odstavec)

   Chceme-li pokračovat v citátu dalším odstavcem,
   musíme jej odsadit stejně.

Blokové literály
----------------

.. sidebar:: Blokový literál

   Za tímto odstavcem bude následovat literál::

      tělo literálu

   ::

      samostatný literál

.. code-block:: rst

   Za tímto odstavcem bude následovat literál::

      tělo literálu

   ::

      samostatný literál

Viz také :ref:`direktivy pro zdrojový kód <dir-zdrojaky>`.

..
   Line bloky
   ----------

   | Blokový prvek,
   | který
     zachovává
   | zalomení řádků.
   |
   | Skvělý
   | pro psaní
   | poezie.

Seznamy
-------

Výčty nějakých logických celků.

Položky seznamu mohou obsahovat další blokové prvky.

Nečíslované seznamy
*******************

.. code-block:: none
   :caption: Znaky přípustné pro označení položek nečíslovaného seznamu

   * + - • ‣ ⁃

.. sidebar:: Nečíslovaný seznam

   - A bullet list

     + Nested bullet list.
     + Nested item 2.

   - Item 2.

     Paragraph 2 of item 2.

     * Nested bullet list.
     * Nested item 2.

       - Third level.
       - Item 2.

     * Nested item 3.


.. code-block:: rst

   - A bullet list

     + Nested bullet list.
     + Nested item 2.

   - Item 2.

     Paragraph 2 of item 2.

     * Nested bullet list.
     * Nested item 2.

       - Third level.
       - Item 2.

     * Nested item 3.

Více o :rstref:`nečíslovaném seznamu <bullet-lists>`.


Číslované seznamy
*******************

.. sidebar:: Číslovaný seznam

   1. Arabic numerals.

      a) lower alpha)

         (i) (lower roman)

             A. upper alpha.

                I) upper roman)

   2. Lists that don't start at 1:

      3. Three

      4. Four

      C. C

      D. D

      iii. iii

      iv. iv

   #. List items may also be auto-enumerated.

.. code-block:: rst

   1. Arabic numerals.

      a) lower alpha)

         (i) (lower roman)

             A. upper alpha.

                I) upper roman)

   2. Lists that don't start at 1:

      3. Three

      4. Four

      C. C

      D. D

      iii. iii

      iv. iv

   #. List items may also be auto-enumerated.

Více o :rstref:`číslovaném seznamu <enumerated-lists>`.



Volby programu (option list)
----------------------------

Seznam voleb programu jako v nápovědě vypsané programem.

.. sidebar:: Programové volby

   -a         Output all.
   -b         Output both (this description is
              quite long).
   -c arg     Output just arg.
   --long     Output all day long.

   -p         This option has two paragraphs in the description.
              This is the first.

              This is the second.  Blank lines may be omitted between
              options (as above) or left in (as here and below).

   --very-long-option  A VMS-style option.  Note the adjustment for
                       the required two spaces.

   --an-even-longer-option
              The description can also start on the next line.

   -2, --two  This option has two variants.

   -f FILE, --file=FILE  These two options are synonyms; both have
                         arguments.

   /V         A VMS/DOS-style option.

.. code-block:: rst

   -a         Output all.
   -b         Output both (this description is
              quite long).
   -c arg     Output just arg.
   --long     Output all day long.

   -p         This option has two paragraphs in the description.
              This is the first.

              This is the second.  Blank lines may be omitted between
              options (as above) or left in (as here and below).

   --very-long-option  A VMS-style option.  Note the adjustment for
                       the required two spaces.

   --an-even-longer-option
              The description can also start on the next line.

   -2, --two  This option has two variants.

   -f FILE, --file=FILE  These two options are synonyms; both have
                         arguments.

   /V         A VMS/DOS-style option.

Více o :rstref:`seznamu programových voleb <option-lists>`.

Tabulky
-------

Různé syntaxe:

* :rstref:`grid tables <grid-tables>`,
* :rstref:`simple tables <simple-tables>`,
* použití direktiv (csv table, list table) -- viz :ref:`dir-tabulky`

Bibliografické prvky
--------------------

.. 
   sidebar:: Definice

   Term
       Definition
   Term
       Definition paragraph 1.

       Definition paragraph 2.
   Term
       Definition

.. code-block:: rst
   :caption: Definice

   Term
       Definition
   Term
       Definition paragraph 1.

       Definition paragraph 2.
   Term
       Definition

..
   sidebar:: Citace

   .. [CIT2002] Citations are text-labeled footnotes. They may be
      rendered separately and differently from footnotes.

   Here's a reference to the above, [CIT2002]_, and a [nonexistent]_
   citation.

.. code-block:: rst
   :caption: Citace

   .. [CIT2002] Citations are text-labeled footnotes. They may be
      rendered separately and differently from footnotes.

   Here's a reference to the above, [CIT2002]_, and a [nonexistent]_
   citation.


..
   sidebar:: Poznámky pod čarou

   .. [1] A footnote contains body elements, consistently indented by at
      least 3 spaces.

      This is the footnote's second paragraph.

   .. [#label] Footnotes may be numbered, either manually (as in [1]_) or
      automatically using a "#"-prefixed label.  This footnote has a
      label so it can be referred to from multiple places, both as a
      footnote reference ([#label]_) and as a hyperlink reference
      (label_).

   .. [#] This footnote is numbered automatically and anonymously using a
      label of "#" only.

   .. [*] Footnotes may also use symbols, specified with a "*" label.
      Here's a reference to the next footnote: [*]_.

   .. [*] This footnote shows the next symbol in the sequence.

   .. [4] Here's an unreferenced footnote, with a reference to a
      nonexistent footnote: [5]_.

.. code-block:: rst
   :caption: Poznámky pod čarou

   .. [1] A footnote contains body elements, consistently indented by at
      least 3 spaces.

      This is the footnote's second paragraph.

   .. [#label] Footnotes may be numbered, either manually (as in [1]_) or
      automatically using a "#"-prefixed label.  This footnote has a
      label so it can be referred to from multiple places, both as a
      footnote reference ([#label]_) and as a hyperlink reference
      (label_).

   .. [#] This footnote is numbered automatically and anonymously using a
      label of "#" only.

   .. [*] Footnotes may also use symbols, specified with a "*" label.
      Here's a reference to the next footnote: [*]_.

   .. [*] This footnote shows the next symbol in the sequence.

   .. [4] Here's an unreferenced footnote, with a reference to a
      nonexistent footnote: [5]_.

..
   sidebar:: Informační pole

   :what: Field lists map field names to field bodies, like database
          records.  They are often part of an extension syntax.  They are
          an unambiguous variant of :rfc:`2822` fields.

.. code-block:: rst
   :caption: Informační pole

   :what: Field lists map field names to field bodies, like database
          records.  They are often part of an extension syntax.  They are
          an unambiguous variant of :rfc:`2822` fields.


Direktivy
---------

Další blokové prvky (např. obsahový strom, obrázky, ukázky kódu)
můžeme definovat pomocí :doc:`direktiv <Direktivy>`.
