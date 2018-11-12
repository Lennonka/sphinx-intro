.. index:: quickstart

Vytvoření projektu
==================

Na inicializaci nového projektu použijte program :program:`sphinx-quickstart`:

.. code-block:: shell

   sphinx-quickstart

Program se interaktivně ptá na různé volby, na které odpovíte.

.. todo:: popsat volby

Nakonec v adresáři vytvoří základní soubory:

* hlavní dokument (*master document*) s obsahem
  (:rst:role:`toctree`), např. :file:`index.rst`,
* konfigurační soubor :file:`conf.py` přizpůsobený podle vašich voleb,
* soubor :file:`Makefile` a/nebo :file:`make.bat` pro spouštění buildů.
