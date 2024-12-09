  
**Introduction.**  
Telecom companies face the critical challenge of addressing customer churn to ensure consistent service delivery and maintain a competitive edge. This effort aims to provide seamless access to services while minimizing disruptions caused by customer attrition. However, predicting the likelihood of churn, especially among customers with variable usage patterns, remains a challenge. Developing an accurate churn prediction model can enhance retention strategies by identifying at-risk customers, tailoring interventions to improve customer satisfaction, and prioritizing support for the most vulnerable segments.

**Business Understanding.**   
The primary goal of this project is to develop a model that predicts customer churn for a telecom company. This involves analyzing customer demographics, location, usage patterns, and service preferences to understand their impact on churn predictions.

**Problem Statement.**

Telecom customer churn is a critical issue that can lead to significant revenue loss for service provider institutions. Understanding why customers leave the telecom service provider and predicting which customers are at risk of churning enables the telecom service provider to take proactive measures to retain customers. In this project I aim to predict customer churn using a machine learning model.

**Objectives.**

* **Main objective.**  
  Develop a machine learning model to predict customer churn.  
    
* **Specific Objectives.**  
1. Conduct Exploratory Data Analysis (EDA) to understand the distribution and relationships of various features and identify patterns associated with customer churn.  
2. Achieve high accuracy and recall to minimize false negatives (missed churners).  
3. Provide actionable insights for stakeholders to reduce churn rates.

**Metrics of Success**

* Accuracy Score: ≥ 85%  
* Recall Score: ≥ 80%

**Data Preparation and Cleaning.**

Data preparation involves handling missing values, normalizing features, and encoding categorical variables to ensure the dataset is ready for model training. Key steps include:

* Dropping irrelevant columns.  
* Imputing missing values.  
* Encoding categorical variables.  
* Scaling numerical features for consistency.


**Exploratory Data Analysis(EDA)**

**Key Insights**

* **Churn Distribution.**  
         ![Churn Pie chart](https://raw.githubusercontent.com/Delvinah/Phase_3_project./main/download%20(4).png)
  This pie chart illustrates the frequency distribution of the churn rate in our dataset. Out of 3333 customers in our dataset 483 customers have churned which is represented by 14.5%.  
* **International plan distribution**
      ![Internatinal plan bar chart](https://github.com/Delvinah/Phase_3_project./blob/main/download%20(5).png)
  This bar chart shows the frequency distribution of customers' international plan subscriptions. Out of 3333 customers in our dataset only 323 have subscribed to an international plan.

* **Location Distribution.**

  ![Location bar chart](https://github.com/Delvinah/Phase_3_project./blob/main/download%20(6).png)

The bar chart depicts the distribution of regions where customers are using telecom services. Area code 415 has the highest frequency of customers, followed by area code 510 and area code 408\. 

* **Distribution across different numeric features**  
  ![numeric distribution histogram](https://github.com/Delvinah/Phase_3_project./blob/main/download%20(7).png)


**Customer Behavior Consistency:** Most features, including total minutes, calls, and charges across various time periods (day, evening, and night), exhibit normal or symmetric distributions. This indicates consistent usage patterns among customers.

**Voicemail Usage:** Voicemail usage is notably sparse, with a significant number of customers not utilizing this service at all.

**Proportional Relationships:** The charges are directly proportional to the usage minutes across all categories, reflecting the billing structure of the service.

* **Total day charges vs churn**  
    ![Histogram](https://github.com/Delvinah/Phase_3_project./blob/main/download%20(9).png)
  This graph shows that churned customers are slightly more likely to have higher total day charges compared to non-churned customers. This could indicate that customers with higher usage (and charges) might be more prone to churn.  
  


**Modeling**

**Models used:**

* Logistic regression  
* Decision trees

**Evaluation**

Three models—a baseline Decision Tree, a hyperparameter-tuned Decision Tree, and Logistic Regression—were assessed for their ability to forecast customer attrition. Although it showed indications of overfitting, the baseline Decision Tree was able to capture churn cases with an accuracy of 100% which showed overfitting of training data. Although it struggled with non-linear interactions in the dataset, logistic regression produced more consistent predictions with an accuracy of 75% and a recall of 73%. These early models shed light on the main predictive characteristics and the structure of the dataset.

The best-performing model was the hyperparameter-tuned Decision Tree, which had an accuracy of 87%, a recall of 80%, and a ROC-AUC of 85%. The enhanced performance shows that it can mitigate overfitting problems observed in the baseline while striking a balance between recall and precision.

The best-performing model was the hyperparameter-tuned Decision Tree, which had an accuracy of 87%, a recall of 84%, and a ROC-AUC of 87.97%. The enhanced performance shows that it can mitigate overfitting problems observed in the baseline while striking a balance between recall and precision. This model is the best option for deployment to detect and proactively retain at-risk consumers since it captures non-linear interactions efficiently.

**Recommendations.**

* **Target High-Risk Customers:** Based on the model’s findings, prioritize retention efforts for customers with a high number of customer service calls. These customers may be facing issues with the service, and offering proactive support or incentives could help retain them.  
* **Review the International Plan:** Customers with an international plan showed a higher likelihood of churning. Consider offering tailored retention packages, such as discounts, additional features, or personalized customer support, to keep these customers engaged.  
* **Personalized Engagement:** Use the churn prediction model to segment customers based on their likelihood to churn. Develop targeted marketing campaigns and personalized offers to these high-risk segments, focusing on improving customer satisfaction and loyalty.  
* **Improve Customer Service Experience:** Since high customer service calls correlate with churn, addressing root causes of customer dissatisfaction (e.g., service reliability, billing issues) could help reduce churn rates. Implementing better self-service options or enhancing customer support may also alleviate frequent interactions.

**Limitations**

Although the model is effective at forecasting customer attrition, there are a number of drawbacks to take into account. First, it's possible that not all pertinent churn-influencing elements were included in the dataset used to train the models. For instance, although they were not considered in the investigation, outside variables such as consumer sentiment, market competitiveness, and economic conditions may have an effect. Furthermore, there are more non-churners in the dataset than churners, which can make it more difficult for the model to forecast churn for smaller classes. In comparison to other sophisticated models like random forests or gradient boosting, the Decision Tree still has limits when it comes to managing more complex relationships, even though its performance was enhanced via hyperparameter tuning. 

**Conclusions**

Key elements that impact customer churn, like customer service encounters and the use of international plans, have been effectively identified by the churn prediction project. Particularly after hyperparameter tuning, the Decision Tree model had the highest efficacy in identifying these trends and accurately forecasting churn. The business can use this model to identify clients who are at risk and target them with customized retention measures. Even though the model works well in the current situation, its accuracy will need to be maintained through continuous data collecting and model retraining. To lower churn, enhance customer retention, and boost overall happiness, the business should take proactive measures by concentrating on the factors that have been identified as predictors of churn, such as high customer care calls and international plan usage.
