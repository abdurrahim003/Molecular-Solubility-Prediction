# Predicting Molecular Solubility of Organic Molecules Using Machine Learning

## Overview
This project uses machine learning to predict the aqueous solubility (LogS) of organic molecules based on their molecular descriptors. Solubility prediction is crucial in drug design, environmental science, and chemical engineering.

## Dataset
- **Name:** AqSolDB — A curated aqueous solubility dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/sorkun/aqsoldb-a-curated-aqueous-solubility-dataset)
- **Size:** 9,982 unique organic molecules
- **Features:** 17 molecular descriptors (MolWt, MolLogP, TPSA, NumHDonors, etc.)
- **Target:** Aqueous solubility (LogS in mol/L)
- **Reference:** Sorkun, M.C., Khetan, A. & Er, S. *Scientific Data* 6, 143 (2019)

## Models and Results

| Model | R² Score | RMSE | MAE |
|-------|----------|------|-----|
| Linear Regression | 0.4955 | 1.6543 | 1.2127 |
| **Random Forest** | **0.7831** | **1.0846** | **0.7485** |
| Gradient Boosting | 0.7783 | 1.0966 | 0.7702 |

**Best Model:** Random Forest (R² = 0.78, MAE = 0.75 LogS units)

**Cross-Validation:** 5-Fold Mean R² = 0.7051 ± 0.1260

## Key Findings
- **MolLogP** (lipophilicity) is the strongest predictor of solubility (importance = 0.649)
- Non-linear models significantly outperform Linear Regression
- Molecular size (MolWt) and complexity (BertzCT) are secondary predictors
- Hydrogen bond donors improve water solubility

## Top 5 Feature Importance (Random Forest)
1. MolLogP — 0.6490
2. BertzCT — 0.0739
3. MolWt — 0.0462
4. BalabanJ — 0.0437
5. MolMR — 0.0386

## Tools Used
- **Language:** Python
- **Libraries:** pandas, NumPy, Matplotlib, Seaborn, scikit-learn
- **Platform:** Kaggle Notebooks

## Kaggle Notebook
[View the full notebook on Kaggle](https://www.kaggle.com/code/abdurrahim003/predicting-molecular-solubility-using-ml)

## Author
**Abdur Rahim**
B.Sc. in Chemistry, Gopalganj Science and Technology University (GSTU), Bangladesh

- Kaggle: [abdurrahim003](https://www.kaggle.com/abdurrahim003)
- GitHub: [abdurrahim003](https://github.com/abdurrahim003)
