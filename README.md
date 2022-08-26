python simulator for integrated modelling of 5G (pysim5g)
===========================================

[![Build Status](dhaneshrajpysim5g.svg?branch=master)](pysim5g)
[![Coverage Status](dhaneshraj)](dhaneshraj)

Description
===========
**pysim5g** is an open-source techno-economic assessment framework for 5G deployment.

Based on the Monte-Carlo method, the aim is to enable both engineering and economic cost metrics to be assessed in a unified, systematic framework.

The tool includes statistical analysis of radio interference to assess the system-level performance of 4G and 5G frequency band coexistence (including millimeter wave), while simultaneously quantifying the costs of ultra-dense 5G networks.

One example application of this framework includes exploring the techno-economics of 5G infrastructure sharing strategies.

Example results
===============
![Example](/example_results.png)

Setup and configuration
=======================

All code for **pysim5g** is written in
Python (Python>=3.5) and has a number of dependencies.
See `requirements.txt` for a full list.

Using conda
-----------

The recommended installation method is to use [conda](http://conda.pydata.org/miniconda.html),
which handles packages and virtual environments,
along with the `conda-forge` channel which has a host of pre-built libraries and packages.

Create a conda environment called `pysim5g`:

    conda create --name pysim5g python=3.5

Activate it (run each time you switch projects)::

    activate pysim5g

First, install required packages including `fiona`, `shapely`, `numpy`, `rtree`, `pyproj` and `pytest`:

    conda install fiona shapely numpy rtree pyproj pytest

For development purposes, run this command once per machine:

    python setup.py develop

To install pysim5g permanently:

    python setup.py install

The run the tests:

    pytest

To generate results run:

    python scripts/run.py

To visualize the results, install `matplotlib`, `pandas` and `seaborn`:

    conda install matplotlib pandas seaborn

And then run:

    python vis/vis.py
