=============
目录
=============

局部目录
============
局部目录指的是从当前文档中的相关标题来构建一个目录.采用 ``contents`` 指令现给出一个从当前标题下的一个2级目录:

.. code-block:: rst

    .. contents:

        :depth: 2
        :local:

output:

.. contents::
   :depth: 2
   :local:

大标题一
----------

小标题一
++++++++++

大标题二
----------

小标题二
+++++++++

.. note:: 指令 ``contents`` 详细内容 `参阅 <docutils.sourceforge.net/docs/ref/rst/directives.html>`_

全局目录
===========
全局目录指的是从其它文档中的相关标题来构建一个目录. 采用 ``toctree`` 指令现给出一个从其它文档导入的一个2级目录:

参数详解:

.. code-block:: text

    :maxdepth:2             设置最大深度
    :numbered:              自动编号 
    :name:                  名字
    :titlesonly:            只显示标题
    :glob:                  通配符，这样写文件条目简单写
    :reversed:              反向编号
    :hidden:                隐藏

code:

.. code-block:: rst

    .. toctree::
        :maxdepth:2
        :numbered:
        
        diagrams
        math 

output:

.. toctree::
    :maxdepth:2

    diagrams
    math 

.. note:: 指令 ``toctree`` 详细内容 `参阅toctree <https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html?highlight=toctree>`_
