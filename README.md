
# Global Demographic Growth Analysis & Prediction

## Course
**Tools & Techniques for Data Science (TTDS)**

## Student Information
- **Name:** Fatima Shaheen  
- **Registration No:** MSCS23019  
- **Program:** MS Computer Science  

---

## 📌 Project Overview
This semester project presents a comprehensive analysis of **global demographic growth patterns** using real-world public data. The study examines population dynamics including **birth rates, death rates, migration trends**, and **overall population growth** across multiple countries over time.

In addition to exploratory and statistical analysis, **machine learning models** were developed and evaluated to predict **future population growth rates**, making this project both analytical and predictive in nature.

---

## 🎯 Objectives
The primary objectives of this project are:
- To analyze global demographic indicators using structured data  
- To perform data cleaning and exploratory data analysis (EDA)  
- To visualize population trends across countries and years  
- To build and evaluate machine learning models for population growth prediction  
- To identify the most suitable predictive model based on performance metrics  

---

## 📊 Dataset Description

### Data Source
The dataset was retrieved from the **Google Cloud BigQuery Public Datasets**.

- **Table ID:**  
  `bigquery-public-data.census_bureau_international.birth_death_growth_rates`

### Dataset Overview
The dataset contains **annual population-related indicators** for countries worldwide, enabling longitudinal analysis of demographic trends.

---

## 🔑 Dataset Features
- **country_code:** Unique identifier for each country  
- **country_name:** Full name of the country  
- **year:** Calendar year of the record  
- **crude_birth_rate:** Live births per 1,000 individuals  
- **crude_death_rate:** Deaths per 1,000 individuals  
- **net_migration:** Difference between immigrants and emigrants  
- **natural_increase_rate:** Natural population change (Birth Rate − Death Rate)  
- **population_growth_rate:** Total annual growth rate including migration  

---

## 🛠 Tools & Technologies Used
- **Programming Languages:** Python 
- **Data Processing:** PySpark, Pandas  
- **Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn  
- **Cloud Platform:** Google Cloud Platform (BigQuery)  
- **Development Environment:** Google Colab, Jupyter Notebook  
- **Version Control:** Git, GitHub  

---

## 🔍 Methodology

### 1. Exploratory Data Analysis (EDA)
EDA was conducted to understand the structure, quality, and behavior of the data:
- Schema validation and data type verification  
- Summary statistics (mean, minimum, maximum, standard deviation)  
- Detection and removal of null values and duplicates  
- Distribution analysis of population growth indicators  

### 2. Data Cleaning & Preprocessing
To ensure data reliability:
- Duplicate records were removed  
- Missing values were handled appropriately  
- Data types were converted for numerical accuracy  
- Invalid or unrealistic values were filtered  

### 3. Data Visualization
Multiple visualizations were generated to identify trends and patterns:
- **Line Charts:** Population growth trends over time  
- **Bar Charts:** Comparison of birth rates, death rates, and migration  
- **Heatmaps:** Correlation analysis among demographic variables  
- **Box Plots:** Distribution analysis and outlier detection  

### 4. Machine Learning Modeling
The following regression models were implemented to predict **population growth rate**:
- Linear Regression (**Best Performing Model**)  
- Random Forest Regressor  
- XGBoost Regressor  
- Lasso Regression  
- Support Vector Regression (SVR)  

---

## 📈 Results & Evaluation

### Model Selection
Based on comparative analysis, **Linear Regression** was selected as the final model.

#### Justification:
- **Limited Dataset Size:** Complex tree-based models exhibited overfitting  
- **Linear Relationships:** Strong linear correlation between growth rate, birth rate, and migration  
- **Interpretability:** Linear Regression provided transparent and explainable results  

### Performance Metrics (Linear Regression)
- **Mean Squared Error (MSE):** 1.97  
- **R² Score:** 0.61  
  - Explains approximately **61% of the variance** in population growth rate  

### Prediction Example
- **Scenario:** Population growth forecast for the year 2027  
- **Predicted Growth Rate:** ~1.72%  

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository
```bash
git clone https://github.com/itsfaama/TTDS_Semester_Project.git

### Step 2: Execute the Notebook

1. Open the project notebook in **Google Colab** or **Jupyter Notebook**.

2. Install the required libraries:
   ```bash
   pip install pyspark pandas matplotlib scikit-learn
Load the dataset:

Establish a connection with Google Cloud BigQuery (if required)

Ensure proper authentication and permissions

Run the notebook:

Execute all cells sequentially

This will reproduce the EDA, visualizations, and machine learning predictions

