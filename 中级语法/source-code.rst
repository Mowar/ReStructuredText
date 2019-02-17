source-code
#############

Inline markup
**************

code:

.. code-block:: rst
    
    This is a normal text paragraph. The next paragraph is a code sample::

        It is not processed in any way, except
        that the indentation is removed.

        It can span multiple lines.

    This is a normal text paragraph again.

output:

This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.


Explicit Markup
*****************

code-block directive
======================

code:

.. code-block:: rst

    .. code-block:: sql
        :linenos:

        SELECT * FROM mytable

output:

.. code-block:: sql
   :linenos:

   SELECT * FROM mytable

Literalinclude directive
==========================

Another option is to include part of a given source code file.

.. code-block:: rst

    .. literalinclude:: filename
        :linenos:
        :language:
        :lines:
        :start-after:
        :end-before:
        :diff:
        :emphasize-lines:

code:

.. code-block:: rst

    .. Insted of using

    use the options ``:start-after`` and ``:end-before:``
    that search the included file for lines containing the specified text.

    .. For example

    .. literalinclude:: source-code.rst
        :language: rst
        :start-after: Instead of using
        :end-before: For example

output:

.. start_first_literalinclude

    use the options ``:start-after`` and ``:end-before:``
    that search the included file for lines containing the specified text.

.. end_first_literalinclude

.. literalinclude:: source-code.rst
    :language: rst
    :start-after: start_first_literalinclude
    :end-before: end_first_literalinclude


code:

.. code-block:: rst

    .. literalinclude:: ../_static/test.py
        :diff: ../_static/test2.py

output:

.. literalinclude:: ../_static/test.py
   :diff: ../_static/test2.py

Highlight directive
========================

.. note::

    其支持的语言有python、bash、json、ruby等. 详情 `参阅 <https://build-me-the-docs-please.readthedocs.io/en/latest/Using_Sphinx/ShowingCodeExamplesInSphinx.html>`_

.. note:: 我们可以在配置文件指定highlight_langeuage="c,python"