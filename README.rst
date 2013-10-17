http://azuwis.github.io/sphinx_demo/

Howto
=====

Generate HTML::

    # apt-get install --no-install-recommends python-sphinx make
    $ make html

Generate PDF::

    # apt-get install --no-install-recommends texlive-xetex texlive-latex-recommended texlive-latex-extra lmodern fonts-linuxlibertine ttf-wqy-microhei
    $ make latexpdf

Use `livereload`_ to preview HTML, install `livereload browser plugin`_, and::

    # apt-get install --no-install-recommends python-pip
    $ pip install livereload
    $ make livehtml

.. _`livereload`: https://github.com/lepture/python-livereload
.. _`livereload browser plugin`: http://help.livereload.com/kb/general-use/browser-extension

Generate CHM::

    # apt-get install --no-install-recommends fp-utils
    $ make chm

Tested with `python-sphinx 1.1.3` and `texlive 2012.20120611` on Debian unstable.

To use other CJK fonts, modify `latex_elements` option in source/conf.py. For more info, read `xeCJK document`_.

.. _`xeCJK document`: http://mirrors.ctan.org/macros/xetex/latex/xecjk/xeCJK.pdf
