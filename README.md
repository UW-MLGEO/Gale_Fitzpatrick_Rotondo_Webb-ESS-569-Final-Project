# Sea Ice Concentration (SIC) Prediction using a PINN as an Emulator

ESS 569 Final Project

Sky Gale, Joey Rotondo, and Geraint Webb

### Data Sources
The data sources for this project include:
* Northern hemisphere (NH) sea ice concentration (SIC) data from the National Snow and Ice Data Center (NSIDC)
* Sea surface temperature (SST) data from ERA5, a reanalysis dataset produced by European Centre for Medium-Range Weather Forecasts (ECMWF)

Our data is geospatial data in netcdf format. It contains 45 September's worth of data from 50N of SST and of thte total arctic SIC on the same grid. 

NEED TO ADD: Describe the data modalities, data formats. If applicable, describe large data archives that can be used for model inference, their size.

### Project Objectives
This project aims to:
* Produce a working physics-informed neural network (PINN) using only previous observational data of SIC and SST to predict present day SIC
* Demonstrate that PINNs can be used as simple climate emulators
* Compare the predicted SIC output from the PINN to observed values as ground truth and model validation

### Instructions for setting up the environment
A .yml environment file has been uploaded to the main repository directory with environment name 'pinn_sea_ice'. This file serves as the basis for setting up the Python environment necessary to run the Physically Informed Neural Network (PINN) desirable as part of this project.

### Script and Notebook Descriptions
_Scripts_

`get_sea_ice_data.ipynb` : This notebook contains the code to download, combine, and clean up the NSIDC SIC data.

_Notebooks_

### Difficulties/DISCLAIMER

We ran into several difficulties surrounding data file size being too large. To manage this, we moved our data to GitHub's Large File Storage (LFS) system. This still was not enough and eventually we transitioned our data into a google drive: https://drive.google.com/drive/folders/1xMseLz6dco2NJCxW-Hg7OOLT4UGA3CkT?usp=sharing.
