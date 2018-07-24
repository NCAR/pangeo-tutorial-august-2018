# NCAR August 2018 Pangeo Tutorial

This repository contains materials for the Pangeo Tutorial [Atmospheric data analysis with Dask and Xarray](https://sea.ucar.edu/event/atmospheric-data-analysis-dask-and-xarray) that will be presented at the August 1, 2018, NCAR Pangeo Tutorial proceeding the Pangeo Developers Workshop (August 13-15, 2018).

## Front Matter

<img src="./images/pangeo_card_green.png" height="125"> <img src="./images/xarray.png" height="125"> <img src="./images/dask.png" height="125"> <img src="./images/jupyter.png" height="125">

-----

- **[About Pangeo](https://pangeo-data.github.io/):** Pangeo is a community effort for big data in the geosciences using Python. A key component of the Pangeo effort is the improved integration of [Xarray](http://xarray.pydata.org/en/latest/index.html) and [Dask](http://dask.pydata.org/en/latest/index.html) to enable analysis of very large datasets.
- **[About Xarray](http://xarray.pydata.org/en/latest/index.html):** xarray is an open source project and Python package that aims to bring the labeled data power of pandas to the physical sciences, by providing N-dimensional variants of the core pandas data structures.
- **[About Dask](http://dask.pydata.org/en/latest/index.html):** Dask is a flexible parallel computing library for analytic computing.
- **[About Jupyter](http://jupyter.org/):** Project Jupyter exists to develop open-source software, open-standards, and services for interactive computing across dozens of programming languages. The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more.

## Setup

This tutorial is designed to run on the [Cheyenne High-Performance Computer](https://www2.cisl.ucar.edu/resources/computational-systems/cheyenne), [Pangeo's JupyterHub deployed on Google Compute Platform](http://pangeo.pydata.org/), or on a local computer (see *Running Locally* below). The larger sample datasets may only be available on GCP and/or Cheyenne.  **We recommend running this tutorial on your local computer until you get to Section 3.**

For detailed setup instructions, see [setup.md](./setup.md).

### Running Locally

```
git clone https://github.com/NCAR/pangeo-tutorial-august-2018.git
cd pangeo-tutorial-august-2018
conda env create -f environment.yml -n pangeo
source activate pangeo
```

Then start a JupyterLab server:

```
jupyter lab
```

## Acknowledgements

At its core, Pangeo is a community effort built around open-source software. As such, the credit for the developments of the software described here belongs with the community that created it. Ryan Abernathey, Joe Hamman, and Matt Rocklin provided resources and input specific to this tutorial.

Elements of this tutorial were taken from the Xarray, Dask, Cartopy, Holoviews, and Geoviews documentation. Some pieces of text in the Xarray portion of the tutorial were adapted from Hoyer and Hamman (2016).

Pangeo is [supported](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1740633&HistoricalAwards=false) by the [National Science Foundation (NSF)](https://www.nsf.gov/) and the [EarthCube Program](https://www.earthcube.org/). NCAR is separately supported by the [National Science Foundation (NSF)](https://www.nsf.gov/).

Google provided compute credits on [Google Compute Engine](https://cloud.google.com/), which are used to back the Pangeo GCP deployment.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
