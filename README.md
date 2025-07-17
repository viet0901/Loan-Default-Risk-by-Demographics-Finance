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

* We initially observed a high number of correlated variables, so we used a **correlation matrix with a threshold of 0.8** to eliminate redundancy. Highly correlated pairs like `AMT_CREDIT` & `AMT_GOODS_PRICE` and `REGION_RATING_CLIENT` & `REGION_RATING_CLIENT_W_CITY` helped identify key financial and regional patterns. Some redundant variables, like the social circle delinquency counters, were removed for clarity.
* After removing redundancy, we applied **Principal Component Analysis (PCA)** to reduce 122 features to **31 uncorrelated components** while preserving over **94% of the total variance** in the dataset.
* The most influential components—**PC13**, **PC5**, and **PC2**—captured dimensions related to employment history, financial health, and regional credit behavior.
* **Logistic Regression** achieved the highest test accuracy (**70.5%**), outperforming more complex models like XGBoost (66.9%) and Random Forest (66.5%).
* **EXT\_SOURCE\_2**, **EXT\_SOURCE\_3**, and **DAYS\_EMPLOYED** appeared prominently in top PCs, confirming their predictive strength.
* Younger borrowers (age **18–25**) showed **elevated default rates**, while higher income and education levels were consistently associated with successful repayment.

---

### ✨ Recommendations

* Use **correlation filtering and PCA** as a scalable strategy for reducing multicollinearity and model complexity in large, high-dimensional datasets.
* Favor **simple, interpretable models** like Logistic Regression when principal components already capture key variation—especially in regulated environments like credit scoring.
* Prioritize **external credit scores** and **employment duration** when designing loan approval criteria, as these features were consistently strong predictors across models.
* Tailor lending strategies to **younger applicants**, offering educational tools or safeguards, given their higher risk profiles.
* Expand the dataset geographically and **periodically retrain** models to reflect evolving financial behavior and economic trends for stronger generalization.
* Begin integrating **fairness-aware machine learning practices**, especially when demographic data like age or region contribute significantly to predictions.

---

### 📚 References

* [Home Credit Default Risk Dataset (Kaggle)](https://www.kaggle.com/c/home-credit-default-risk)

---

### 📬 Contact

Viet Nguyen: [nguyen\_v5@denison.edu](mailto:nguyen_v5@denison.edu)

Chien Tran: [tran\_c3@denison.edu](mailto:tran_c3@denison.edu)

Ricky Xiong: [xiong\_r1@denison.edu](mailto:xiong_r1@denison.edu)
