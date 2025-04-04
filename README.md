# 🌍 Satellite Land Cover Classification with Sen4Map

This project applies machine learning to Sentinel-2 imagery using the Sen4Map benchmark dataset to classify land cover types in the United Kingdom.

---

## 📦 Step 0 – Environment Setup

All required libraries are listed in `environmental.yml`:

        conda env create -f environment.yml 
        conda activate senmap



---

## 🗂️ Step 1 – Data Setup

Download `United_Kingdom.h5` from the Sen4Map dataset repository:

https://datapub.fz-juelich.de/sen4map/country-wise/

| Country         | Size   | Last Modified         |
|----------------|--------|------------------------|
| United Kingdom | 51.0 GB | 2024-08-15 11:31       |

**License:** MIT  
**Citation:**  
S. Sharma et al., *Sen4Map: Advancing Mapping with Sentinel-2 by Providing Detailed Semantic Descriptions and Customizable Land-Use and Land-Cover Data*, IEEE JSTARS, 2024. https://doi.org/10.1109/JSTARS.2024.3435081

---

## 📊 Step 2 – Exploratory Data Analysis

- *(Optional)* Run `01_Data-Explore.ipynb` to explore the dataset and Sentinel-2 bands.
- Run `02_Data-Analysis.ipynb` to recreate key visualisations from the study.

---

## 🧪 Step 3 – Machine Learning Pipeline

### 3.1 Preprocessing: Train-Test-Validation Split

Run `03_ml-setup.ipynb` to generate training, validation, and test sets from the raw .h5 file. This script produces input CSVs for the baseline, 5 km median aggregation, and 10-nearest neighbour (10-NN) variants.

**Input:** `United_Kingdom.h5` 

**Outputs:**

  - **Baseline (no spatial context)**  
    - `uk_monthly_train_norm.csv`  
    - `uk_monthly_val_norm.csv`  
    - `uk_monthly_test_norm.csv`  

  - **10-Nearest Neighbours (kNN)**  
    - `uk_monthly_train_10nn_norm.parquet` *(convert to CSV before use)*  
    - `uk_monthly_val_10nn_norm.csv`  
    - `uk_monthly_test_10nn_norm.csv`  

  - **5 km Median Aggregation (Main model)**  
    - `uk_monthly_train_adj_norm.csv`  
    - `uk_monthly_val_adj_norm.csv`  
    - `uk_monthly_test_adj_norm.csv`

⚠️ **Note:** Processing `.h5` files can take time due to size (~250,000 samples). You can skip this step by using the pre-generated outputs included in the repository.

---

### 3.2 Model Training & Evaluation

🔵 **Main Model (5 km aggregation) and Visualisations Used in Report:**  
Run `04_ml-adj.ipynb`

⚫️ **Baseline (no spatial features):**  
Run `05_ml-baseline.ipynb`

⚫️ **10-Nearest Neighbours (optional):**  
Run `06_ml-10nn.ipynb`

---

