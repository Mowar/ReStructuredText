============
code-file
============

有些时候需要显示的代码来自某个文件或者某个url,以及显示出两个文件的差异

引用一个文件
==================================

.. literalinclude:: ../_static/test.py
   :encoding: utf-8
   :language: python
   :emphasize-lines: 1,3-4
   :linenos:
   :lines: 1,4-

diff2个文件
========================================

.. literalinclude:: ../_static/test.py
   :diff: ../_static/test2.py
