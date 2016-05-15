====================================
 PySlurm: Slurm interface for Python
====================================

:Authors: Mark Roberts <mark@gingergeeks.co.uk> and Stephan Gorget <phantez@gmail.com>

Overview
========

Currently `PySlurm` is under development to move from it's thin layer on top of the Slurm C API to an object orientated interface.

The current branch is based on the Slurm 14.11.5 to 14.11.8 API with 14.11.9 tentative support.

Prerequistes
=============

This version has been tested with :

	* Slurm 14.11.5-14.11.7, Cython 0.15.1 and Python 2.6.6
	* Slurm 14.11.5-14.11.8, Cython 0.23.4 and Python 2.6.1
	* Slurm 14.11.5-14.11.8, Cython 0.22.1 and Python 2.7.4
	* Slurm 14.11.5-14.11.8, Cython 0.23.1 and Python 2.7.4
	* Slurm 14.11.5-14.11.9, Cython 0.24 and Python 2.7.10


* [Slurm] http://www.schedmd.com
* [Python] http://www.python.org
* [Cython] http://www.cython.org

Installation
============

You will need to instruct the setup.py script where either the Slurm install root 
directory or where the Slurm libraries and Slurm include files are :

#. Slurm default directory (/usr):

	* python setup.py build

	* python setup.py install

#. Indicate Blue Gene type (L/P/Q) on build line:

	* --bgl or --bgp or --bgq

#. Slurm root directory (Alternate installation directory):

	* python setup.py build --slurm=PATH_TO_SLURM_DIR

	* python setup.py install

#. Separate Slurm library and include directory paths:

	* python setup.py build --slurm-lib=PATH_TO_SLURM_LIB --slurm-inc=PATH_TO_SLURM_INC

	* python setup.py install

#. The build will automatically call a cleanup procedure to remove temporary build files but this can be called directly if needed as well with :

	* python setup.py clean

Documentation
=============

`Sphinx <http://www.sphinx-doc.org>`_ (needs to be installed) is currently used to generate the 
documentation from the reStructuredText based doc strings from the module once it is built 
and can be regenerated at any time :

	* cd doc
	* make clean
	* make html

Prebuilt documentation for the module can be reviewed `online
<http://www.gingergeeks.co.uk/pyslurm>`_, and the source code 
is available on `GitHub <http://github.com/gingergeeks/pyslurm>`_.

