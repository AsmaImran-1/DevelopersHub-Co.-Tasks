# Data Science Internship Tasks: Machine Learning Projects

This repository contains solutions for three core data science tasks, demonstrating proficiency in data manipulation, exploratory data analysis (EDA), visualization, and supervised machine learning classification.

***

## Task 1: Exploring and Visualizing a Simple Dataset (Iris)

| Section | Description |
| :--- | :--- |
| **Dataset** | Iris Dataset (available via `seaborn`) |
| **Skills Used** | Pandas for loading/inspection, Matplotlib/Seaborn for visualization. |

### 🎯 Objective
To understand the fundamentals of data handling, summarization, and basic visualization techniques.

### 💡 Approach
1.  **Inspection:** Used `.shape`, `.columns`, and `.head()` to inspect the dataset structure.
2.  **Visualization:** Generated key plots to summarize the data:
    * **Scatter Plots:** To analyze the relationship between features (e.g., petal length vs. petal width) and species separation.
    * **Histograms:** To show the distribution of individual features (e.g., sepal length).
    * **Box Plots:** To identify outliers and compare the spread of values across species.

### 📊 Results and Insights
* **Separation:** Visualizations clearly showed that the **Setosa** species is easily distinguishable from the others.
* **Key Features:** **Petal Length** and **Petal Width** were confirmed as the most effective features for classification, as their distributions show minimal overlap between species.

***

## Task 2: Credit Risk Prediction (Loan Prediction Dataset)

| Section | Description |
| :--- | :--- |
| **Dataset** | Loan Prediction Dataset (Kaggle) |
| **Skills Used** | Data imputation, EDA, Logistic Regression/Decision Tree, Model Evaluation. |

### 🎯 Objective
To build a classification model that predicts whether a loan applicant is likely to default on a loan (i.e., predict the Loan Status).

### 💡 Approach
1.  **Data Cleaning:** Handled missing data using appropriate imputation methods (e.g., mode for categorical features, mean/median for numerical features).
2.  **EDA:** Visualized the relationship between key variables (`Education`, `ApplicantIncome`, `Credit_History`) and the target variable.
3.  **Modeling:** Trained a **Logistic Regression** classifier.
4.  **Evaluation:** Measured performance using **Accuracy** and a **Confusion Matrix**.

### 📊 Results and Insights
* **Accuracy:** Achieved an overall classification accuracy (e.g., $\approx 80\%$ depending on model choice and tuning).
* **Confusion Matrix:** Provided a clear view of **True Positives** (correctly approved loans) and **False Negatives** (safe applicants incorrectly rejected).
* **Key Predictors:** **Credit History** was identified as the single most critical factor, followed by Applicant Income and Loan Amount.

***

## Task 3: Customer Churn Prediction (Bank Customers)

| Section | Description |
| :--- | :--- |
| **Dataset** | Churn Modelling Dataset (kaggle) |
| **Skills Used** | One-Hot Encoding, Feature Scaling, Random Forest, Feature Importance Analysis. |

### 🎯 Objective
To build a predictive model to identify high-risk customers who are likely to leave the bank and analyze the factors influencing churn.

### 💡 Approach
1.  **Data Preparation:** Removed irrelevant columns and applied **Standard Scaling** to numerical features.
2.  **Encoding:** Used **One-Hot Encoding** to convert categorical features (`Geography`, `Gender`) into numerical format.
3.  **Modeling:** Trained a **Random Forest Classifier** with `class_weight='balanced'` to address the class imbalance ($20\%$ churn rate).
4.  **Evaluation:** Used **Accuracy**, **Classification Report**, and analyzed **Feature Importance**.

### 📊 Results and Insights
* **Performance:** Achieved an overall **Accuracy of $86.05\%$**. However, the **Recall for the Churn Class (1) was $0.44$** (44%), indicating that the model missed a significant number of actual churners.
* **Key Churn Drivers (Feature Importance):**
    1.  **Age:** The most critical predictor, suggesting older customers are at higher risk.
    2.  **NumOfProducts:** Low or excessively high product count strongly correlates with churn.
    3.  **Balance:** High account balances, especially when combined with low engagement, are a risk sign.
    4.  **Geography (Germany):** Customers in Germany show a statistically higher likelihood of leaving.
    5.  **IsActiveMember:** Customer inactivity is a strong indicator of impending churn.

**Conclusion:** The bank should focus retention efforts on older, non-active customers, particularly in Germany. Future modeling efforts should prioritize improving **Recall** using techniques like SMOTE or probability threshold adjustment.
