.. pfdocs documentation master file, created by
   sphinx-quickstart on Fri Jun 12 15:23:41 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to pfdocs
=================

Hi. I'm Pete, and I write technical docs.

.. code-block:: make

   github:
      @make clean
      @rm -rfv docs/
      @make html
      @cp -a build/html/. ./docs

.. code-block:: make

   publish:
      @make clean
      @rm -rfv docs/
      @make html
      @cp -a build/html/. ./docs
      @git commit -am "update content"
      @git push


Autobuilding
************

You can set up auto-building on every save of a ``.rst`` file:

#. Activate virtualenv, if not already active::

    source bin/activate
#. Install watchdog tools, if not already installed::

    pip install watchdog
#. Run watchmedo to monitor all .rst files::

watchmedo shell-command \
   --patterns="*.rst" \
   --ignore-pattern='_build/*' \
   --recursive \
   --wait \
   --command='make html'

.. toctree::
   :maxdepth: 2
   :caption: Contents:

Cool Resources
++++++++++++++

- `Publishing Sphinx-generated docs on GitHub Pages <http://daler.github.io/sphinxdoc-test/>`_
- `Docs Like Code <https://www.docslikecode.com/>`_

   * `Yes You Can Use GitHub Pages with Python Sphinx <https://www.docslikecode.com/articles/github-pages-python-sphinx/>`_

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
