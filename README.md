# Sea Ice Concentration (SIC) Prediction using a PINN as an Emulator

ESS 569 Final Project

Sky Gale, Liam Kirkpatrick, Joey Rotondo, and Geraint Webb

### Data Sources
The data sources for this project include:
* Northern hemisphere (NH) sea ice concentration (SIC) data from the National Snow and Ice Data Center (NSIDC)
* Sea surface temperature (SST) data from ERA5, a reanalysis dataset produced by European Centre for Medium-Range Weather Forecasts (ECMWF)

NEED TO ADD: Describe the data modalities, data formats. If applicable, describe large data archives that can be used for model inference, their size.

### Project Objectives
This project aims to:
* Produce a working physics-informed neural network (PINN) using only previous observational data of SIC and SST to predict present day SIC
* Demonstrate that PINNs can be used as simple climate emulators
* Compare the predicted SIC output from the PINN to observed values as ground truth and model validation

### Instructions for setting up the environment
A .yml environment file will be uploaded alongside the PINN script later.

### Script and Notebook Descriptions
_Scripts_

`get_sea_ice_data.ipynb` : This notebook contains the code to download, combine, and clean up the NSIDC SIC data.

_Notebooks_
