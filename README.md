# Bank Marketing Success Prediction: A State-of-the-Art ML Approach

![Python](https://img.shields.io/badge/python-3.13-blue.svg)
![CatBoost](https://img.shields.io/badge/CatBoost-Winner-yellow.svg)
![Poetry](https://img.shields.io/badge/poetry-dependency%20manager-blueviolet)

## Project Overview
Direct marketing remains a cornerstone for banking institutions to promote term deposits. However, unsolicited phone calls incur significant operational costs and risk customer dissatisfaction. 
This project develops a highly accurate predictive model to identify customers with a high probability of conversion, comparing our findings to existing literature benchmarks (Moro et al.).

## Business Impact & ROI
By optimizing the targeting process, the bank can maximize successful deposits while drastically reducing unnecessary contacts.
* **Lift Score:** 4.83 at the top 10% of the high-priority population.
* **Efficiency:** The bank can capture nearly half (48.28%) of all total deposits by contacting only 10% of its client base.

## Modeling & Performance
A multi-algorithmic framework was evaluated using rigorous 5-fold Stratified Cross-Validation to address severe class imbalance (89% 'no' vs 11% 'yes'). The models included Logistic Regression, SVM, KNN, Random Forest, and CatBoost.

* **Winning Model:** CatBoost (Gradient Boosting Decision Tree).
* **CatBoost Final Test AUC:** 0.8157 (Surpassing the 0.794 neural network benchmark).
* **Key Drivers:** Euribor 3m Rate, Education, and Campaign intensity emerged as the most critical predictors.
* **Data Leakage Prevention:** The `duration` variable was explicitly excluded to prevent data leakage, aligning with real-world deployment constraints.

## Tech Stack
* **Language:** Python 3.13
* **Environment Management:** Poetry
* **Libraries:** scikit-learn, CatBoost, pandas, matplotlib, seaborn
* **Preprocessing:** StandardScaler, OneHotEncoder

 

## How to Run Locally

This project uses `Poetry` for dependency management, ensuring a fully reproducible environment.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/GZempilis/Bank-Marketing.git](https://github.com/GZempilis/Bank-Marketing.git)
   cd Bank-Marketing

2. **Download the Data:**
   Download the "Bank Marketing" dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing) and make sure to use **`bank-additional-full.csv`** (the full dataset version used in this project), placing it inside a `data/` directory in the project root.


** For detailed academic analysis check the **`Report/ML_Project_2.pdf`**
