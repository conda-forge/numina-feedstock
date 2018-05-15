About numina
============

Home: http://guaix.fis.ucm.es/projects/numina

Package license: GPL-3.0

Feedstock license: BSD 3-Clause

Summary: Numina reduction package

======
Numina
======

|zenodo| |docs| 

.. image:: https://travis-ci.org/guaix-ucm/numina.svg?branch=master
    :target: https://travis-ci.org/guaix-ucm/numina

.. image:: https://coveralls.io/repos/guaix-ucm/numina/badge.svg?branch=master&service=github 
    :target: https://coveralls.io/github/guaix-ucm/numina?branch=master 

This is Numina, the data reduction package used by the following GTC
instruments: EMIR, FRIDA, MEGARA and MIRADAS.

Numina is distributed under GNU GPL, either version 3 of the License, 
or (at your option) any later version. See the file LICENSE.txt for 
details.

Requirements
------------

Python 2.7 or Python >= 3.4 is required. Numina requires the following
packages installed in order to work properly:

 - setuptools (http://pythonhosted.org/setuptools/)
 - six >= 1.7 (https://pythonhosted.org/six/)
 - numpy >= 1.6 (http://numpy.scipy.org/) 
 - scipy (http://www.scipy.org)
 - astropy >= 1.0 (http://www.astropy.org/)
 - PyYaml (http://pyyaml.org/)
 - dateutil (https://pypi.org/project/python-dateutil/)

For Python 2.7, the following compatibility packages are required:
  - singledispatch (https://pypi.python.org/pypi/singledispatch)
  - enum34 (https://pypi.org/project/enum34/)

The documentation of the project is generated using Sphinx (http://sphinx.pocoo.org/)

Additional packages are optionally required:
 - sphinx (http://sphinx-doc.org) to build the documentation
 - pytest (http://pytest.org) for testing
 - pytest-benchmark (https://github.com/ionelmc/pytest-benchmark/) for 
   benchmarks of certain algorithms

Webpage: https://guaix.fis.ucm.es/projects/numina
Maintainer: sergiopr@fis.ucm.es


Stable version
--------------

The latest stable version of Numina can be downloaded from  
https://pypi.python.org/pypi/numina

To install numina, use the standard installation procedure:::

    $ tar zxvf numina-X.Y.Z.tar.gz
    $ cd numina-X.Y.Z
    $ python setup.py install


The `install` command provides options to change the target directory. By default
installation requires administrative privileges. The different installation options
can be checked with::: 

   $ python setup.py install --help

Development version
-------------------

The development version can be checked out with:::

    $ git clone https://github.com/guaix-ucm/numina.git

And then installed following the standard procedure:::

    $ cd numina
    $ python setup.py install

Building the documentation
--------------------------
The Numina documentation is based on `sphinx`_. With the package installed,
the html documentation can be built from the `doc` directory::

  $ cd doc
  $ make html

The documentation will be copied to a directory under `build/sphinx`. 

The documentation can be built in different formats. The complete list will appear
if you type `make` 

.. _virtualenv: http://pypi.python.org/pypi/virtualenv
.. _sphinx: http://sphinx.pocoo.org

.. |docs| image:: https://readthedocs.org/projects/numina/badge/?version=latest
    :alt: Documentation Status
    :target: http://numina.readthedocs.org/en/latest/?badge=latest

.. |zenodo| image:: https://zenodo.org/badge/13088/guaix-ucm/numina.svg
   :target: http://dx.doi.org/10.5281/zenodo.17986




Current build status
====================

[![Linux](https://img.shields.io/circleci/project/github/conda-forge/numina-feedstock/master.svg?label=Linux)](https://circleci.com/gh/conda-forge/numina-feedstock)
[![OSX](https://img.shields.io/travis/conda-forge/numina-feedstock/master.svg?label=macOS)](https://travis-ci.org/conda-forge/numina-feedstock)
![Windows disabled](https://img.shields.io/badge/Windows-disabled-lightgrey.svg)

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-numina-green.svg)](https://anaconda.org/conda-forge/numina) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/numina.svg)](https://anaconda.org/conda-forge/numina) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/numina.svg)](https://anaconda.org/conda-forge/numina) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/numina.svg)](https://anaconda.org/conda-forge/numina) |

Installing numina
=================

Installing `numina` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `numina` can be installed with:

```
conda install numina
```

It is possible to list all of the versions of `numina` available on your platform with:

```
conda search numina --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](http://docs.anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating numina-feedstock
=========================

If you would like to improve the numina recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/numina-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.