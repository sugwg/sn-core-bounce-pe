# Inferring physical properties of stellar collapse by third-generation gravitational-wave detectors

**Chaitanya Afle<sup>1,2</sup>, Duncan A. Brown<sup>1, 2</sup>**

**<sup>1</sup>Department of Physics, Syracuse University, Syracuse, NY 13244, USA**

**<sup>2</sup>Kavli Institute for Theoretical Physics, University of California, Santa Barbara, CA 93106, USA**

## Introduction

This notebook is a companion to Afle & Brown (2020) posted at [arxiv:](url to archive). In the paper we investigate the ability of Advanced LIGO, Cosmic Explorer 1, and Cosmic Explorer 2 to measure the physical propeties of core-collapse supernovae through its gravitational-wave radiation. This notebook demonstrates the three salient results of this work:

1. Principal components that form our waveform model. The principal components are stored in [principal_components.hdf](https://github.com/sugwg/sn-core-bounce-pe/blob/master/principal_components_files/principal_components.hdf).

2. The map between the model parameters (principal components and their coefficients) and physical parameters (core rotation rate $\beta$ and postbounce oscillation frequency $f_{peak}$).

3. Extracting the posteriors of model parameters from [posterior files](https://github.com/sugwg/sn-core-bounce-pe/tree/master/posterior_files) and using the map to transform these posteriors of physical parameters. 

## License

![Creative Commons License](https://i.creativecommons.org/l/by-sa/3.0/us/88x31.png "Creative Commons License")

This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 United States License](http://creativecommons.org/licenses/by-sa/3.0/us/).


## Runing this notebook in a Docker container

This notebook can be run from a PyCBC Docker container, or a machine with PyCBC installed. Instructions for [downloading the docker container](http://gwastro.github.io/pycbc/latest/html/docker.html) are available from the [PyCBC home page.](https://pycbc.org/) To start a container with instance of Jupyter notebook, run the commands
```sh
docker pull pycbc/pycbc-el7:v1.16.9
docker run -p 8888:8888 --name pycbc_notebook -it pycbc/pycbc-el7:v1.16.9 /bin/bash -l
```
Once the container has started, this git repository can be downloaded with the command:
```sh
git clone https://github.com/sugwg/sn-core-bounce-pe.git
```
The notebook server can be started inside the container with the command:
```sh
jupyter notebook --ip 0.0.0.0 --no-browser
```
You can then connect to the notebook server at the URL printed by ``jupyter``. Navigate to the directory `sn-core-bounce-pe` in the cloned git repository and open [data_release.ipynb](https://github.com/sugwg/sn-core-bounce-pe/blob/master/data_release.ipynb), the notebook that demonstrates use of these reults.

## Acknowledgements
The authors thank Adam Burrows, Daniel Finstad, and Chris Fryer for helpful discussions and the Kavli Institute for Theoretical Physics for hospitality.

### Funding

The authors were supported by National Science Foundation awards PHY-1707954, PHY-1836702, and PHY-2011655. The authors thank the partial support from National Science Foundation award PHY-1748958. Computational work was supported by Syracuse University and National Science Foundation award OAC-1541396.

### Authors contributions