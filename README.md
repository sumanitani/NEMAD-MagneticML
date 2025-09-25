# NEMAD-MagneticML
# Magnetic Materials Machine Learning Models

This repository contains machine learning models and datasets for predicting and classifying magnetic material properties, including **Curie temperature prediction**, **Néel temperature prediction**, and **magnetic phase classification**.



## Usage Instructions

### 1. Feature Generation  
For **new datasets**, generate features before applying models:  
Feature_Engineering/feature_generator_from_chemical_composition.ipynb
This notebook creates descriptors such as elemental proportion vectors, atomic weights, electronegativity, etc., which are required by all models.

---

### 2. Classification Models  
- **Notebooks**: `Classification_Models/Classification_RF.ipynb`, `XGB_classification.ipynb`  
- **Dataset**: `Dataset/Classification_FM_AFM_NM.csv`  
- **Task**: Classify compounds into **FM** (ferromagnetic), **AFM** (antiferromagnetic), or **NM** (non-magnetic).

---

### 3. Curie Temperature Prediction  
- **Notebooks**: `Curie_Temperature_Prediction_Models/ENN_balanced.ipynb`, `Random_forest_balanced.ipynb`, `XGBoost_with_balanced_data.ipynb`  
- **Dataset**: `Dataset/FM_with_curie.csv`  
- **Task**: Predict Curie temperature (`Mean_TC_K`) for ferromagnetic materials.

---

### 4. Néel Temperature Prediction  
- **Notebooks**: `Neel_Temperature_Prediction_Models/ENN_Neel_balanced_data.ipynb`, `RF_neel_balanced_data.ipynb`, `XGB_Neel_balanced_data.ipynb`  
- **Dataset**: `Dataset/AFM_with_Neel.csv`  
- **Task**: Predict Néel temperature for antiferromagnetic materials.

---

## Installation & Requirements

To run the notebooks, install the following:

- Python ≥ 3.8  
- [Jupyter Notebook or JupyterLab](https://jupyter.org/)  

### Core Packages
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

For notebooks with ENN (Ensemble Neural Network) in their name, you will also need TensorFlow and Keras:
pip install tensorflow keras
