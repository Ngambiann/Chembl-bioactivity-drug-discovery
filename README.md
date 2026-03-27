# ChEMBL Bioactivity Analysis for Drug Discovery

## 📌 Overview

This project builds a data analysis pipeline for small-molecule drug discovery using bioactivity data from the ChEMBL. It demonstrates how raw experimental data can be transformed into meaningful features for downstream analysis and machine learning.

## ⚙️ Objectives

* Retrieve bioactivity data for a selected protein target
* Clean and preprocess experimental IC50 values
* Convert IC50 to pIC50 (log scale)
* Generate molecular descriptors using RDKit
* Perform exploratory data analysis (EDA)

## 🧪 Workflow

### 1. Data Collection

* Queried ChEMBL API for target-specific bioactivity data
* Extracted compound IDs, SMILES, and activity values

### 2. Data Preprocessing

* Removed missing values
* Standardized IC50 values
* Classified compounds into:

  * Active
  * Inactive
  * Intermediate

### 3. Feature Engineering

* Converted IC50 → pIC50 using log transformation
* Computed Lipinski descriptors:

  * Molecular Weight (MW)
  * LogP
  * Hydrogen Bond Donors
  * Hydrogen Bond Acceptors

### 4. Exploratory Data Analysis(EDA)

* Distribution analysis of bioactivity classes
* Descriptor relationships
* Identification of trends in drug-likeness

## 🧰 Tools & Libraries

* Python
* pandas
* numpy
* RDKit
* matplotlib / seaborn

## 📂 Project Structure

```
│
├── data/
│   ├── raw/                # Original downloaded CSVs
│   └── processed/          # Cleaned, normalized CSVs (used for analysis)
│
├── notebooks/
│   ├── 01_data_collection.ipynb   # Data collection + cleaning + pre-processing
│   ├── 02_exploratory_data_analysis.ipynb   #  pIC50 + Lipinski + EDA + plots + stats
│
├── results/                # final plots and stats
│   ├── plots/
│   └── stats/
│
│
├── README.md
└── requirements.txt        # Python packages needed

```

## 📊 Key Concepts Demonstrated

* Bioactivity data analysis
* Feature engineering in cheminformatics
* Log transformation (pIC50)
* Lipinski's Rule of Five

## 🚀 Future Improvements

* Build QSAR models for activity prediction
* Apply machine learning classification/regression
* Generate molecular fingerprints
* Visualize chemical structures

## 📎 Notes

This project is part of a computational biology learning pathway focused on drug discovery and data-driven analysis by Channin Nantasenamat AKA the DataProfessor on his youtube platform.cle