超链接
##################

External links
*****************

inline
===================

code:

.. code-block:: rst

    This is a `inline links <http://example.com/>`_

output:

This is a `inline links <http://example.com/>`_

separate
===================

example 1
------------------
code:

.. code-block:: rst

    This is a paragraph that contains `a link`_.

    .. _a link: http://example.com/

output:

This is a paragraph that contains `a link`_.

.. _a link: http://example.com/

example 2
----------------------

code:

.. code-block:: rst

    This is a paragraph that contains word_.

    .. _word: http://example.com/

output:

This is a paragraph that contains word_.

.. _word: http://example.com/

.. admonition:: This is a tip.

   The use of inline web links is discouraged, 
   to improve the readability of the reST text.
   
   Simple links (e.g. to institutional sites, software sites, and so on)
   should be kept together at the end of the text file 
   (this is merely a way to simplify the editing procedure, 
   and the update and verification of the links).
   
Internal links
********************

为了在文档中任意位置使用交叉引用,这个标签名(label names)在文档中必须是独一无二的.这里有两种方式可以引用标签名(label names).

example 1
==============

code:

.. code-block:: rst 

    .. _example: 
    
    This is an example crossreference target.

    Internal crossreferences, like example_. 

output:

.. _example:

This is an example crossreference target.

Internal crossreferences, like example_.


example 2
======================

code:

.. code-block:: rst

    .. _rst-figures-ref:

    This is the text of the section.

    This is an example crossreference target. :ref:`figures <rst-figures-ref>`

output:

.. _rst-figures-ref:

This is the text of the section.

This is an example crossreference target. :ref:`figures <rst-figures-ref>`