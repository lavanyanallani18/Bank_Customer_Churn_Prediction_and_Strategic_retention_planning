# **Customer Churn Prediction and Strategic Retention Planning in Banking**

## **Overview**

Customer retention is a top priority in the banking industry, where losing clients can result in significant revenue loss. As a **Data Analyst**, I led the end-to-end analysis and modeling workflow to build a predictive system that helps banks proactively identify customers likely to churn.

By analyzing behavioral and financial attributes using Python-based tools, I supported the creation of actionable business insights and data-driven strategies to reduce attrition and improve customer lifetime value.

<p align="center">
  <img src="https://github.com/lavanyanallani18/project_images/blob/3d82fc4621703aaf8b3ea9ed1a820d7e66e56678/customer%20churn.png" width="700" height="400"/>
</p>


---

## **Problem Statement**

Traditional churn mitigation strategies are reactive and often miss early signs of customer dissatisfaction. My goal was to design a predictive analytics solution that allows banks to:

* Detect potential churners early using historical customer data.
* Understand which features (e.g., balance, tenure, product usage) drive churn.
* Recommend interventions based on patterns discovered in the data.

---

## **Role and Responsibilities**

As the Data Analyst on this project, I was responsible for:

* Conducting exploratory data analysis (EDA) to uncover trends and risks.
* Engineering features to capture underlying churn behavior.
* Preprocessing and preparing data for machine learning.
* Evaluating model performance and interpreting results.
* Translating outputs into strategic business recommendations.

---

## **Dataset Summary**

* **Source:** Bank Customer Churn Dataset
* **Size:** 10,000 customer records
* **Target Variable:** `Exited` (1 = Churned, 0 = Retained)

### **Key Attributes**

* **Demographics:** Age, Gender, Geography
* **Financials:** Credit Score, Balance, Estimated Salary
* **Behavioral:** Tenure, Number of Products, Credit Card Ownership, Active Membership

---

## **Exploratory Data Analysis (EDA)**

Key insights revealed:

* **Churn Rate:** \~20% of customers left, with imbalance in class distribution.
* **Age Impact:** Churn increases with customer age.
* **Zero Balance:** Customers maintaining zero balance were more likely to leave.
* **Membership Activity:** Inactive members churned at significantly higher rates.
* **Product Usage:** Low product usage correlated strongly with churn risk.

---

## **Feature Engineering**

As part of data preprocessing, I implemented:

* **Binary Flags:** For zero account balance.
* **Interaction Terms:** Between tenure, credit score, and balance.
* **Categorical Encoding:** Used one-hot encoding for features like geography and gender to make them machine learning-compatible.

---

## **Modeling & Evaluation**

I collaborated on training and tuning multiple classification models:

| **Model**              | **Accuracy** | **AUC Score** |
| ---------------------- | ------------ | ------------- |
| Random Forest          | **86.50%**   | **0.86**      |
| Support Vector Machine | 85.60%       | 0.83          |
| Logistic Regression    | 81.20%       | 0.78          |
| Decision Tree          | 78.15%       | 0.67          |

### **Optimization Techniques**

* Used **GridSearchCV** and **RandomizedSearchCV** for hyperparameter tuning.
* Evaluated performance using AUC, accuracy, and confusion matrix.
* Random Forest provided the best balance of performance and interpretability.

---

## **Top Features Influencing Churn**

| **Feature**            | **Importance** | **Business Impact**                            |
| ---------------------- | -------------- | ---------------------------------------------- |
| **Balance**            | 29.6%          | Signals disengagement or inactivity.           |
| **Credit Score**       | 25.3%          | Reflects financial reliability.                |
| **Active Membership**  | 18.2%          | Lack of engagement increases churn likelihood. |
| **Number of Products** | 15.4%          | More product usage correlates with loyalty.    |
| **Tenure**             | 8.1%           | Helps assess relationship maturity.            |

---

## **Key Business Recommendations**

Based on the insights and model outputs, I proposed the following strategies:

* **Flag At-Risk Customers:** Use churn scores to prioritize retention campaigns.
* **Engage Inactive Clients:** Personalized outreach and loyalty benefits.
* **Cross-Sell Products:** Encourage multi-product adoption for stronger engagement.
* **Reward Long-Term Customers:** Tailored offers to retain high-tenure clients.

---

## **Future Enhancements**

* **Live Model Deployment:** Integration with CRM systems for real-time prediction.
* **Richer Features:** Incorporate transactional patterns, feedback, and channel activity.
* **Model Monitoring:** Schedule periodic retraining and accuracy checks.
* **Explainable AI:** Use SHAP or LIME to visualize churn explanations per customer.

---

## **Conclusion**

This project demonstrates how data-driven insights can significantly enhance customer retention in the banking sector. As the Data Analyst, I enabled actionable intelligence through a full pipeline—from EDA to model interpretation.

* **Random Forest** achieved the highest accuracy (86.50%) and strongest interpretability.
* Business teams can now proactively reduce churn risk using the model’s insights.
* The methodology is scalable, interpretable, and ready for deployment in real-world banking systems.

This work lays a strong foundation for smarter, proactive customer success strategies using the power of analytics.
