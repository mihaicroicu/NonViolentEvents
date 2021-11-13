# NonViolentEvents

Replication files are available as three `Jupyter Notebooks`, combining data, program code and output into one file. You can explore them without running them at the Github repository of the paper (https://github.com/mihaicroicu/NonViolentEvents) as well as download and run them from Github.

The three notebooks are:

1. One for the analysis concerning Nepal data : https://github.com/mihaicroicu/NonViolentEvents/blob/main/Nepal_submit.ipynb
2. One for the analysis concerning the Sudan data : https://github.com/mihaicroicu/NonViolentEvents/blob/main/darfur_submit.ipynb
3. One for the Bayesian Change Point analysis : https://github.com/mihaicroicu/NonViolentEvents/blob/main/BayesChangePoint_submit.ipynb

Notebooks 1. and 2. are written in `Python`, notebook 3. is written in `R`.

The easiest way to run the three notebooks is installing `Anaconda` and replicate the two virtual environments the code was created into. To do this, we have provided two environment files, that you can use to install the virtual environments:

1. `replicate.yaml` to replicate the Python virtual environment we use.
2. `replicate_r.yaml` to replicate the R virtual environment we use.

Run, at your prompt, in the directory containing the replication data:

`conda env create -f replicate.yaml`

`conda env create -f replicate_r.yaml`

We also provide two `yaml` environment files for exact environment replication at binary level (`replicate_arch.yaml`, `replicate_r_arch.yaml`), but these will only install on OSX 15.

When you are done installing this, activate the environment in the folder with the notebooks and run the notebook server:

For the `Python` notebooks:

`conda activate nver && jupyter notebook`

For the `R` notebook:

`conda activate r_env && jupyter notebook`

A browser will appear. Click the desired notebook, and run it.

Note: All notebooks and code were developed on OSX 10.15, and tested on a variety of Linux distributions (Ubuntu 21.04, Arch-current etc.). Contact us if you are Windows users and want to run the code on Windows. Small numerical differences may appear due to different implementations of the random state generators between operating systems and between systems with different numbers of cores and threads. Runtimes should be reasonable (the Nepal Notebook should run around 20 seconds on a 2019 i9 with 32 GB of RAM, and about 65 seconds on a 2014 i5 with 8 GB of RAM; the Darfur Notebook takes about 100 seconds, mostly due to reading Excel files; the bcp R notebook should take about 3 seconds).
