# Loan Default Risk by Demographics & Finance

## Project Overview

This project analyzes loan default risks by leveraging demographic and financial data. By identifying key patterns, it supports financial institutions in making informed lending decisions while promoting financial inclusion.

**Authors:** Viet Nguyen, Chien Tran, Ricky Xiong  
**Date:** December 14, 2024  

## Motivation

Many individuals lack traditional credit histories, creating challenges in accessing loans. This project utilizes advanced data analytics to provide financial institutions with actionable insights, reducing default risks and enhancing financial accessibility.

## Dataset

The data originates from the Home Credit Default Risk dataset on Kaggle. It includes 307,511 observations from six countries (Kazakhstan, Russia, Vietnam, China, Indonesia, and the Philippines) with 122 variables such as:

- Demographics
- Financial information
- Employment status
- Housing characteristics
- Credit bureau inquiries

The target variable indicates whether a client had payment difficulties.

## Methodology

1. **Data Cleaning and Preprocessing**
   - Handling missing values using imputation.
   - Removing irrelevant or highly correlated variables.
   - Engineering features based on domain knowledge.

2. **Exploratory Data Analysis**
   - Analyzed repayment patterns by education, income, age, and credit ranges.
   - Visualized relationships between features and loan defaults.

3. **Feature Selection**
   - Applied Elastic Net regression to select significant variables.
   - Used Principal Component Analysis (PCA) to reduce dimensionality.

4. **Modeling**
   - Built predictive models using machine learning techniques.
   - Evaluated models with precision-focused metrics to address class imbalance.

## Key Insights

- Higher education levels correlate with better loan repayment behavior.
- Younger age groups (18–25) face repayment difficulties due to limited financial stability.
- Clients with higher income and credit amounts exhibit better repayment rates.

## Tools & Libraries

The project is implemented in R, utilizing the following libraries:
- **Data Manipulation:** `tidyverse`, `dplyr`
- **Visualization:** `ggplot2`, `ggthemes`
- **Modeling:** `caret`, `glmnet`, `randomForest`, `xgboost`
- **Evaluation:** `pROC`, `gtsummary`

## Ethical Considerations

- Ensuring privacy and confidentiality for individuals in the dataset.
- Avoiding bias in the analysis to support fair lending practices.
- Highlighting the importance of responsible and inclusive financial decision-making.

## Usage

Clone the repository and install required R packages to run the project. The data preprocessing and analysis steps are provided in R scripts.

```bash
git clone <repository_url>
```

Run the main R script to reproduce the analysis.

## Future Work

- Experiment with additional machine learning models.
- Investigate the impact of cultural and regional factors on loan repayment behavior.
- Develop a web-based dashboard for real-time risk assessment.

## References

- [Home Credit Default Risk Dataset](https://www.kaggle.com/c/home-credit-default-risk)

