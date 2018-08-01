Getting Started with Pangeo
===============

This notebooks in this tutorial are designed to run on the Cheyenne High-Performance Computer, Pangeo's JupyterHub deployed on Google Compute Platform, or on a local computer (see Running Locally below). Most of the datasets used in the tutorial are small and are packaged with xarray. The larger sample datasets may only be available on GCP and/or Cheyenne.

## Prerequisites

There are some basic requirements before the rest of this setup can work for you.  These include:

1. Have `git` installed on your system

1. Have a Github account (accounts are free)

1. Have a modern web browser (Chrome, Safari, etc.)

1. Basic understanding of your machine's command-line interface (e.g., Mac OS's Terminal application)

## Setup Python for working on a personal computer or on Cheyenne

#### Download Miniconda

    # for linux
    $ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh

    # for osx
    $ curl https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o miniconda.sh

    # for windows
    # go to: https://conda.io/miniconda.html

#### Install Miniconda

    $ bash miniconda.sh
    # follow instructions

At this point, you may need to make sure that `conda` is available in your path.  (Installing Miniconda should give you the option of putting a line at the end of your profile/login script to add `conda` to your path when you log in, again.  You may need to `source` your profile/login script or re-login or open a new terminal window to activate this change.)

#### Download the Tutorial Repository & Enter the Repository Directory

    $ git clone https://github.com/ncar/pangeo-tutorial-august-2018
    $ cd pangeo-tutorial-august-2018
    
#### Install Pangeo Environment

*This step can take some time.  If it fails, just run it again and it will pick up where it left off.*

    $ conda env create --file environment.yml

#### Activate the Pangeo Environment

This step, apparently, assumes that you're shell is `bash` or something like it.  If you are using `csh` or `tcsh`, you may need to run the following commands in a `bash` login (e.g., type `bash`, hit enter, and continue).

    $ source activate pangeo

#### Install the necessary Jupyter Plugins

*These steps can also take some time.  Just FYI.*

    $ jupyter labextension install jupyterlab_bokeh
    $ jupyter labextension install @pyviz/jupyterlab_pyviz

#### Run a quick test

    $ python

    >>> import xarray as xr
    >>> xr.show_versions()
    >>> xr.tutorial.load_dataset('air_temperature')
    >>> xr.tutorial.load_dataset('rasm')

## Launching Jupyter locally

    $ jupyter lab

## Launching Jupyter and Dask on Cheyenne

  1. Launching jupyter lab requires a few extra steps (on Cheyenne)

         $ export PBS_ACCOUNT=[your project number]
         $ qinteractive -l walltime=4:00:00
         $ export LD_LIBRARY_PATH=
         $ source activate pangeo
         $ ./start-jlab

  1. Run the ssh command returned by `start-jlab` on your local computer, and then open up `localhost:8888` in your browser

  1. Once you start the `distributed` cluster, you can create another ssh tunnel to the Dashboard.
