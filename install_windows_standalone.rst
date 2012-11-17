====================================================
How to install on Windows (stand alone installer)
====================================================

We are looking forward to your usage reports for Standalone-installer. Earlier report is here: :ref:`mailinglist`.

.. contents::


Sphinx standalone installer
==============================

* `SphinxInstaller_ja-1.1.3.20121026-py2.7-win32.zip`_

.. _`SphinxInstaller_ja-1.1.3.20121026-py2.7-win32.zip`: https://bitbucket.org/sphinxjp/website/downloads/SphinxInstaller_ja-1.1.3.20121026-py2.7-win32.zip

Includes::

   Python: 2.7.3

   Sphinx: 1.1.3 + patch (`PR#61`_, `PR#81`_)

   sphinxjp.themecore 0.1.3
   sphinxjp.themes.bizstyle 0.1.5
   sphinxjp.themes.dotted 0.1.1
   sphinxjp.themes.htmlslide 0.1.4
   sphinxjp.themes.impressjs 0.1.2
   sphinxjp.themes.s6 0.2.0
   sphinxjp.themes.solarized 0.1.0
   sphinxjp.themes.sphinxjp 0.1.1
   sphinxjp.themes.trstyle 0.1.0

   sphinxcontrib-actdiag = 0.5.0
   sphinxcontrib-blockdiag = 1.2.0
   sphinxcontrib-nwdiag = 0.6.0
   sphinxcontrib-seqdiag = 0.5.0

   blockdiag = 1.2.0
   blockdiagcontrib-class = 0.1.3
   blockdiagcontrib-qb = 0.1.3
   blockdiagcontrib-square = 0.1.3
   actdiag = 0.4.0
   nwdiag = 0.9.0
   seqdiag = 0.8.0

   distribute = 0.6.30
   docutils = 0.9.1
   funcparserlib = 0.3.5
   jinja2 = 2.6
   pillow = 1.7.7
   pygments = 1.5
   pypng = 0.0.13
   webcolors = 1.4
   zc.recipe.egg = 1.3.2
   zc.buildout = 1.6.3



Install using the Standalone Sphinx
==========================================================

Download latest `Sphinx standalone installer`_ and execute it. The
installer installs python, sphinx and path settings.

.. note::


   If you are going to install on Windows Vista or later, you may need
   to install with administrator privilege (right click and choose
   "Run as Administrator").

Run **Command Prompt** or enter ``cmd`` to the "search program and
files" text box. After command prompt window appear, type
``python[Enter]``. If you can get installed python version and prompt
about ``>>>``, the Python installation is succeeded.  Enter ``Ctrl+Z``
key to quit.

Next, try to enter ``sphinx-quickstart``` at the Command Prompt. If
you get these text, the Sphinx installation is succeeded. Enter
``Ctrl+C`` key to quit.

That it. Install is over. Let's go to  :doc:`make_project`.

::

  Welcome to the Sphinx 1.0.8 quickstart utility.

  Please enter values for the following settings (just press Enter to
  accept a default value, if one is given in brackets).

  Enter the root path for documentation.
  > Root path for the documentation [.]:


.. warning::

   If you set ``PYTHONPATH`` environment variable, the installer may
   fail to install. To get the current PYTHONPATH environment
   valuable, type :command:`set PYTHONPATH` on the Command Prompt. You
   need to delete this value (delete may cause other problem) or enter 
   :command:`set PYTHONPATH=` every time before you use Sphinx command
   disable this valuable temporarily.

   Some program such as old Thinkpad or Track Lightning may set
   PYTHONPATH environment variable automatically.


Release Note
====================

* 20121026_

  * Based upon Sphinx-1.1.3 release
  * include `PR#81`_ (newer LaTeX Japanese LaTeX path)
  * include `PR#61`_ (Japanese file name patch)
  * include newer blockdiag at 2012/10/26

* 20111025_

  * Change the base sphinx to 1.0.8
  * latest blockdiag family

* 20110830_

  * Change the base sphinx to 1.0.7
  * Includes Pillow instead of PIL

* 20110620_

  * Fix the stalling problem when the off-line

* 20110618

  * Initial release

`other releases`_


.. _20110620: https://bitbucket.org/sphinxjp/website/downloads/Sphinx-1.0.7.alpha20110620-py2.7-win32.exe
.. _20110830: https://bitbucket.org/sphinxjp/website/downloads/Sphinx-1.0.7alpha_20110830-py2.7-win32.zip
.. _20111025: https://bitbucket.org/sphinxjp/website/downloads/Sphinx-1.0.8_ja_20111025-py2.7-win32.zip
.. _20121026: https://bitbucket.org/sphinxjp/website/downloads/SphinxInstaller_ja-1.1.3.20121026-py2.7-win32.zip
.. _`other releases`: https://bitbucket.org/sphinxjp/website/downloads
.. _`PR#61`: https://bitbucket.org/birkenfeld/sphinx/pull-request/61
.. _`PR#81`: https://bitbucket.org/birkenfeld/sphinx/pull-request/81

