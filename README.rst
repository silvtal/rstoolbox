RosettaSilentToolbox
====================

This repo fixes a very small bug trat prevented `plot_96wells` from working. Also, if you're using the original tutorials, remove the `set_ticks` line too

    np.random.seed(0)
    
    df = pd.DataFrame(np.random.randn(8, 12))
    
    fig, ax = plot_96wells(cdata = df, sdata = -df, bdata = df<0)
    
    plt.subplots_adjust(left=0.1, right=0.8, top=0.9, bottom=0.1)
    
    # set_ticks(range(8))
    
    plt.show()
    
    plt.close()

Install

    git clone https://github.com/silvtal/rstoolbox
    
    cd rstoolbox
    
    git archive --output=./rstoolbox_repo_archive.tar --format=tar HEAD
    
    python -m pip install rstoolbox_repo_archive.tar 

.. image:: https://travis-ci.org/jaumebonet/RosettaSilentToolbox.svg?branch=master
    :target: https://travis-ci.org/jaumebonet/RosettaSilentToolbox
    :alt: Build Status

.. image:: https://coveralls.io/repos/github/jaumebonet/RosettaSilentToolbox/badge.svg?branch=master
    :target: https://coveralls.io/github/jaumebonet/RosettaSilentToolbox?branch=master
    :alt: Coverage Status

.. image:: https://codecov.io/gh/jaumebonet/RosettaSilentToolbox/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/jaumebonet/RosettaSilentToolbox
    :alt: codecov

.. image:: https://img.shields.io/pypi/pyversions/rstoolbox.svg
    :target: https://pypi.org/project/rstoolbox/
    :alt: Python Versions

.. image:: https://api.codacy.com/project/badge/Grade/8e2823ea80984efc8b764f9d8d26ecf6
    :target: https://www.codacy.com/app/jaumebonet/RosettaSilentToolbox?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=jaumebonet/RosettaSilentToolbox&amp;utm_campaign=Badge_Grade
    :alt: Codacy Badge

The ``rstoolbox`` is a python library aimed to the analysis and management of big populations of protein or nucleotide decoys.

.. image:: https://img.shields.io/badge/bioRxiv%20preprint-doi.org/10.1101/428045-blue.svg
    :target: https://doi.org/10.1101/428045
    :alt: bioRxiv

.. image:: https://img.shields.io/badge/BMC%20Bioinformatics-doi.org/10.1186/s12859--019--2796--3-green.svg
    :target: https://doi.org/10.1186/s12859-019-2796-3
    :alt: BMC Bioinformatics

Although inspired by the output of the protein design tool **ROSETTA**, the library aims to be of a wider applicability, and can be
easily set up to retrieve data from other design tools.

It is particularly aimed towards two distinct user profiles:

1. Protein designers comfortable with light scripting to process their data. Ideally, used to work with **Ipython**, for which this library has a particular affinity.
2. Developers that develop new protein design tools/protocols/approaches and wish to benchmark their innovations with previously existing methods.

See a working example notebook at:

.. image:: https://mybinder.org/badge_logo.svg
    :target: https://mybinder.org/v2/gh/lpdi-epfl/rstoolbox/51ccd51?filepath=notebook
    :alt: Binder

Despite its name, the library **does not require a local installation of ROSETTA**, files can be imported from whatever cluster service the user has access to. That said, some functions can or need to exploit **ROSETTA**. Those functions are few and their requirements are
clearly highlighted on their `documentation <http://lpdi-epfl.github.io/RosettaSilentToolbox>`_.

Start using the ``rstoolbox`` is as easy as installing it via pip:

.. code-block:: bash

    pip install rstoolbox


A complete `documentation <http://jaumebonet.cat/RosettaSilentToolbox>`_ with detailed explanation for each function is available.
