=================================
Install on the Mac OS X or Linux
=================================

There are several way to install Mac OS X or Linux.

Using packaging system
========================================

MacPorts
--------

If you use Mac OS X `MacPorts <http://www.macports.org/>`_ , use this
command to install all software.

.. code-block:: bash

   $ sudo port install py27-sphinx

However, the execution path is not added, use select command to use
Python2.7 as default.

.. code-block:: bash

   $ sudo port select --set python python27
   $ sudo port select --set sphinx py27-sphinx

Type ``which sphinx-quickstart`` to check the installation.

Debian/Ubuntu
-------------------

You may install using this command if you use Debian/Ubuntu.

.. code-block:: bash

   $ aptitude install python-sphinx


Install by your own
======================

If you use system installed Python or build your own Python, you can
use that python to install Sphinx. The actual command list is same as
these install.

* :ref:`install_easy_install`
* :ref:`install_sphinx`

After install
==================

That it. Install is over. Let's go to  :doc:`make_project` to make
Sphinx project.

