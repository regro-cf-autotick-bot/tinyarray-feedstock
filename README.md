About tinyarray
===============

Home: http://git.kwant-project.org/tinyarray/about/

Package license: BSD 2-Clause

Feedstock license: BSD 3-Clause

Summary: Arrays of numbers for Python, optimized for small sizes

Tinyarrays are similar to NumPy arrays, but optimized for small sizes.
Common operations on very small arrays are to 3-7 times faster than
with NumPy (with NumPy 1.6 it used to be up to 35 times), and 3 times
less memory is used to store them. Tinyarrays are useful if you need
many small arrays of numbers, and cannot combine them into a few
large ones.


Installing tinyarray
====================

Installing `tinyarray` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `tinyarray` can be installed with:

```
conda install tinyarray
```

It is possible to list all of the versions of `tinyarray` available on your platform with:

```
conda search tinyarray --channel conda-forge
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


Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)

Current build status
====================

Linux: [![Circle CI](https://circleci.com/gh/conda-forge/tinyarray-feedstock.svg?style=shield)](https://circleci.com/gh/conda-forge/tinyarray-feedstock)
OSX: [![TravisCI](https://travis-ci.org/conda-forge/tinyarray-feedstock.svg?branch=master)](https://travis-ci.org/conda-forge/tinyarray-feedstock)
Windows: [![AppVeyor](https://ci.appveyor.com/api/projects/status/github/conda-forge/tinyarray-feedstock?svg=True)](https://ci.appveyor.com/project/conda-forge/tinyarray-feedstock/branch/master)

Current release info
====================
Version: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/tinyarray/badges/version.svg)](https://anaconda.org/conda-forge/tinyarray)
Downloads: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/tinyarray/badges/downloads.svg)](https://anaconda.org/conda-forge/tinyarray)


Updating tinyarray-feedstock
============================

If you would like to improve the tinyarray recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/tinyarray-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.
