# **Customer Churn Prediction and Strategic Retention Planning in Banking**

## **Overview**

Customer churn is one of the biggest profitability challenges in the banking sector. Acquiring new customers is far more expensive than retaining existing ones. By identifying at-risk customers early, banks can intervene with targeted strategies to improve retention.

This project applies supervised machine learning techniques to predict customer churn based on demographic, financial, and behavioral data. The goal is to help financial institutions understand the drivers of churn and develop data-driven strategies to retain valuable customers.

---

## **Problem Statement**

Banks face difficulty in predicting which customers are likely to leave and why. Without predictive insights, they rely on reactive strategies that are often too late.

This project addresses this gap by:

* Predicting churn risk based on historical customer data.
* Identifying key drivers of churn (e.g., balance, credit score, tenure).
* Recommending proactive strategies to reduce churn and improve engagement.

---

## **Dataset and Features**

* **Dataset Source:** Internal banking dataset (10,000 records)
* **Target Variable:** `Exited` (1 = Churned, 0 = Retained)

**Feature Categories:**

* **Demographics:** `Geography`, `Gender`, `Age`
* **Financial Data:** `CreditScore`, `Balance`, `EstimatedSalary`
* **Banking Behavior:** `Tenure`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`

---

## **Exploratory Data Analysis (EDA)**

Key insights discovered during EDA:

* **Churn Rate:** Around 20% of customers churned.
* **Age:** Older customers were more likely to leave.
* **Balance:** Customers with zero balance were highly represented among churners.
* **Active Membership:** Inactive customers were 2x more likely to churn.
* **Product Usage:** Customers with only 1 product had a significantly higher churn rate.

---

## **Feature Engineering**

To improve predictive power:

* **Zero Balance Flag:** Binary feature indicating customers with no account balance.
* **Interaction Terms:** Between tenure, credit score, and balance.
* **One-Hot Encoding:** For categorical variables like geography and gender.

---

## **Model Development and Evaluation**

Four classification models were tested and evaluated on performance:

| **Model**              | **Accuracy** | **AUC Score** |
| ---------------------- | ------------ | ------------- |
| Random Forest          | **86.50%**   | **0.86**      |
| Support Vector Machine | 85.60%       | 0.83          |
| Logistic Regression    | 81.20%       | 0.78          |
| Decision Tree          | 78.15%       | 0.67          |

### **Hyperparameter Optimization**

Performed using GridSearchCV and RandomizedSearchCV to improve model accuracy:

* **Random Forest:** Tuned `n_estimators`, `max_depth`, and `min_samples_split`.
* **SVM:** Tuned `C`, `gamma`, and kernel types.
* **Logistic Regression:** Adjusted regularization strength.

Random Forest outperformed all other models in terms of both accuracy and AUC.

---

## **Feature Importance Analysis**

From the Random Forest model:

| **Top Features**   | **Importance (%)** | **Reason**                                        |
| ------------------ | ------------------ | ------------------------------------------------- |
| **Balance**        | 29.6%              | High or zero balances often signal disengagement. |
| **CreditScore**    | 25.3%              | Low scores reflect financial instability.         |
| **IsActiveMember** | 18.2%              | Inactive members are more prone to churn.         |
| **NumOfProducts**  | 15.4%              | Limited product usage signals weak engagement.    |
| **Tenure**         | 8.1%               | Mid-tenure users may be considering switching.    |

---

## **Business Insights & Recommendations**

* **Early Intervention:** Use churn probabilities to trigger retention workflows.
* **Customer Segmentation:** Target customers with low activity and single-product usage.
* **Product Bundling:** Cross-sell products to increase engagement and stickiness.
* **Incentives:** Offer personalized rewards to customers flagged as high-risk.
* **Loyalty Programs:** Reinforce long-term commitment with milestone benefits.

---

## **Future Scope**

* **Real-Time Prediction:** Deploy model for live churn detection in CRM.
* **Add Behavioral Data:** Include digital activity and service feedback.
* **Model Retraining:** Schedule regular updates using fresh customer data.
* **Advanced Modeling:** Explore XGBoost, deep learning, and SHAP interpretability.

---

## **Conclusion**

This end-to-end customer churn prediction project provides banks with actionable insights to combat attrition. Using machine learning, we were able to:

* Identify churn-prone customers with \~86% accuracy.
* Understand key churn factors like balance, credit score, and activity level.
* Recommend data-driven strategies for retention and customer success.

This predictive solution equips banks with a powerful tool for improving loyalty and reducing customer acquisition costs.
