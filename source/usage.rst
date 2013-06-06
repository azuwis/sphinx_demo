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

Livereload会自动调用浏览器打开生成的HTML文档，使用任意编辑器编辑\ `.rst`\ 文件，保存时，Livereload会自动更新HTML文档，并刷新浏览器，保留页面位置。

Livereload只负责更新HTML和刷新浏览器，并不能自动打开对应页面，编辑前需要先手工定位浏览器到对应的页面位置。

另外注意，浏览器URL里有锚点的话，刷新页面时一定会跳到这一锚点上。

.. NOTE::
   Livereload默认使用8000端口，如果已经占用，编辑\ `Makefile`\ 和\ `make.bat`\ 更改。

注意事项
--------

* 编辑\ `.rst`\ 时注意使用空格，不要用制表符、中文空格。
* 用锚点来引用章节，不要用章节数字编号。
* 不要手工给列表、章节添加数字标号，Sphix能自动编号。列表可用\ ``#.``\ ，章节可给\ ``.. toctree::``\ 添加\ ``:numbered:``\ 属性。
* 如果Sphinx出现奇怪的行为(修改样式不生效、自动编号不正确等)，可以尝试先清除缓存(运行\ ``make clean``\ ，或者删除\ `build`\ 目录)，再重新生成目标文件。

常用链接
--------

* Sphinx主页 http://sphinx-doc.org/
* Sphinx中文翻译 http://sphinx-doc-zh.readthedocs.org/
