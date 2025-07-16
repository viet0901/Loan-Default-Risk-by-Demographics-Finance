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

* Imputed missing values, dropped redundant features
* Explored trends across income, education, and age

**Feature Selection & Dimensionality Reduction**

* Applied Elastic Net to select relevant features
* Used PCA to reduce 122 variables into 25 components

**Modeling & Evaluation**

* Trained Logistic Regression, Random Forest, and XGBoost
* Focused on **precision** due to class imbalance
* Interpreted top principal components using loading analysis

---

### 📈 Key Findings

* **Logistic Regression** achieved the highest precision (0.467)
* **EXT\_SOURCE\_2**, **EXT\_SOURCE\_3**, and **DAYS\_EMPLOYED** were top predictors
* **PC12** and **PC2** had strong influence across all models
* Higher education and income correlated with timely repayment
* Young borrowers (18–25) had highest default rates

---

### ✨ Recommendations

* Leverage simple, interpretable models (e.g. Logistic Regression) for credit assessment
* Prioritize external credit sources and employment history in scoring models
* Expand data collection to better support fairness-aware modeling
* Design lending strategies that consider borrower age and education status

---

### 📚 References

* [Home Credit Default Risk Dataset (Kaggle)](https://www.kaggle.com/c/home-credit-default-risk)

---

### 📬 Contact

Viet Nguyen: [nguyen\_v5@denison.edu](mailto:nguyen_v5@denison.edu)
Chien Tran: [tran\_c3@denison.edu](mailto:tran_c3@denison.edu)
Ricky Xiong: [xiong\_r1@denison.edu](mailto:xiong_r1@denison.edu)
