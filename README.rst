http://azuwis.github.io/sphinx_demo/

To generate HTML::

    # apt-get install --no-install-recommends python-sphinx make
    $ make html

To generate PDF::

    # apt-get install --no-install-recommends texlive-xetex texlive-latex-recommended texlive-latex-extra lmodern ttf-wqy-microhei
    $ make latexpdf

To use `Livereload <https://github.com/mockko/livereload>`_::

    # apt-get install --no-install-recommends python-pip
    $ pip install livereload
    $ make livehtml

To generate CHM::

    # apt-get install --no-install-recommends fp-utils
    $ make chm

Tested with `python-sphinx 1.1.3` and `texlive 2012.20120611` on Debian unstable.

To use other CJK fonts, modify `latex_elements` option in source/conf.py. For more info, read http://mirrors.ctan.org/macros/xetex/latex/xecjk/xeCJK.pdf
