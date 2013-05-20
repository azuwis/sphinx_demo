使用
====

构建Sphinx工程
--------------

从零开始
~~~~~~~~

运行::

    sphinx-quickstart foo

之后回答一些问题，就可以在\ `foo`\ 目录下建好工程。

从一开始
~~~~~~~~

下载解压以下链接::

    https://github.com/azuwis/sphinx_demo/archive/master.zip

或者使用Git::

    git clone git://github.com/azuwis/sphinx_demo.git

Sphinx基础
----------

Sphinx工程的目录结构::

    ├── Makefile
    ├── make.bat
    └── source
        ├── conf.py         <-- 配置文件
        ├── index.rst       <-- 文档入口
        ├── *.rst           <-- 文档章节
        └── images          <-- 静态资源，目录名可任意取
           └── *.png

编辑\ `source/conf.py`\ 里的以下部分::

    project = u'测试文档'       # 如"Foo用户文档"
    copyright = u'2013, 作者'   # 如"2013, Foo Corp, Inc."、"2013, 某某有限公司"
    author = u'作者'            # 如"某公司某小组"
    version = '1.0'             # 短版本号，如"1.0"
    release = '1.0'             # 长版本号，如"1.0beta20130808"

`source/index.rst`\ 的\ `toctree`\ 决定了Sphinx处理.rst的顺序，比如::

    .. toctree::
    :maxdepth: 2

    setup
    usage
    demo

则可以看作把\ `setup.rst`\ 、\ `usage.rst`\ 、\ `demo.rst`\ 按顺序拼接起来，一般一个章节一个.rst文件。

使用Livereload
--------------

Windows下双击\ `make-livehtml.bat`\ ，Linux下运行::

    $ cd sphinx_demo
    $ make livehtml

Livereload会自动调用浏览器打开生成的HTML文档，使用任意编辑器编辑\ `.rst`\ 文件，保存时，Livereload会自动更新HTML文档，并刷新浏览器。

.. NOTE::
   Livereload默认使用8000端口，如果已经占用，编辑\ `Makefile`\ 和\ `make.bat`\ 更改。

注意事项
--------

编辑\ `.rst`\ 时注意使用空格，避免用制表符，勿用中文空格。

常用链接
--------

* Sphinx主页 http://sphinx-doc.org/
* Sphinx中文翻译 http://sphinx-doc-zh.readthedocs.org/
