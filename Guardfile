#!/usr/bin/env python
from livereload.task import Task
import subprocess
import functools

@functools.partial
def build_sphinx():
    """ Any time a file is modified, call ``make html`` """
    import subprocess
    import sys
    if sys.platform == 'win32':
        subprocess.call(['make.bat', 'html'])
    else:
        subprocess.call(['make', 'html'])

# You may have a different path, e.g. _source/
Task.add('source/', build_sphinx)
