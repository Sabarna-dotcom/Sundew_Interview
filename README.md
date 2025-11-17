

# **Insurance Cost Prediction – Machine Learning Project**

This project focuses on predicting the insurance cost for an individual using health, lifestyle and medical history parameters.
The goal is to use data-driven techniques so that the insurance company can estimate an optimal premium while minimizing financial risk.
Customers also benefit through fair pricing that reflects their real habits and health conditions.

---

## **Project Overview**

Healthcare costs vary widely depending on daily habits, exercise level, diet, medical conditions and overall well-being.
To support smarter decision-making, this project builds a machine learning model that predicts insurance cost using structured data collected from individuals.

Several steps were followed to build a complete and reliable pipeline:

* understanding the business problem
* performing full exploratory data analysis
* engineering meaningful features
* encoding categorical data
* scaling numerical features
* training multiple machine learning models
* evaluating their performance
* saving the best performing model, scalers and encoders
* preparing an inference pipeline for real-world predictions

---

## **Dataset Summary**

The dataset contains both numerical and categorical features related to:

* lifestyle habits
* medical history
* demographic information
* health measurements
* behavioral patterns

Examples of features include exercise level, smoking status, adventure sports, age, cholesterol level, glucose level, weight change over the last year and more.

The target variable is **insurance_cost**.

---

## **Exploratory Data Analysis**

The analysis involved:

* checking missing values
* understanding distributions of numerical features
* studying unique counts in categorical features
* performing correlation analysis
* identifying patterns affecting insurance cost
* applying domain understanding to interpret trends

The goal of EDA was to prepare a clean foundation for model training and to understand how lifestyle and health metrics influence cost.

---

## **Feature Engineering**

To make the data ready for modeling, several transformation steps were applied:

* Label Encoding was used to convert categorical variables into numeric form
* Standard Scaling was applied to numerical features so that models can learn effectively
* All transformations were saved for later inference
* Domain knowledge was used to retain important features even when statistical tests suggested otherwise

The combined approach ensured the model captures medically relevant signals.

---

## **Model Training**

Two machine learning models were trained:

1. **Linear Regression**
2. **Support Vector Regression (SVR)**

Normally, GridSearchCV would be used to tune hyperparameters for more accuracy, but it was avoided due to computation time and system limitations.
The code still includes clearly marked comments showing what could have been done if resources permitted.

Both models were trained on the scaled and encoded dataset.
Their performance was evaluated using:

* R² score
* Mean Absolute Error
* Root Mean Squared Error

The model with the highest R² score was selected as the final model.

---

## **Model Saving and Deployment Preparation**

To support future predictions, the following components were saved using joblib:

* the best performing model
* the standard scaler
* the label encoders for all categorical columns
* the feature order required during prediction

These allow the model to be reused with new input data while maintaining consistent preprocessing.

---

## **Future Enhancements**

If time and system resources allow, the following modern tools and improvements can be introduced:

* building a full **FastAPI** endpoint for real-time insurance cost prediction
* containerizing the solution using **Docker**
* deploying the model on cloud platforms such as AWS, Azure or GCP
* adding SHAP or LIME for model explainability
* performing advanced hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* adding more complex models like Gradient Boosting or XGBoost
* converting the pipeline into a fully automated ML workflow

These enhancements would make the project production-ready.

---

## **Conclusion**

This project demonstrates a complete end-to-end machine learning workflow for predicting insurance cost using real-world health and lifestyle features.
Through careful data preprocessing, thoughtful feature engineering, model evaluation and deployment preparation, the solution becomes usable, scalable and practical for insurance analytics.

