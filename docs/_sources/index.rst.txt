.. pfdocs documentation master file, created by
   sphinx-quickstart on Fri Jun 12 15:23:41 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to pfdocs
=================


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


.. toctree::
   :maxdepth: 2
   :caption: Contents:



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
