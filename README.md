# Explainable AI Framework for Bone Marrow Cancer Subtyping

![Project Status](https://img.shields.io/badge/Status-Active_Development-green) ![Python](https://img.shields.io/badge/Python-3.9%2B-blue) ![Bioinformatics](https://img.shields.io/badge/Focus-Genomics-red)

## 🧬 Project Overview
This repository hosts a machine learning framework designed to identify **molecular biomarkers** and predictive signatures in **Bone Marrow Cancers** (specifically Acute Myeloid Leukemia - AML). 

Unlike standard "Black Box" predictions, this project prioritizes **Explainable AI (XAI)**. It uses SHAP (Shapley Additive Explanations) values to deconvolute *why* a model classifies a patient as high-risk, mapping computational features back to biological mechanisms (e.g., T-cell exclusion or myeloid differentiation blocks).

**Key Objective:** To bridge the gap between high-accuracy ML predictions and biologically interpretable discoveries in hematological oncology.

---

## 🔬 Scientific Methodology

The pipeline is structured into four distinct computational modules:

### Module A: Data Acquisition & Curation
* **Source:** Gene Expression Omnibus (GEO) / TCGA.
* **Data Type:** Transcriptomic data (RNA-seq / Microarray) from bone marrow aspirates.
* **Target:** Datasets involving AML, MDS, and MPN, with a focus on immune infiltration and drug resistance.

### Module B: Preprocessing
* **Quality Control:** Normalization (TPM/RMA), Batch Correction, and Outlier detection.
* **Dimensionality Reduction:** PCA and t-SNE/UMAP for visualizing patient clusters and subtype separation.

### Module C: Machine Learning Classifiers
* **Models:** Random Forest, XGBoost, and Logistic Regression (Baseline).
* **Validation:** Stratified K-Fold Cross-Validation to ensure robust performance on unseen patients.

### Module D: Explainability (XAI)
* **Global Interpretation:** Identifying the top 20 "Driver Genes" across the entire cohort using SHAP summary plots.
* **Local Interpretation:** Analyzing individual patient "force plots" to understand specific drug resistance profiles.

---

## 🛠️ Tech Stack
* **Core Logic:** Python (Pandas, NumPy)
* **Machine Learning:** Scikit-Learn, XGBoost
* **Explainability:** SHAP, LIME
* **Visualization:** Seaborn, Matplotlib
* **Genomics (R):** GEOquery, Biobase (for data retrieval)

---

## 📅 Development Roadmap (Jan 2026 – May 2026)

- [ ] **Phase 1: Foundations (Jan)**
    - Environment setup (Anaconda/Jupyter).
    - Acquisition of primary AML dataset from GEO.
    - Initial data cleaning and EDA (Exploratory Data Analysis).

- [ ] **Phase 2: The Baseline (Feb)**
    - Implementation of PCA/t-SNE visualization.
    - Training of baseline Logistic Regression model.
    - Assessment of class imbalance.

- [ ] **Phase 3: The Model (March)**
    - Training of Ensemble Models (Random Forest/XGBoost).
    - Hyperparameter tuning.
    - Application of SHAP to generate feature importance rankings.

- [ ] **Phase 4: Interpretation (April/May)**
    - Biological enrichment analysis (Gene Ontology/KEGG) of top SHAP features.
    - Final report generation for the *Brunel Bioinformatics Symposium*.

---

## 📊 Preliminary Results
*(This section will be updated with PCA plots and SHAP summary charts as the project progresses).*

---

## 👤 Author
**Gabor Adorjani**
* *BSc Mathematics & Computer Science (Foundation), Brunel University London*
* **Focus:** Computational Oncology, XAI, Mathematical Biology.

---

## ⚠️ Disclaimer
*This project is for educational and research purposes only. It is not a clinical diagnostic tool.*
