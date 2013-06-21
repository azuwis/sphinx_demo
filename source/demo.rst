样例
====

.. contents:: 本节内容
   :local:

标题
----

::

    一级标题
    ========

    二级标题
    --------

    三级标题
    ~~~~~~~~

    四级标题
    ^^^^^^^^

.. NOTE:: 中文占两个字符宽度。标题和标记并不强制要求对齐。

   也可以用以下的形式::

       ====
       标题
       ====

段落
----

段落不需要特殊标记，有缩进的段落生成的结果也会有缩进。

段落用一个空行隔开，换行只会产生一个空格。

源码::

    第一段
    换行

    第二段

        缩进第一段

        缩进第二段

结果:

第一段
换行

第二段

    缩进第一段

    缩进第二段

文字强调
--------

====================================== ==================================
源码                                   结果
====================================== ==================================
``支持对\ *文字*\ 的\ **强调**``       支持对\ *文字*\ 的\ **强调**
``*emphasis* and **strong emphasis**`` *emphasis* and **strong emphasis**
====================================== ==================================

.. NOTE:: 中文问题

   reStructuredText的特殊标记一般需要两侧是空格或者行首末，英文用空格隔开单词，所以不需要作特殊处理。

   而中文则很可能需要两侧添加\ ``\空格``\ 。

图片
----

========================================================= =====================================================
源码                                                      结果
========================================================= =====================================================
``.. image:: images/ball1.gif``                           .. image:: images/ball1.gif
``.. image:: http://www.w3schools.com/images/pulpit.jpg`` .. image:: http://www.w3schools.com/images/pulpit.jpg
========================================================= =====================================================

.. NOTE:: 路径相对于\ `conf.py`\ 所在目录。生成的PDF不支持外链图片。

链接
----

+----------------------------------------------+------------------------------------------+
| 源码                                         | 结果                                     |
+==============================================+==========================================+
| ::                                           |                                          |
|                                              |                                          |
|   http://example.com                         | http://example.com                       |
+----------------------------------------------+------------------------------------------+
| ::                                           |                                          |
|                                              |                                          |
|   This is a `link <http://example.com>`_     | This is a `link <http://example.com>`_   |
+----------------------------------------------+------------------------------------------+
| ::                                           |                                          |
|                                              |                                          |
|   这是一个\ `链接 <http://example.com>`_     | 这是一个\ `链接 <http://example.com>`_   |
+----------------------------------------------+------------------------------------------+
| ::                                           |                                          |
|                                              |                                          |
|   这也是一个\ `链接`_，\ `另一个链接`_       | 这也是一个\ `链接`_，\ `另一个链接`_     |
|                                              |                                          |
|   .. _`链接`: http://example.com             | .. _`链接`: http://example.com           |
|   .. _`另一个链接`: http://example2.com      | .. _`另一个链接`: http://example2.com    |
+----------------------------------------------+------------------------------------------+

.. NOTE::
   当一段文字里有大量超链接时，推荐使用上面表格里最后一种方式。

引用
----

Line-blocks
~~~~~~~~~~~

::

    | line-blocks
    | *line-blocks*

| line-blocks
| *line-blocks*

Literal-blocks
~~~~~~~~~~~~~~

::

    ::

        literal-blocks
        *literal-blocks*

::

    literal-blocks
    *literal-blocks*

脚注(Footnote)
--------------

