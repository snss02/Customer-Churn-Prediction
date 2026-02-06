# Customer-Churn-Prediction
Telecom customer churn analysis using Python and logistic regression.
Description:
This project analyzes a telecom dataset of 7,043 customers to predict customer churn using machine learning. The analysis includes data preprocessing, feature engineering (e.g., tenure groups), exploratory data analysis (EDA), and building a logistic regression model that achieves approximately 80% accuracy. Key churn drivers, such as contract type, monthly charges, and internet service preferences, are identified to inform customer retention strategies.

The project demonstrates skills in Python programming, data preprocessing, EDA, machine learning, and analytical thinking. It was developed using Google Colab for ease of access and reproducibility.

Table of Contents
Installation
Usage
Dataset
Methodology
Results
Conclusion
Technologies Used
License
Author
Installation
Prerequisites:

A Google account (for Google Colab).
Basic familiarity with Python (optional, as code is explained).
MySQL Workbench (optional, for SQL-based exploration).
Libraries:

The notebook uses pre-installed libraries in Google Colab. If running locally, install via pip:

Copy code
pip install pandas scikit-learn matplotlib seaborn
For SQL integration (optional): pip install pymysql.
Clone or Download:

Download the notebook (Customer_Churn_Prediction.ipynb) from this repository.
Upload the dataset (see Dataset) to your Colab environment.
Usage
Open the notebook in Google Colab.
Upload the dataset file to Colab (Files tab > Upload).
Run the cells sequentially:
Load and preprocess data.
Perform EDA (visualizations).
Train and evaluate the logistic regression model.
Review feature importance for insights.
Customize as needed (e.g., adjust model parameters for better accuracy).
For SQL exploration (optional):

Use MySQL Workbench to load the dataset and run queries like SELECT Contract, AVG(MonthlyCharges) FROM customers GROUP BY Contract;.
Dataset
Source: Telco Customer Churn dataset from Kaggle (publicly available).
File: WA_Fn-UseC_-Telco-Customer-Churn.csv (download from Kaggle).
Size: ~7,043 rows, 21 columns.
Features: Includes demographics (e.g., gender, senior citizen), services (e.g., internet, phone), billing (e.g., monthly charges, contract type), and the target variable (Churn: Yes/No).
Note: The dataset is clean with minimal missing values, making it ideal for analysis.
Methodology
Data Acquisition: Load the CSV into pandas (or MySQL for SQL queries).
Preprocessing: Handle missing values, encode categoricals (one-hot encoding), and convert data types.
Feature Engineering: Create tenure groups (e.g., 0-12 months, 13-24 months) and encode them.
EDA: Visualize distributions (e.g., churn rates, correlations) using seaborn and matplotlib.
Modeling: Split data (80/20 train/test), train logistic regression, and evaluate accuracy.
Analysis: Extract feature importance to identify churn drivers.
Results
Model Performance: Logistic regression achieved ~80% accuracy on the test set.
Key Churn Drivers (Top Features by Importance):
InternetService_Fiber optic (0.548): Strong predictor of churn.
TenureGroup_Long (0.504): Long-tenure customers at risk.
PaperlessBilling (0.341) and PaymentMethod_Electronic check (0.312): Digital preferences linked to churn.
Others: MultipleLines, StreamingMovies, SeniorCitizen, StreamingTV, Partner, MonthlyCharges (0.010).
Visualizations: Included plots for churn distribution, correlations, and boxplots (e.g., MonthlyCharges vs. Churn).
Conclusion
Overall, the model achieved ~80% accuracy, confirming its reliability for predicting churn. To support customer retention, telecom companies should prioritize personalized interventions: offer incentives for fiber optic users, enhance digital experiences, and monitor long-tenure customers for early signs of dissatisfaction. This analysis demonstrates the power of data preprocessing, EDA, and machine learning in deriving actionable insights, ultimately reducing churn and improving business outcomes. 
This analysis highlights actionable insights for telecom retention: Focus on fiber optic users with service enhancements, monitor long-tenure customers, and optimize digital billing/payment options. The model's accuracy validates its use for predictions, potentially reducing churn through targeted strategies. Future improvements could include advanced models (e.g., random forests) or hyperparameter tuning.
Technologies Used
Python: Core language.
Libraries: Pandas (data manipulation), Scikit-learn (ML), Matplotlib/Seaborn (visualization).
Tools: Google Colab (development).
Other: Markdown for documentation.
License
This project is open-source under the MIT License. Feel free to use, modify, and distribute.
