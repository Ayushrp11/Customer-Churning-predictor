# Churn Data Analysis Project

## Overview
This project aims to analyze customer churn within a telecommunications dataset. The focus is on performing exploratory data analysis (EDA) and building predictive models to accurately classify customer churn.

## Files
- **EDA Script**: Contains code for performing data exploration and visualization.
- **Predictive Model Script**: Includes code for training and evaluating churn prediction models.

## Data Exploration and Insights
- The dataset comprises 7,043 customer records with 21 variables.
- A notable class imbalance was observed, with fewer churned customers compared to retained ones.
- Key factors contributing to churn:
  - **Higher churn rates**: Month-to-month contracts, absence of online security, no tech support, and customers in their first year of service.
  - **Lower churn rates**: Long-term contracts, no internet services, and customers with more than five years of tenure.
- Variables like gender, phone service availability, and multiple lines had minimal influence on churn likelihood.

## Data Cleaning and Preparation
- Data cleaning involved managing missing data and converting categorical variables into numerical ones for model training.
- Feature engineering, such as categorizing tenure, was performed to better understand churn patterns across different customer tenures.

## Model Development
- A Decision Tree Classifier was initially applied for churn prediction, but it showed lower accuracy due to the dataset's imbalance.
- The SMOTEENN method was used to balance the classes by oversampling the minority class (churned customers), improving model performance.
- A Random Forest Classifier was then implemented, yielding better accuracy and recall for predicting churn compared to the Decision Tree model.

## Performance Evaluation
- Model performance was assessed using precision, recall, F1 score, and accuracy metrics. The Random Forest model with SMOTEENN provided the best performance, achieving around 92% accuracy.
- Additional tests with PCA showed potential benefits of dimensionality reduction, but they did not outperform the Random Forest model.

## Model Deployment
- The final model (Random Forest Classifier with SMOTEENN) was serialized using pickle, ready for deployment in a production environment with API access for real-time churn predictions.

## Future Work
- Test alternative classification algorithms to further improve model performance.
- Incorporate additional features, such as customer engagement metrics, for a more in-depth churn analysis.
- Implement a monitoring system to track the model's performance in production, ensuring ongoing accuracy.

## Conclusion
This project provides a strong foundation for understanding and predicting customer churn, offering valuable insights for telecommunications companies to improve retention strategies.