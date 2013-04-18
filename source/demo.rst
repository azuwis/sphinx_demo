测试章节
========

文字强调
--------

====================================== ==================================
源码                                   结果
====================================== ==================================
``支持对\ *文字*\ 的\ **强调**``       支持对\ *文字*\ 的\ **强调**
``*emphasis* and **strong emphasis**`` *emphasis* and **strong emphasis**
====================================== ==================================

.. NOTE::
    中文文字需要用 ``\空格``

图片
----

========================================================= =====================================================
源码                                                      结果
========================================================= =====================================================
``.. image:: _static/pulpit.jpg``                         .. image:: _static/pulpit.jpg
``.. image:: http://www.w3schools.com/images/pulpit.jpg`` .. image:: http://www.w3schools.com/images/pulpit.jpg
========================================================= =====================================================

.. NOTE::
    生成的PDF不支持外链图片

链接
----

+----------------------------------------------+------------------------------------------+
| 源码                                         | 结果                                     |
+==============================================+==========================================+
| ``http://example.com``                       | http://example.com                       |
+----------------------------------------------+------------------------------------------+
| ``This is a `link <http://example.com>`_``   | This is a `link <http://example.com>`_   |
+----------------------------------------------+------------------------------------------+
| ``这也是一个\ `链接 <http://example.com>`_`` | 这是一个\ `链接 <http://example.com>`_   |
+----------------------------------------------+------------------------------------------+
| ``这是一个\ `链接`_``                        | 这也是一个\ `链接`_                      |
|                                              |                                          |
| ``.. _`链接`: http://example.com``           | .. _`链接`: http://example.com           |
+----------------------------------------------+------------------------------------------+

代码段
------

ruby代码样例

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

自动生成目录
------------

见生成的HTML及PDF

锚点跳转
--------

见生成的HTML及 PDF

表格
----

==== ====
中文 表格
==== ====
测试 测试
测试 测试
==== ====

CSS样式
-------

创建source/_static/default.css就可以覆盖内置的样式
