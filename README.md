## Loan Default Risk by Demographics & Finance

**Team:** Viet Nguyen, Chien Tran, Ricky Xiong

---

### 🔍 Overview

This project evaluates how demographic and financial factors influence loan default risk. Using data from the Home Credit competition on Kaggle, we identified patterns tied to repayment behavior and built models to help lenders assess creditworthiness more equitably—especially for underbanked populations.

---

### 🗂 Project Structure

```
.
├── data/               # Raw training and testing datasets
├── dictionary/         # Variable descriptions
├── markdown/           # RMarkdown notebook for full analysis
├── model/              # Saved model objects (Elastic Net, XGB, RF)
├── presentation/       # Final slides
├── report/             # HTML report of results
└── README.md           # Project summary and documentation
```

---

### ⚙️ Methodology

**Data Preprocessing & EDA**

* Imputed missing values and removed redundant or low-variance features
* Explored trends across income, education, and employment characteristics

**Dimensionality Reduction**

* Applied **Principal Component Analysis (PCA)** to reduce 122 features to 31 principal components
* Standardized features before PCA to ensure consistent scale and variance contribution

**Modeling & Evaluation**

* Trained **Logistic Regression**, **Random Forest**, and **XGBoost** models using down-sampled training sets to address class imbalance
* Evaluated models using **accuracy** via 10-fold cross-validation
* Interpreted top principal components using loadings and regression coefficients to understand key drivers of loan repayment behavior

---

### 📈 Key Findings

* **Logistic Regression** achieved the highest test accuracy (**70.5%**), outperforming Random Forest (66.5%) and XGBoost (66.9%)
* **EXT\_SOURCE\_2**, **EXT\_SOURCE\_3**, and **DAYS\_EMPLOYED** were among the most influential variables in the top principal components
* **PC13**, **PC5**, and **PC2** were the most important components across all models, reflecting employment status, financial profile, and regional credit behavior
* Borrowers with **higher income and education** levels were more likely to repay loans on time
* **Young borrowers (18–25)** showed the highest default rates, indicating elevated credit risk in this group

---

### ✨ Recommendations

* Prioritize **simple, interpretable models** like Logistic Regression for efficient and effective credit risk modeling
* Emphasize **external credit scores** and **employment history** as key features in risk scoring systems
* Expand the dataset to include **broader geographic regions** for better generalization across borrower populations
* Integrate **fairness-aware machine learning** techniques to reduce unintended bias from demographic variables
* Tailor lending strategies to account for **borrower age and education**, especially for younger individuals with limited credit history

---

### 📚 References

* [Home Credit Default Risk Dataset (Kaggle)](https://www.kaggle.com/c/home-credit-default-risk)

---

### 📬 Contact

Viet Nguyen: [nguyen\_v5@denison.edu](mailto:nguyen_v5@denison.edu)

Chien Tran: [tran\_c3@denison.edu](mailto:tran_c3@denison.edu)

Ricky Xiong: [xiong\_r1@denison.edu](mailto:xiong_r1@denison.edu)
