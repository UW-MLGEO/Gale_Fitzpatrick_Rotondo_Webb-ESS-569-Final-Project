# Sea Ice Concentration (SIC) Prediction using a Simple PINN as an Emulator

ESS 569 Final Project

Authors: Sky Gale, Joey Rotondo, and Geraint Webb

### Project Objectives
This project aims to:
* Produce a working physics-informed neural network (PINN) using only previous observational data of SIC and SST to predict present day SIC
* Demonstrate that PINNs can be used as simple climate emulators
* Compare the predicted SIC output from the PINN to observed values as ground truth and model validation

### Data Sources
The data sources for this project include **Northern hemisphere (NH) sea ice concentration (SIC)** and **Sea surface temperature (SST)** data from ERA5, a reanalysis dataset produced by European Centre for Medium-Range Weather Forecasts (ECMWF).

Our data is geospatial data in netcdf format. It contains 45 September's worth of data from 50N of SST and of the total arctic SIC on the same grid. 

**Data Modalities and Formats**
This project utilizes the following data modalities and formats for model inference in sea ice prediction:

_Data Modalities_

Type: Reanalysis
Variable(s): Sea Ice Concentration (SIC), Sea Surface Temperature (SST)
Source: ERA5 reanalysis datasets from the European Centre for Medium-Range Weather Forecasts (ECMWF)

_Data Formats_

NetCDF (.nc): The primary format used for storing multidimensional scientific data, applicable to both satellite and reanalysis datasets.

ERA5 Reanalysis:
Description: Provides detailed and comprehensive reanalysis data, including Sea Surface Temperature and other climate variables.
Size: Multiple petabytes of climate data, available on a global scale with hourly resolution.
Data Access: DOI - https://doi.org/10.24381/cds.adbb2d47, URL - https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview

### Instructions for setting up the environment
A .yml environment file has been uploaded to the main repository directory with environment name 'pinn_sea_ice'. This file serves as the basis for setting up the Python environment necessary to run the Physically Informed Neural Network (PINN) desirable as part of this project.

### Script and Notebook Descriptions
_Notebooks_

`get_sst_data.ipynb`: Designed for downloading and preprocessing sea surface temperature (SST) data from the ERA5 reanalysis dataset. It outlines steps to retrieve the data, clean it, and structure it for use in subsequent analyses. The notebook ensures that the SST data is ready for integration with other datasets, such as sea ice concentration, for modeling purposes.

`process_sic_sst_data.ipynb`: Contains the code to download, combine, and clean up the ERA5 SIC and SST data at once. It includes steps for loading raw data, cleaning, and transforming it to prepare for analysis. Key operations involve removing missing or invalid values, aggregating data over specific time periods, and formatting it for compatibility with machine learning models. The notebook aims to ensure that the dataset is clean and structured appropriately for subsequent modeling tasks in the project. It also focuses on transforming and preparing the cleaned data for use in artificial intelligence applications. It involves reshaping the dataset, normalizing values, and possibly splitting the data into training and testing sets. The goal is to ensure the data is structured appropriately for training machine learning models, enhancing the effectiveness of the predictive algorithms.

Note: This notebook performs the fetching, cleaning, and preparing of the SIC and SST data since saving the data at each step overwhelmed the Github, so only the final product is output as a .nc file.

### Difficulties/DISCLAIMER

We ran into several difficulties surrounding data file size being too large. To manage this, we moved our data to GitHub's Large File Storage (LFS) system. This still was not enough and eventually we transitioned our data into a **google drive**: https://drive.google.com/drive/folders/1xMseLz6dco2NJCxW-Hg7OOLT4UGA3CkT?usp=sharing.
