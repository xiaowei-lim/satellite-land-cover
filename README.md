# satellite-land-cover

## Step 0 - Environmental Setup
All libraries can be found in the .yaml file.

## Step 1 - Data Setup
Note: _Please download the "United_Kingdom.h5" file from the source here: https://datapub.fz-juelich.de/sen4map/country-wise/_

| sen4map Country | Size   | Last Modified by Creator |
| :--------------- | ---: | :------------------ |
| United Kingdom | 51.0 G | 2024-08-15 11:31 |

Data Source: https://datapub.fz-juelich.de/sen4map/
_(The Sen4Map Benchmark dataset and code used in the project are distributed under MIT License)_
S. Sharma, R. Sedona, M. Riedel, G. Cavallaro, C. Paris, "Sen4Map: Advancing Mapping with Sentinel-2 by Providing Detailed Semantic Descriptions and Customizable Land-Use and Land-Cover Data," in IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing (JSTARS), vol. 17, pp. 13893-13907, 2024, https://doi.org/10.1109/JSTARS.2024.3435081.

## Step 2 - Run Exploratory Data Analysis

*Optional*: Run 01_Data-Explore.ipynb to view the dataset and satellite image bands

Run the 02_Data-Analysis.ipynb to recreate the charts and graphs from the paper

## Step 3 - Set up ML pipeline 
### 3.1 Train-test-val files
Preprocesing ML Data
These sets of code processes the source file "United_Kingdom.h5" into the train-test-val csv files for the baseline, 5km median aggregation and 10-nn scenarios respectively.

⚠️ *Note*: These h5 files may take a LONG TIME TO PROCESS due to the nature of the file type and number of image bands within (>250,000). Alternatively, skip this step as the output files are saved nicely in the github repo for use.

To sum up ...

Input file: 

        United_Kingdom.h5

Output files:

    1. Baseline (no spatial data) scenario:

        uk_monthly_test_norm.csv

        uk_monthly_train_norm.csv

        uk_monthly_val_norm.csv

    2. 10-Nearest Neighbours scenario:

        uk_monthly_test_10nn_norm.csv

        uk_monthly_train_10nn_norm.csv

        uk_monthly_val_10nn_norm.csv

    3. 5km Median Aggregation scenario:

        uk_monthly_test_adj_norm.csv

        uk_monthly_train_adj_norm.csv
        
        uk_monthly_val_adj_norm.csv
### 3.2 ML Models for Different Scenarios 
#### 3.2.1 Baseline (No spatial aggregation)
#### 3.2.2 10-Nearest Neighbours
#### 3.2.3 5km Median Aggregation (Main model used for this study)

### 3.3 Visualisations from ML model


