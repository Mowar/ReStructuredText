============
Comments
============

每个非有效的显示标记都会被作为注释.

单行注释
------------

code:

.. code-block:: rst

    .. This is a comment.

.. This is a comment.

多行注释
---------------------

方法一
++++++++++

code:

.. code-block:: rst

    ..
      This whole indented block
      is a comment.

      Still in the comment.

..
    This whole indented block
    is a comment.

    Still in the comment.

方法二
+++++++++++++

code:

.. code-block:: rst

    .. begin-plantuml-first-example

        .. uml:: 
        
        @startuml
        user -> (use PlantUML)

        note left of user
            Hello!   
        end note
        @enduml

    .. end-plantuml-first-example

.. begin-plantuml-first-example

.. uml:: 
   
   @startuml
   user -> (use PlantUML)

   note left of user
      Hello!   
   end note
   @enduml

.. end-plantuml-first-example

.. admonition:: 惯例.

   Comments 可以在文档中作为占位符标记当前的位置.For example:

   *   ``.. links-placeholder`` 放置在文档末尾的超链接;
      
   *  ``.. metadata-placeholder`` 放置在文档开始的文档元数据(作者,日期等)