:tocdepth: 2

.. highlight:: none

.. metadata-placeholder

   :DC.Title:
   	Using Graphics and Diagrams in Sphinx
   :DC.Creator:
   	Nery, Fernanda
   :DC.Date:
   	2013-10-01
   :DC.Description:
      Overview of some available alternatives for
      producing and including SVG graphics and UML diagrams in Sphinx.
   :DC.Language:
   	en
   :DC.Format:
   	text/x-rst


Creating diagrams in Sphinx
***************************

Using Graphviz
==============

除了使用图片(PNG,JPG,etc.)之外,例图也可以使用 ``sphinx.ext.graphviz`` 扩展.

``GraphViz`` 是一个开源的图形可视化软件.可视化图形是一种把结构化信息作为抽象图和网络图的表示方式之一.

使用这个扩展之前必须要安装该软件.

Requires
--------------

Graphviz 扩展 默认包括在Sphinx中, 但是这个扩展必须要在 ``conf.py`` 文件中开启::

   extensions = ['sphinx.ext.graphviz']

Examples
--------

code:

.. literalinclude:: diagrams.rst
   :lines: 51-55

output:

.. graphviz::

   digraph {
      "From" -> "To";
   }

code:

.. literalinclude:: diagrams.rst
   :lines: 64-77
   
output:

.. graphviz::

   digraph Flatland {
   
      a -> b -> c -> g; 
      a  [shape=polygon,sides=4]
      b  [shape=polygon,sides=5]
      c  [shape=polygon,sides=6]
   
      g [peripheries=3,color=yellow];
      s [shape=invtriangle,peripheries=1,color=red,style=filled];
      w  [shape=triangle,peripheries=1,color=blue,style=filled];
      
      }

大量在线的例子可以从如下网站获得:

*  https://en.wikipedia.org/wiki/DOT_(graph_description_language)
*  http://www.graphviz.org/pdf/dotguide.pdf
*  http://graphs.grevian.org/example.html

Using PlantUML
==============

``Sphinx PlantUML extension`` 允许Sphinx通过使用PlantUML来画UML图例.

``PlantUML``  是一个允许快速画简单UML图例的java组件:

*  case diagrams,
*  class diagrams,
*  activity diagrams,
*  state diagrams,
*  component diagrams,
*  sequence diagrams,
*  object diagram.

Installing the extension
------------------------

安装插件::
   
   pip install sphinxcontrib-plantuml

安装Plantuml jar包.


开启插件::

   #编辑 conf.py文件
   extensions = ['sphinxcontrib.plantuml']
   plantuml = 'java -jar  全路径/plantum.jar'

.. note:: 

    是否需要安装Graphviz

.. warning:: 限制是非常大的,若是作为在线使用，由于需要安装plantum.jar 所以在线使用不了.可以线下把图例生成好，作为图像使用.

Examples
--------

code:

.. begin-plantuml-first-example

.. uml:: 
   
   @startuml
   user -> (use PlantUML)

   note left of user
      Hello!   
   end note
   @enduml

.. end-plantuml-first-example

output:

.. literalinclude:: diagrams.rst
   :language: rst
   :start-after: begin-plantuml-first-example
   :end-before: end-plantuml-first-example


Another code:

.. begin-plantuml-second-example

.. uml::
   
   @startuml 
   Alice -> Bob: Hi!
   Alice <- Bob: How are you?
   @enduml

.. end-plantuml-second-example

output:

.. literalinclude:: diagrams.rst
   :language: rst
   :start-after: begin-plantuml-second-example
   :end-before: end-plantuml-second-example


其它的例子参阅:

* https://build-me-the-docs-please.readthedocs.io/en/latest

.. links-placeholder
