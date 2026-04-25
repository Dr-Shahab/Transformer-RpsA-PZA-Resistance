# Step 1: Data Retrieval and Preparation

## Purpose
This step retrieves and preprocesses Mycobacterium tuberculosis bioactivity data from the ChEMBL database.

## Input
- raw_mtb_data.csv: Raw dataset containing compound bioactivity information retrieved from ChEMBL.

## Code
- dataset_preparation.ipynb: Jupyter notebook used for data cleaning, filtering, and standardization (removal of duplicates, missing values, and structural normalization using RDKit).

## Output
- curated_mtb_dataset.csv: Cleaned and standardized dataset used for downstream analysis.

## How to run
Open and execute the notebook:

```bash
jupyter notebook code/dataset_preparation.ipynb