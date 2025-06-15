# Customer Churn Analysis with Power BI and Machine Learning
**Project Overview**
This Power BI project focuses on analyzing customer churn to help businesses understand why customers leave and identify opportunities for retention. The project combines data visualization with machine learning to provide actionable insights.

**Key Objectives:**

- Identify patterns in customer churn behavior
- Predict which customers are likely to churn
- Provide actionable insights to reduce churn rates
- Monitor key churn-related metrics through interactive dashboards


**Project Components**

**1. Data Pipeline**
The project follows a comprehensive ETL (Extract,Transform, Load) process:

SQL Data Preparation:
- Data exploration queries to understand distributions and null values
- Data cleaning and transformation before loading to production tables
- Creation of specialized views for Power BI consumption
  
Power Query Transformations:
- Created calculated columns for churn status, age groups, tenure groups
- Implemented data categorization (e.g., monthly charge ranges)
- Unpivoted service columns for better analysis

**2. Key Metrics and Measures**
Summary Page Metrics:

Total Customers = Count(prod_Churn[Customer_ID])

New Joiners = CALCULATE(COUNT(prod_Churn[Customer_ID]), prod_Churn[Customer_Status] = "Joined")

Total Churn = SUM(prod_Churn[Churn Status])

Churn Rate = [Total Churn] / [Total Customers]

Churn Prediction Page Metrics:

Count Predicted Churner = COUNT(Predictions[Customer_ID]) 

Title Predicted Churners = "COUNT OF PREDICTED CHURNERS : " & COUNT(Predictions[Customer_ID])


![Capture](https://github.com/user-attachments/assets/142340aa-4d5d-4912-89ce-2ab137141d80)

**3. Machine Learning Integration**
Random Forest Classifier Implementation:

In this churn analysis project, the Random Forest Classifier was used as the core predictive model. Random Forest is an ensemble learning technique that builds multiple decision trees during training and merges their results to produce more accurate and stable predictions. By training the model on 80% of the preprocessed dataset and testing on the remaining 20%, we ensured a reliable evaluation using a confusion matrix and classification report. The algorithm was particularly useful for handling both numerical and categorical features, which had been label encoded beforehand. One of its major advantages is the ability to determine feature importance, helping us identify the key factors that influence customer churn. This insight guided targeted retention strategies. Finally, the trained model was applied to new customer data to predict those at high risk of churning, enabling proactive intervention.

**4. Dashboard Features**
**Churn Analysis Dashboard:**

- Visual breakdowns by demographic factors (age, gender, location)
- Service usage patterns among churned customers
- Contract type and payment method analysis
- Predictive Analytics Dashboard:
- Count and list of predicted churners
- Probability scores for at-risk customers
- Feature importance visualization



**Technical Implementation:**
**Data Sources:**
- SQL Server database with staging and production tables
- Excel and csv files for machine learning data input/output
  

**Technologies Used**
- Power BI: For visualization and interactive reporting
- Python: For machine learning implementation (Random Forest)
- SQL: For data preparation and transformation
- Jupyter Notebooks: For model development and testing


![Capture1](https://github.com/user-attachments/assets/e455450f-a8e3-499d-97b7-bdd7a8ad5764)



**How to Run the Project?**

1- Download and install Power BI Desktop.

2- Open the Power BI project file: CarsSalesDashboard.pbix.


