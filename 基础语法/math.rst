===============
数学公式
===============

其中能够支持行内公式(inline formula)和公式块(math block),所采用的数学符号是Latex符号的部分子集

行内公式
===============

code::

    The area of a circle is :math:`A_\text{c} = (\pi/4) d^2`.

output:

The area of a circle is :math:`A_\text{c} = (\pi/4) d^2`.


公式块
===============

单行公式
--------------

code:

.. code-block:: rst

     .. math:: α_t(i) = P(O_1, O_2, … O_t, q_t = S_i λ)

output:

.. math:: α_t(i) = P(O_1, O_2, … O_t, q_t = S_i λ)


公式组
----------------

code:

.. code-block:: rst

    .. math::
        :label:

        (a + b)^2 = a^2 + 2ab + b^2

        (a - b)^2 = a^2 - 2ab + b^2

        (a + b)^2  &=  (a + b)(a + b) \\
               &=  a^2 + 2ab + b^2

output:

.. math::
    :label: 

    (a + b)^2 = a^2 + 2ab + b^2

    (a - b)^2 = a^2 - 2ab + b^2

    (a + b)^2  &=  (a + b)(a + b) \\
               &=  a^2 + 2ab + b^2


code:

.. code-block:: rst

    .. math::
       :nowrap:

        \begin{eqnarray}
            y    & = & ax^2 + bx + c \\
            f(x) & = & x^2 + 2xy + y^2
        \end{eqnarray}

output:

.. math::
       :nowrap:

        \begin{eqnarray}
            y    & = & ax^2 + bx + c \\
            f(x) & = & x^2 + 2xy + y^2
        \end{eqnarray}

.. note:: 
    
    :nowrap: 防止在数学环境中包装给定的数学

.. note:: 
    
    :label: 产生数字标号并可以交叉引用