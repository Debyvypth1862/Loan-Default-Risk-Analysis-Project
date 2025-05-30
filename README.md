# Risk Analytics for Loan Default Prediction

This project focuses on applying **Exploratory Data Analysis (EDA)** techniques to analyze the patterns and factors that contribute to **loan defaults** in a consumer finance company. The goal is to identify applicants who are likely to default on their loans, allowing the company to make more informed decisions and minimize the risk of financial loss.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Approach](#approach)
- [Analysis](#analysis)
  - [Missing Data Handling](#missing-data-handling)
  - [Outlier Detection](#outlier-detection)
  - [Data Imbalance](#data-imbalance)
  - [Correlation Analysis](#correlation-analysis)
- [Visualizations](#visualizations)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview

Loan approval is a critical decision for financial institutions, and the process involves assessing the risk of potential defaulters. The dataset provided contains information about loan applicants, including their previous loan history and various attributes at the time of their application. The objective of this project is to perform an **Exploratory Data Analysis (EDA)** to identify the key factors that influence a client’s likelihood of defaulting on a loan. This will help in making better decisions such as loan approval, loan amount adjustment, and setting higher interest rates for risky clients.

## Data Description

The dataset consists of **three files**:
1. **`application_data.csv`**: Contains information about the loan applicant at the time of the application, including attributes like income, loan amount, loan type, etc.
2. **`previous_application.csv`**: Contains data about the client's previous loan applications, including whether the application was approved, cancelled, refused, or resulted in an unused offer.
3. **`columns_description.csv`**: A data dictionary describing each variable in the dataset.

The target variable is `client_payment_difficulty`, which indicates whether a client had payment difficulties (1 for yes, 0 for no).
**`link to data`**: https://drive.google.com/drive/folders/16RQztUqCfJOlbooHqYlJrp6Q7iL65uZB?usp=drive_link


## Approach

### 1. Data Preprocessing
   - **Missing Data Handling**: Identify columns with missing data and apply appropriate techniques for handling them, such as removing rows/columns or imputing values.
   - **Outlier Detection**: Detect potential outliers using visualization methods (box plots, histograms) and statistical techniques.
   - **Data Transformation**: Encode categorical variables (e.g., loan status, previous applications) into numeric form for analysis.
   
### 2. Exploratory Data Analysis (EDA)
   - **Univariate Analysis**: Investigate individual variables to understand their distributions and significance.
   - **Bivariate Analysis**: Explore relationships between pairs of variables, focusing on how they influence loan defaults.
   - **Segmentation**: Segment the data by the target variable (`client_payment_difficulty`) and analyze the differences in other attributes.
   - **Correlation Analysis**: Identify correlations between variables and how they relate to loan defaults.

### 3. Risk Factors Identification
   - Identify key factors (driver variables) that contribute to loan default.
   - Use visualizations to present insights from the data analysis.

## Analysis

### Missing Data Handling
- Identifying columns with missing values and dealing with them using methods such as imputation or removal.
- Imputation strategies, if necessary, could include replacing missing values with mean/median (for numerical variables) or mode (for categorical variables).

### Outlier Detection
- Use box plots and other visualization techniques to detect outliers in numerical columns.
- Outliers will be flagged for further investigation, although they may not necessarily be removed for this analysis.

### Data Imbalance
- Analyze the class distribution of the target variable (`client_payment_difficulty`).
- Identify the imbalance and propose strategies to handle it, such as resampling techniques or adjusted evaluation metrics.

### Correlation Analysis
- Calculate correlations between the variables and investigate how they relate to loan defaults.
- Segment the data by the target variable (`client_payment_difficulty`) and analyze the top correlations.

## Visualizations
- The project includes several visualizations to help understand the patterns and relationships in the data:
  - Histograms and box plots for univariate analysis.
  - Heatmaps for correlation analysis.
  - Bar plots for categorical variable distribution.
  - Scatter plots for bivariate relationships.
  
All visualizations are created using **Python libraries** such as **Matplotlib**, **Seaborn**, and **Plotly**.

## Installation

To run this project locally, follow the steps below:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/Loan-Default-Risk-Analysis.git
   ```

2. **Install dependencies**:
   You can install the required Python libraries by running:
   ```bash
   pip install -r requirements.txt
   ```

3. **Ensure you have the dataset files** (provided in the zip folder) and place them in the appropriate directories.

## Usage

1. **Run the Jupyter notebook** (`Client-Payment_Analysis.ipynb`).
2. The notebook contains detailed explanations of the steps, including:
   - Data loading and preprocessing.
   - Univariate and bivariate analysis.
   - Correlation and segmentation analysis.
3. **View the results**: The notebook includes various visualizations and summaries to help understand the key factors affecting loan defaults.
