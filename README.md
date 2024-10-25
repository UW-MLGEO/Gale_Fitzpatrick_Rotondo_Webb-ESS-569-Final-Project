# Sea Ice Concentration (SIC) Prediction using a PINN as an Emulator

ESS 569 Final Project

Sky Gale, Joey Rotondo, and Geraint Webb

### Data Sources
The data sources for this project include:
* Northern hemisphere (NH) sea ice concentration (SIC) data from the National Snow and Ice Data Center (NSIDC)
* Sea surface temperature (SST) data from ERA5, a reanalysis dataset produced by European Centre for Medium-Range Weather Forecasts (ECMWF)

Our data is geospatial data in netcdf format. It contains 45 September's worth of data from 50N of SST and of the total arctic SIC on the same grid. 

**Data Modalities and Formats**
This project utilizes the following data modalities and formats for model inference in sea ice prediction:

_Data Modalities_

Satellite Observations:
Type: Sea ice concentration and related variables.
Source: National Snow and Ice Data Center (NSIDC).
Reanalysis Data:
Type: Sea Surface Temperature (SST) data.
Source: ERA5 reanalysis datasets from the European Centre for Medium-Range Weather Forecasts (ECMWF).
Data Formats

NetCDF (.nc): The primary format used for storing multidimensional scientific data, applicable to both satellite and reanalysis datasets.

National Snow and Ice Data Center (NSIDC):
Description: Offers extensive datasets related to snow and ice, including daily sea ice concentration and extent from satellite observations.
Size: Several terabytes of data spanning multiple decades.
Access: NSIDC Data Search: https://nsidc.org/data/g02202/versions/4
ERA5 Reanalysis:
Description: Provides detailed and comprehensive reanalysis data, including Sea Surface Temperature and other climate variables.
Size: Multiple petabytes of climate data, available on a global scale with hourly resolution.
Access: ERA5 Data Access: https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview

### Project Objectives
This project aims to:
* Produce a working physics-informed neural network (PINN) using only previous observational data of SIC and SST to predict present day SIC
* Demonstrate that PINNs can be used as simple climate emulators
* Compare the predicted SIC output from the PINN to observed values as ground truth and model validation

### Instructions for setting up the environment
A .yml environment file has been uploaded to the main repository directory with environment name 'pinn_sea_ice'. This file serves as the basis for setting up the Python environment necessary to run the Physically Informed Neural Network (PINN) desirable as part of this project.

### Script and Notebook Descriptions
_Notebooks_

`get_sea_ice_data.ipynb`: This notebook contains the code to download, combine, and clean up the NSIDC SIC data.

`clean_sea_ice_data.ipynb`: focuses on preprocessing sea ice concentration data. It includes steps for loading raw data, cleaning, and transforming it to prepare for analysis. Key operations involve removing missing or invalid values, aggregating data over specific time periods, and formatting it for compatibility with machine learning models. The notebook aims to ensure that the dataset is clean and structured appropriately for subsequent modeling tasks in the project.

`get_sst_data.ipynb`: is designed for downloading and preprocessing sea surface temperature (SST) data from the ERA5 reanalysis dataset. It outlines steps to retrieve the data, clean it, and structure it for use in subsequent analyses. The notebook ensures that the SST data is ready for integration with other datasets, such as sea ice concentration, for modeling purposes.

`prepare_AI_ready_sea_ice_data.ipynb`: focuses on transforming and preparing the cleaned sea ice concentration data for use in artificial intelligence applications. It involves reshaping the dataset, normalizing values, and possibly splitting the data into training and testing sets. The goal is to ensure the data is structured appropriately for training machine learning models, enhancing the effectiveness of the predictive algorithms.

### Difficulties/DISCLAIMER

We ran into several difficulties surrounding data file size being too large. To manage this, we moved our data to GitHub's Large File Storage (LFS) system. This still was not enough and eventually we transitioned our data into a **google drive**: https://drive.google.com/drive/folders/1xMseLz6dco2NJCxW-Hg7OOLT4UGA3CkT?usp=sharing.
