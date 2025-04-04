# satellite-land-cover
## Step 1 - Data Setup

Note: _Please download the "United_Kingdom.h5" file from the source here: https://datapub.fz-juelich.de/sen4map/country-wise/_

| sen4map Country | Size   | Last Modified by Creator |
| :--------------- | ---: | :------------------ |
| United Kingdom | 51.0 G | 2024-08-15 11:31 |

Data Source: https://datapub.fz-juelich.de/sen4map/
_(The Sen4Map Benchmark dataset and code used in the project are distributed under MIT License)_
S. Sharma, R. Sedona, M. Riedel, G. Cavallaro, C. Paris, "Sen4Map: Advancing Mapping with Sentinel-2 by Providing Detailed Semantic Descriptions and Customizable Land-Use and Land-Cover Data," in IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing (JSTARS), vol. 17, pp. 13893-13907, 2024, https://doi.org/10.1109/JSTARS.2024.3435081.

## Step 2 - Run Exploratory Data Analysis

Run the EDSA.ipynb to recreate the charts and graphs from the paper

## Step 3 - Set up ML pipeline 
### 3.1 Train-test-val files

### 3.2 ML Models for Different Scenarios 
#### 3.2.1 Baseline (No spatial aggregation)
#### 3.2.2 10-Nearest Neighbours
#### 3.2.3 5km Median Aggregation (Main model used for this study)

### 3.3 Visualisations from ML model


