.. image:: https://img.shields.io/badge/dmtn--291-lsst.io-brightgreen.svg
   :target: https://dmtn-291.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-291/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-291/actions/

#####################################################
DM Plans for Wavelength-Dependent PSFs and Astrometry
#####################################################

DMTN-291
========

Rubin observations will be affected by differential chromatic refraction (DCR) and other chromatic PSFs at a level that will impact our science goals if left unmitigated, in at least some bands.  This technote describes how we will model these effects and what that means for the data products that science users will see.

Links
=====

- Live drafts: https://dmtn-291.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-291

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-291

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
