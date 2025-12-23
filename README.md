# Marketing Campaign Data Analysis
This project performs an end-to-end exploratory data analysis (EDA) and data cleaning process on a marketing campaign dataset to understand customer behavior, demographics, and purchasing patterns.

# Table of Contents
  - Dataset Overview
  - Key Objectives
  - Analysis Workflow
  - Technologies Used
  - Key Insights

# Dataset Overview
  - The dataset contains 2,240 customer records with 28 initial features, including:
  - Demographics: ID, Year of Birth, Education, Marital Status, and Income .
  - Customer Habits: Recency of purchase, amount spent on various products (Wines, Fruits, Meat, Fish, Sweets, Gold), and number of purchases via different channels (Web, Catalog, Store) .
  - Campaign Responses: Whether the customer accepted offers in 5 different campaigns .

# Key Objectives
  - Data Cleaning: Handle missing values and correct data types (e.g., converting Income from string to float).
  - Feature Engineering: Create new metrics such as Total_Children, Total_Spending, Total_Purchases, and Age.
  - Outlier Treatment: Identify and trim outliers in purchase channels using the Interquartile Range (IQR) method.
  - Exploratory Data Analysis: Visualize distribution channels and customer demographics to find actionable pattern.

# Analysis Workflow
## Data Preprocessing
    - Income Cleaning: Removed currency symbols and commas to convert income into a numeric format .
    - Imputation: Missing income values (24 records) were filled using the mean income grouped by the customer’s Education and Marital_Status to ensure demographic accuracy .
## Feature Engineering
    - New variables were derived to simplify analysis:
    - Total_Children: Sum of Kidhome and Teenhome.
    - Total_Spending: Aggregate spending across all product categories.
    - Age: Calculated using 2014 as the reference year (the last transaction year in the data) .

## Visualizations & Outlier Treatment
    - Histograms & Boxplots: Used to analyze the distribution of NumWebPurchases, NumCatalogPurchases, and NumStorePurchases.
    - Outlier Trimming: Specifically targeted extreme values in web and catalog purchases to prevent skewed statistical results .

## Correlation Analysis
    - Heatmap: Generated to identify relationships between income, spending habits, and demographic factors.

# Technologies Used
    - Python (Core analysis) 
    - Pandas & NumPy (Data manipulation) 
    - Matplotlib & Seaborn (Data visualization) 

# Key Insights
  - Customer Complaints: A significant majority (over 85%) of customer complaints originate from those with Graduation or 2nd Cycle educational backgrounds.
  - Spending Patterns: Created clear visualizations linking the number of children in a household to total purchasing power.

# How to Run
  - Ensure you have the marketing_data.csv and the data dictionary Excel file in your working directory.
  - Run the Jupyter Notebook Marketing Campaign - Jupyter Notebook.ipynb
