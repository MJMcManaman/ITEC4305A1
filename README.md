# ITEC4305A1

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

What we covered using machine learning:
1. **Data preprocessing**:
   Visualization with histograms, barcharts, scatterplots, and correlation matrix.
   Handled missing and unnecessary data.
   Data type transformation (categorical features to numerial features using label_encoding).
   Detected outliers but did not remove any, reason being those are important to the dataset.
2. Chanllenge we faced during data preprocessing - **Imbalanced dataset**
   What we did to resolve this issue - **SMOTE (synthetic minority oversampling technique)**
   Why it helps - SMOTE helps balance imbalanced datasets by generating synthetic samples for the minority class. The re-sampled dataset has an equal number of samples for both classes, improving model performance on the minority class.

















   
