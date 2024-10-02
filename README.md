# Predicting Customer Response for MegaMart
## Overview
This project focuses on predicting the likelihood of customer responses to a new Gold Membership offer by MegaMart, a leading retail chain. MegaMart's Gold Membership offers a 20% discount on all purchases for a limited time at a special price of $499 (down from $999). This project aims to build a predictive model that helps MegaMart identify which customers are most likely to accept the offer. The model will also assist in segmenting high and low-value customers based on their purchasing behavior, allowing for targeted marketing and personalized promotions.

## Project Objectives
- Predict Customer Response: Using machine learning techniques to predict whether a customer will accept the Gold Membership offer based on their historical purchase data.
- Customer Segmentation: Analyze customer value (CV) to distinguish between high and low-value customers to optimize future promotional efforts.

## Dataset
The dataset consists of customer transaction data from the past two years, including variables like spending habits, purchase frequency, and channel preferences. The raw datasets is attached to the respository.

Key Features:
- ID: Unique customer identifier.
- Year_Birth: Customer's birth year.
- Education: Customer’s education level.
- Marital Status: Customer's marital status.
- Income: Yearly household income.
- Purchase Data: Amounts spent on various product categories (e.g., Wines, Meat, Fruits, Gold Products).
- NumWebPurchases: Number of purchases made online.
- NumStorePurchases: Number of in-store purchases.
- NumDealsPurchases: Number of purchases made using discounts.
- Recency: Number of days since the last purchase.
- Response (Target Variable): Indicates whether a customer accepted the offer in the last campaign (1 = accepted, 0 = rejected).

## Project Workflow
- Data Preprocessing:
Handle missing values, perform necessary transformations, and encode categorical variables.
Standardize numerical data to improve model performance.

- Feature Engineering:
Calculate Customer Value (CV) using the following formula:
         - Total Spending per Customer: Sum of spending across all product categories.
         - Average Purchase Value (APV): Total spending divided by the number of purchases.
         - Average Purchase Frequency (APF): Number of purchases divided by the total time since the customer's enrollment.
         - Customer Value (CV): APV multiplied by APF.

- Model Building:
Split the dataset into training and testing sets. Also applying machine learning algorithms such as:
Logistic Regression, Random Forest Classifier, Gradient Boosting, Decision Tree Classifier, XGBC Classifier and KNeighborsClassifier

## Model Evaluation
Evaluate the models using metrics such as 
- Accuracy: 0.7114093959731543
- Precision: 0.30      
- Recall: 0.80      
- F1-score:0.43

After training and comparing the model with different machine learning model the most preferred model was K-Nearest Neighbours because to predict the likelihood of a customer giving a positive response to the Gold Membership offer its best to have low precision and high recall. The probability of having high number of customers responding to the gold membership is higher than the probability of customer not responding to it.

## Model Tuning:
- Use techniques like Grid Search or Random Search for hyperparameter optimization.
- Perform cross-validation to prevent overfitting.
