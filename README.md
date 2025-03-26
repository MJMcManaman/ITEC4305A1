# Introduction

This assignment focuses on suggesting business actions and strategies on lowering the percentage of churned customer using machine learning. <br>
Here is a list of featuers involved and their meanings:

Attrition_Flag: Indicates whether the customer is an existing customer or has closed their account (attrited).<br>
Customer_Age:The age of the customer. (Numerical)<br>
Gender:The gender of the customer. (Categories: "M" (Male), "F" (Female))<br>
Dependent_count:The number of dependents the customer supports. (Numerical - Integer)<br>
Education_level:The highest education level attained by the customer. <br>
Marital_status:The marital status of the customer.<br>
Income_category:The customer’s income category.<br>
Card_category: The type of credit card the customer holds.<br>
Months_on_book: The total number of months the customer has had an account with the bank.<br>
Credit_limit: The total credit limit assigned to the customer.<br>
Total_revolving balance: The total balance on the customer’s revolving credit accounts.<br>
Avg_open_to_buy: The average amount of credit available to the customer (Credit Limit - Revolving Balance).<br>
Total_amt_chng_Q4_Q1: The percentage change in the total transaction amount between the fourth and first quarters.<br>
Total_trans_amt: The total transaction amount spent by the customer.<br>
Total_trans_ct: The total number of transactions made by the customer.<br>
Total_ct_chng_Q4_Q1: The percentage change in the total transaction count between the fourth and first quarters.<br>
Avg_utilization_ratio: The average utilization ratio of the customer's credit limit (Total Balance / Credit Limit).<br>

Dataset Link:https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers

# What we covered using machine learning:

1. **Data preprocessing**:
   Visualization with histograms, barcharts, scatterplots, and correlation matrix.<br>
   Handled missing and unnecessary data.<br>
   Data type transformation (categorical features to numerial features using label_encoding).<br>
   Detected outliers but did not remove any, reason being those are important to the dataset.<br>
2. Chanllenge we faced during data preprocessing - **Imbalanced dataset**<br>
   What we did to resolve this issue - **SMOTE (synthetic minority oversampling technique)**<br>
   Why it helps - SMOTE helps balance imbalanced datasets by generating synthetic samples for the minority class. The re-sampled dataset has an equal number of samples for both classes, improving model performance on the minority class.
   
3. **Model Selection and Performance Evaluations**:<br>
   **Naive Bayes** - We first used Naïve Bayes classifier for predicting customer churn using features like age, credit limit, and transaction history. We employed stratified 5-fold cross-validation to ensure reliable performance metrics across balanced data splits. Key evaluation metrics include accuracy, precision, recall, RMSE, and R², with results averaged across folds. The aggregated confusion matrix visualizes prediction errors.
   **Result** RMSE: 0.4351

   **Decision Tree** - Next we chose Decision Tree classifier for predicting customer churn using features like age, credit limit, and transaction history. We also uses stratified 5-fold cross-validation to ensure balanced splits and reliable metrics. Key performance measures include accuracy, precision, recall, RMSE, and R², averaged across folds. <br>
   By limiting tree depth, the model balances interpretability and performance. Results show how well the tree distinguishes churners from retained customers, providing actionable insights while avoiding overfitting.<br>
   **Result** RMSE: 0.3048
   
   **XGBoost** - Next step we used XGBoost classifier for predicting customer churn using features like age, credit limit, and transaction history. It employs stratified 5-fold cross-validation to ensure robust performance metrics. Key evaluation measures include accuracy, precision, recall, RMSE, and R², with results averaged across folds. <br>
   XGBoost’s gradient-boosted trees optimize predictive performance while minimizing overfitting. The model's effectiveness is summarized through mean metrics, providing insights into its ability to classify churn accurately.
   **Result** RMSE: 0.2174
   
   **Random Forest** - Lastly, we used Random Forest classifier (100 trees) for predicting customer churn using features like age, credit history, and transaction patterns. Also uses stratified 5-fold cross-validation to ensure reliable performance metrics. The model tracks accuracy, precision, recall, RMSE, and R², with results averaged across folds. <br>
   Random Forest's ensemble approach combines multiple decision trees to improve generalization and reduce overfitting. The output provides clear performance metrics, demonstrating the model's effectiveness in identifying customer churn patterns from the given features.
   **Result** RMSE: 0.1940
   
5. **Hyperparameter Tuning**:<br>
   **On XGBoost**: We used GridSearchCV to optimize customer churn prediction. It tests combinations of key parameters including tree depth, learning rate, and subsampling ratios. The search employs stratified 3-fold cross-validation to evaluate model performance on accuracy, RMSE, and R² metrics. We output the best parameter set and corresponding scores, balancing predictive power and computational efficiency. This approach systematically improved model performance by finding the optimal configuration for the XGBoost algorithm.
   **Result** Before: 0.2174, after: 0.13106
   
   **On Random Forest**: We performed grid search optimization for a Random Forest model to predict customer churn. It tests combinations of key parameters including number of trees, split criterion, and leaf/node sample requirements. We output the optimal parameter set and corresponding evaluation scores. This systematic approach ensures the Random Forest classifier achieves peak performance by balancing model complexity and predictive power for customer churn prediction.<br>
   **Result** Before: 0.1940, after: 0.1475

   **Conclusion** - After hyperparameter tuning, XGBoost now have lower it's RMSE from 0.2174 to 0.1310, Random Forest also decrease it's RMSE from 0.1940 to 0.1475. However this means after fine tuning XGBoost becomes the model that have best performance. <br>
  Throughout testing we also noticed that using GridSearchCV require much less runtime than using itertool while perform hyperparameter tuning under same param_grid and cross-validate setting.




















   
