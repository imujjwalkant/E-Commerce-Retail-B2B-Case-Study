# E-Commerce-Retail-B2B-Case-Study

## Contributors
Ujjwal <br>
Tiana<br>
Tushar<br>
## Date
5th August 2024
## Problem Identification
A sports retail company, Schuster, dealing in B2B transactions often interacts with vendors on a credit basis, some of whom may not adhere to the stipulated payment deadlines. Vendor delays result in financial lag and loss, hampering smooth business operations. Additionally, company employees spend significant time chasing payments, leading to non-value-added activities and wasteful resource expenditure.<br>
## Business Objectives
- Segment customers to understand their payment behavior.
- Predict delayed payments using historical data for transactions with upcoming due dates.
- Enhance resource allocation, accelerate credit recovery, and reduce low-value activities.
## Approach Strategy
### Process Summary
- Data Reading and Understanding
- Exploratory Data Analysis (EDA)
- Data Cleaning and Feature Engineering
- Customer Segmentation (K-means clustering)
- Data Preparation/Splitting/Model Building
- Model and Feature Tuning – Metric Analysis
- Model Testing on Historical Data
- Model Confirmation
- Prediction Using the Model
- Summary/Conclusion/Recommendations
## EDA & Data Analysis
### Univariate Analysis Observations
- Payment delayers constitute 65.7% of the class imbalance, which is manageable without imbalance correction.
- The ‘Local Amount’ column is redundant due to the presence of 'USD Amount', and hence was dropped.
- Payments are mostly made in USD, SAR, or AED.
- The majority of bills fall under the 'INV' invoice class.
- 'WIRE' is the most preferred payment method.
### Bivariate Analysis Observations
- The third month has the highest number of invoices but a lower late payment rate compared to other high-invoice months.
- Late payment rates rise sharply starting in the seventh month, despite fewer invoices in the latter half of the year.

## Customer Segmentation
### K-means Analysis
Customer-level attributes significantly enhance model performance. Segmenting customers based on average payment time and standard deviation identifies distinct customer groups:

- Cluster 0: Medium Invoice Payment
- Cluster 1: Early Invoice Payment
- Cluster 2: Prolonged Invoice Payment
Early customers constitute 88.7%, medium payment duration 8.7%, and prolonged payers 2.6%.

## Model Building
### Logistic Regression vs. Random Forest
- Logistic regression indicated an optimum cutoff probability of 0.65.
- Random forest outperformed logistic regression in total precision and recall scores.
- Due to categorical nature of the data, random forest was deemed more suitable.
### Predictions
Applying the final model's predictions to open-invoice data:
- 50.2% of transactions are expected to experience payment delays, potentially causing business lag.
- Customers with a history of long payment delays are anticipated to have nearly 100% delay rates.
## Recommendations
- Credit Note Payments: Exhibit the highest delay rates compared to Debit Note or Invoice types. Stricter payment policies are recommended.
- Lower-Value Payments: Majority of transactions fall in this category and often face delays. Penalties could be applied based on billing amounts—smaller bills should incur higher penalties as a last resort.
- Goods-Related Invoices: Have higher delay rates than non-goods types, suggesting stricter payment policies.
- Customer Segments: Cluster 1 (prolonged payments) should receive extensive focus due to higher delay rates.
- High-Probability Companies: Prioritize companies with the highest probability and counts of delayed payments for focused attention.
## Conclusion
By implementing these strategies, Schuster can improve credit recovery, enhance resource allocation, and reduce non-value-added activities, ensuring smoother business operations and financial stability.
