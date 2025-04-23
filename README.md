# credit-card-fraud-detection

The aim of the project is to build a model where the forecasted variable is the number of shipments in a given week. This repository contains code written in Python using Jupyter Notebooks, along with a `requirements.txt` file for dependency management.

## Overview

This project uses XGBoost models to effectively forecast posting volumes for multiple clients. There is separate model for Customer_X due to the provided forecast and significantly higher average number of packages sent. Model build for remaining clients incorporates laged volume values and dummy variables to distinguish clients. 

## Dataset

- **Data description:**
  - DimDates - CSV File - Database with information about dates
  - PostingVolumes - Parquet File - Database with daily shipments
  - X_ClientsORDERS - EXCEL File - Data provided by the client (X) since the beginning of 2023. Data for the upcoming month is sent at the end of the previous one. The file contains the number of orders (on the client's platform) expected by the client's analytics team for each day of the upcoming month for the APM product.
  - Zadanie_Dane_Temperatura - Folder with CSV Files - The folder contains CSV files where each file stores data on temperatures

- **Location in this Project:**  
  The dataset files are stored in the `input/` folder.

## Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/alestankiewicz/shipment-volume-forecating.git
    cd shipment-volume-forecating

2. **Set Up a Virtual Environment (Optional but Recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate

3. **Install the Required Packages:**
    ```bash
    pip install -r requirements.txt

## Usage

- **Launch Jupyter Notebook:**
  ```bash
  jupyter notebook

- **Open the notebooks:**
  - data_preparation.ipynb for data preprocessing and exploratory data analysis.
  - model_development.ipynb for training models and evaluating performance.

## Methodology

- **Data Preprocessing:**
  - Handling missing data and analysis of datasets. 

- **Model Training & Hyperparameter Tuning:** 
  - XGBoost regressor is used on the preprocessed data.
  - Rolling window split is used to split data. 
  - Gaussian process minimization (gp_minimize()) is applied for hyperparameter optimization to find the best model configurations.

- **Evaluation:**  
  - The models are evaluated using RMSE. 

## Results
  - Detailed visualizations (provided within the notebooks) that show data analysis findings and show model results.
  - suggestions for future improvements. 
