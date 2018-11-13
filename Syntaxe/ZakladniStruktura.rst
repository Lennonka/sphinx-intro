Základní struktura
==================

Každý zdrojový soubor musí mít hlavní nadpis.

Nadpisy
-------

Nadpisy definují strukturu dokumentu čili jeho členění na menší oddíly
jako jsou kapitoly, sekce a podsekce.

Nadpis musí být podtržen jedním z přípustných znaků alespoň v takové délce,
jakou má text nadpisu.

.. code-block:: none
   :caption: Znaky přípustné pro podtržení nadpisů (doporučená podmnožina)

   = - ` : ' " ~ ^ _ * + # < >

Kde začíná nadpis oddílu určité úrovně, tam končí předchozí oddíl též úrovně.
Úrovně oddílů jsou odlišeny podtržením nadpisů.

.. code-block:: rest
   :caption: Ilustrace jednoduchého dokumentu

   =====
   Titul
   =====

   --------
   Podtitul
   --------

   Název kapitoly
   ==============

   Blok+

   Název sekce
   -----------

   Blok+

   Podsekce
   ^^^^^^^^

   Blok+

   Další podsekce
   ^^^^^^^^^^^^^^

   Blok+

   Další sekce
   -----------

   Blok+

Je vhodné zavést si konvenci pro jednotné použití znaků pro jednotlivé
úrovně nadpisů.

Tělo oddílu je tvořeno buď dalšími oddíly nebo :doc:`bloky <Bloky>`.
