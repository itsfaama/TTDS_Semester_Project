Global Demographic Growth Analysis & Prediction
Course: Tools & Techniques for Data Science

Student: Fatima Shaheen (MSCS23019)
📌 Project Overview
This project analyzes global demographic trends using a comprehensive dataset sourced from Google Cloud Platform (GCP). The analysis focuses on population dynamics such as birth rates, death rates, migration patterns, and overall growth trends across various countries over time. Additionally, Machine Learning models were implemented to predict future population growth rates.
📊 Dataset
The dataset was retrieved from the Google Cloud BigQuery Public Datasets:

Table ID: bigquery-public-data.census_bureau_international.birth_death_growth_rates

Description: It includes annual population-related indicators for countries worldwide.

Key Features:
country_code: Unique identifier for each country.

country_name: Full name of the country.

year: The calendar year of the record.

crude_birth_rate: Live births per 1,000 individuals.

crude_death_rate: Deaths per 1,000 individuals.

net_migration: Difference between immigrants and emigrants.

natural_increase_rate: Natural population change (Birth Rate - Death Rate).

population_growth_rate: Total annual growth rate including migration.

🛠 Tools & Technologies Used
Language: Python / R

Data Processing: PySpark, Pandas

Environment: Google Colab

Cloud Services: Google Cloud Platform (BigQuery)

Version Control: Git, GitHub

Visualization: Matplotlib / Seaborn (implied from chart descriptions)

🔍 Methodology
1. Exploratory Data Analysis (EDA)
Comprehensive EDA was performed to understand the data structure and quality:

Schema validation and data type checking.

Summary statistics (mean, min, max, std dev) for numerical columns.

Null value detection and duplicate removal.

Distribution analysis of key variables like growth_rate.

2. Data Cleaning
Removal of duplicate records to ensure data integrity.

Handling of missing/null values to prevent calculation errors.

Type conversion for accurate mathematical operations.

Filtering of invalid entries (e.g., unrealistic negative values).

3. Visualization
Various charts were generated to identify trends and outliers:

Line Charts: Growth rate trends over years and across countries.

Bar Charts: Comparison of birth/death rates and net migration.

Heatmaps: Correlation analysis between demographic variables.

Box Plots: To visualize data distribution and detect outliers.

4. Machine Learning Modeling
Five different machine learning models were trained to predict the Population Growth Rate:

Linear Regression (Best Performer)

Random Forest Regressor

XGBoost Regressor

Lasso Regression

Support Vector Regression (SVR)

📈 Results & Evaluation
Linear Regression was selected as the optimal model for this dataset.

Why Linear Regression?

The dataset features (crude_birth_rate, net_migration, etc.) exhibit strong linear relationships with the target variable.

Tree-based models (Random Forest, XGBoost) suffered from overfitting due to the limited dataset size.

Linear Regression provided the most interpretable results and the lowest error.

Model Performance (Linear Regression):
Mean Squared Error (MSE): 1.97

R² Score: 0.61 (Explains 61% of the variance)

Prediction Example:
Scenario: Forecasting for the year 2027.

Predicted Growth Rate: ~1.72% (based on test input values).

🚀 How to Run
Clone the repository:

Bash

git clone https://github.com/itsfaama/TTDS_Semester_Project.git
Open the notebook in Google Colab or a local Jupyter environment.

Ensure you have the required libraries installed (pyspark, pandas, matplotlib, scikit-learn).

Load the dataset (connection to GCP BigQuery may be required if not using a local CSV dump).

Run the cells sequentially to reproduce the EDA, visualizations, and model predictions.

This project was completed as part of the MSCS coursework requirements.