::

    正文\ [#脚注]_

正文\ [#脚注]_

代码段
------

ruby代码样例
~~~~~~~~~~~~

::

    .. code-block:: ruby

       #!/usr/bin/ruby
       ...

.. code-block:: ruby

   #!/usr/bin/ruby
   class Person
     attr_reader :name, :age
     def initialize(name, age)
       @name, @age = name, age
     end
     def <=>(person) # Comparison operator for sorting
       age <=> person.age
     end
     def to_s
       "#{name} (#{age})"
     end
   end

   # 中文注释
   group = [
     Person.new("Bob", 33),
     Person.new("Chris", 16),
     Person.new("Ash", 23)
   ]

   puts group.sort.reverse

java代码样例
~~~~~~~~~~~~

::

    .. code-block:: java

       // Hello.java
       ...

.. code-block:: java

   // Hello.java
   import java.io.*;
   import javax.servlet.*;

   public class Hello extends GenericServlet {
       public void service(final ServletRequest request, final ServletResponse response)
       throws ServletException, IOException {
           response.setContentType("text/html");
           final PrintWriter pw = response.getWriter();
           try {
               pw.println("Hello, world!");
           } finally {
               pw.close();
           }
       }
   }

.. NOTE:: 有缩进的都会被认为是代码段，可以用\ ``..``\ 显式标明代码结束位置:

   ::

       .. code-block:: java

          // Hello.java
          ...

       ..


列表
----

无序列表
~~~~~~~~

::

    * 第一项

      第一项说明

      * 子项
      * 子项

    * 第二项

          第二项说明(有缩进)

* 第一项

  第一项说明

  * 子项
  * 子项

* 第二项

      第二项说明(有缩进)

有序列表
~~~~~~~~

::

    #. 第一项

       第一项说明

       #. 子项
       #. 子项

    #. 第二项

           第二项说明(有缩进)

#. 第一项

   第一项说明

   #. 子项
   #. 子项

#. 第二项

       第二项说明(有缩进)

表格
----

简单表格
~~~~~~~~

::

    ==== ====
    中文 表格
    ==== ====
    测试 测试
    测试 测试
    ==== ====

==== ====
中文 表格
==== ====
测试 测试
测试 测试
==== ====

网格表格
~~~~~~~~

::

    +------------------------+------------+----------+----------+
    | Header row, column 1   | Header 2   | Header 3 | Header 4 |
    | (header rows optional) |            |          |          |
    +========================+============+==========+==========+
    | body row 1, column 1   | column 2   | column 3 | column 4 |
    +------------------------+------------+----------+----------+
    | body row 2             | Cells may span columns.          |
    +------------------------+------------+---------------------+
    | body row 3             | Cells may  | - Table cells       |
    +------------------------+ span rows. | - contain           |
    | body row 4             |            | - body elements.    |
    +------------------------+------------+---------------------+

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | Cells may span columns.          |
+------------------------+------------+---------------------+
| body row 3             | Cells may  | - Table cells       |
+------------------------+ span rows. | - contain           |
| body row 4             |            | - body elements.    |
+------------------------+------------+---------------------+

.. NOTE:: Vim 的\ `rst-tables <https://github.com/vim-scripts/rst-tables--Chao>`_\ 插件可以辅组表格生成和维护。

   默认主题的表格看起来不大对，是因为下面的CSS样式导致的::

       table.docutils td, table.docutils th {
         border-style: none none solid;
         border-width: 0 0 1px;
       }

列表表格(List-table)
~~~~~~~~~~~~~~~~~~~~

::

    .. list-table:: Frozen Delights!
       :widths: 15 10 30
       :header-rows: 1

       * - Treat
         - Quantity
         - Description
       * - Albatross
         - 2.99
         - On a stick!
       * - Crunchy Frog
         - 1.49
         - If we took the bones out, it wouldn't be
           crunchy, now would it?
       * - Gannet Ripple
         - 1.99
         - On a stick!

.. list-table:: Frozen Delights!
   :widths: 15 10 30
   :header-rows: 1

   * - Treat
     - Quantity
     - Description
   * - Albatross
     - 2.99
     - On a stick!
   * - Crunchy Frog
     - 1.49
     - If we took the bones out, it wouldn't be
       crunchy, now would it?
   * - Gannet Ripple
     - 1.99
     - On a stick!

外部表格
~~~~~~~~

::

    .. csv-table:: 表格描述
       :header: 中文,表格
       :file: table.csv

`table.csv`::

    "测试,测试",测试
    测试,测试

.. csv-table:: 表格描述
   :header: 中文,表格
   :file: table.csv

字段列表(Field lists)
---------------------

::

    :词汇: 解释
    :词汇: 解释

:词汇: 解释
:词汇: 解释

边栏(Sidebar)
-------------

::

    .. sidebar:: 标题
       :subtitle: 副标题

       边栏内容

    正文内容

.. sidebar:: 标题
   :subtitle: 副标题

   边栏内容

正文内容，正文内容，正文内容，正文内容，正文内容，正文内容，正文内容

正文内容

正文内容

正文内容

箴言(Admonitions)
-----------------

::

    .. ATTENTION:: ATTENTION
    .. CAUTION:: CAUTION
    .. DANGER:: DANGER
    .. ERROR:: ERROR
    .. HINT:: HINT
    .. IMPORTANT:: IMPORTANT
    .. NOTE:: NOTE
    .. TIP:: TIP
    .. WARNING:: WARNING
    .. admonition:: 自定义箴言

       箴言内容

.. ATTENTION:: ATTENTION
.. CAUTION:: CAUTION
.. DANGER:: DANGER
.. ERROR:: ERROR
.. HINT:: HINT
.. IMPORTANT:: IMPORTANT
.. NOTE:: NOTE
.. TIP:: TIP
.. WARNING:: WARNING
.. admonition:: 自定义箴言

   箴言内容

替代(Substitution)
------------------

::

    .. |ball| image:: images/ball1.gif

    |ball| |ball|

.. |ball| image:: images/ball1.gif

|ball| |ball|

内嵌HTML
--------

::

    .. raw:: html

       <p>段落，<a href="http://example.com">链接</a></p>

.. raw:: html

   <p>段落，<a href="http://example.com">链接</a></p>

自动生成目录
------------

在\ `index.rst`\ 里添加类似下面的内容，生成的HTML及PDF会自动生成目录::

    .. toctree::
       :numbered:
       :maxdepth: 2

       setup
       usage
       demo

章节里用::

    .. contents:: 本节内容
       :local:

来插入本章节的目录。

锚点跳转
--------

标题会自动生成锚点，也可以手工创建::

    .. _某章节:

    正文

    :ref:`引用 <某章节>`

    具体查看\ `某章节`_

.. _某章节:

正文

:ref:`引用 <某章节>`

具体查看\ `某章节`_

.. NOTE:: 英文标题会生成合理的锚点ID，但中文标题只会生成类似\ `#id2`\ 这样的锚点。

   如果某一章节需要引用，建议手工创建锚点::

       .. _custom_id:

       章节标题
       ========

CSS样式
-------

创建\ `source/_static/default.css`\ 就可以覆盖内置的样式

.. [#脚注] 脚注内容
