安装
====

安装Sphinx
----------

Windows
~~~~~~~

#. 安装Python

   到\ http://python.org/getit/\ 下载安装 Python2 32位版本，当前版本是\ `python 2.7.5 <http://python.org/ftp/python/2.7.5/python-2.7.5.msi>`_\ 。

#. 添加Python路径到Path环境变量里

   右键点击\ `我的电脑`\ ->\ `属性`\ ->\ `高级`\ ->\ `环境变量`\ ，修改\ `系统环境变量`\ 里的\ `Path`\ ，假设Python安装路径为\ `C:\\Python2.7.5`\ ，原来的\ `Path`\ 为\ `%SystemRoot%\\system32`\ ，则改为::

     %SystemRoot%\system32;C:\Python2.7.5;C:\Python2.7.5\Scripts

#. 安装Easy_install

   下载\ http://python-distribute.org/distribute_setup.py\ 到本地，并双击安装。

#. 安装Sphinx及Livereload

   点击\ `开始`\ ->\ `运行`\ ->\ `cmd`\ 来打开命令提示符，并运行::

     easy_install sphinx livereload

Linux(Debian/Ubuntu)
~~~~~~~~~~~~~~~~~~~~

::

# apt-get install python-sphinx python-pip
# pip install livereload

Sphinx版本
----------

推荐使用 Sphinx 1.1.3 及以后的版本。

安装Livereload浏览器插件
------------------------

`Livereload <https://github.com/mockko/livereload>`_\ 支持以下浏览器：

+---------------+------------------------------------------------------------------------------+
| 浏览器        | 插件链接                                                                     |
+===============+==============================================================================+
| Google Chrome | https://chrome.google.com/extensions/detail/jnihajbhpnppcggbcgedagnkighmdlei |
+---------------+------------------------------------------------------------------------------+
| Safari        | https://github.com/downloads/mockko/livereload/LiveReload-1.6.2.safariextz   |
+---------------+------------------------------------------------------------------------------+
| Firefox       | https://addons.mozilla.org/firefox/addon/livereload/                         |
+---------------+------------------------------------------------------------------------------+

选择合适的编辑器
----------------

Windows
~~~~~~~

选择用对Unix格式换行支持良好、中文显示宽度为英文两倍的编辑器。

+----------------+----------------------------------------------------+
| 编辑器         | 链接                                               |
+================+====================================================+
| Sublime text 2 | http://www.sublimetext.com                         |
+----------------+----------------------------------------------------+
| Notepad++      | http://notepad-plus-plus.org/                      |
+----------------+----------------------------------------------------+
| GVim           | http://www.vim.org/download.php                    |
+----------------+----------------------------------------------------+
| Eclipse插件    | http://marketplace.eclipse.org/content/rest-editor |
+----------------+----------------------------------------------------+

Linux
~~~~~

Vim、Emacs、GEdit等对reStructuredText都有良好的支持。
