# User Guidence for House Price Prediction Project

## Overview
This project aims to develop a machine learning model to accurately predict the median house price in California. The primary goal is to determine which features most significantly impact house prices. The dataset used in this project is sourced from Kaggle, and you can find it [here](https://www.kaggle.com/datasets/nazishjaveed/california-house-price-prediction).

After evaluating multiple models, XGBoost emerged as the most accurate with an R² score of 83%. The Random Forest model also performed well, achieving an R² score of 81%.

## Installation

To set up your environment and run the project, follow these steps:

1. **Install Python**:
   - Download and install Python from [python.org](https://www.python.org/downloads/).
   - During installation, ensure that the option to "Add Python to PATH" is checked.

2. **Install pip**:
   - If pip is not already installed, you can install it using:
     ```bash
     sudo python3 get-pip.py
     ```

3. **Install Required Packages**:
   - Use the following commands to install the necessary Python libraries:
     ```bash
     pip install pandas
     pip install numpy
     pip install seaborn
     pip install matplotlib
     pip install scikit-learn
     pip install notebook
     ```

4. **Run Jupyter Notebook**:
   - Start Jupyter Notebook by running the following command:
     ```bash
     jupyter notebook
     ```
   - Open the notebook file `House_Price_Prediction_f-3.ipynb` from the project directory.

## Usage

1. **Clone the Repository**:
   - To get a local copy of the project, run:
     ```bash
     git clone https://github.com/yourusername/house-price-prediction.git
     cd house-price-prediction
     ```

2. **Open Jupyter Notebook**:
   - Launch Jupyter Notebook and open the file:
     ```bash
     jupyter notebook House_Price_Prediction_f-3.ipynb
     ```

3. **Follow the Notebook Instructions**:
   - The notebook contains all the steps for data preprocessing, exploratory data analysis, model training, and evaluation.

## Project Structure

- **Dataset**: The dataset is available on Kaggle and can be accessed [here](https://www.kaggle.com/datasets/nazishjaveed/california-house-price-prediction).
- **Notebook**: The main code and analysis are contained in the Jupyter notebook `House_Price_Prediction_f-3.ipynb`.

## Results

- **XGBoost Model**: Achieved an R² score of 83%, making it the most accurate model in predicting house prices.
- **Random Forest Model**: Achieved an R² score of 81%, performing slightly less accurately than XGBoost but still highly effective.

  

## Date: 2024-06-24

### Activity 1: Initial Setup and Data Exploration
- **Description:** Imported necessary libraries for data analysis and visualization.
- **Time Spent:** 10 minutes
- **Notes:**
  - Libraries used: pandas, seaborn, numpy, matplotlib, warnings.

### Activity 2: Loading and Initial Exploration of Housing Data
- **Description:** Loaded housing data and performed initial exploration.
- **Time Spent:** 20 minutes
- **Notes:**
  - Checked the shape of the dataset.
  - Identified missing values in the data.

### Activity 3: Dataset Description
- **Description:** Described the dataset including all columns.
- **Time Spent:** 15 minutes
- **Notes:**
  - Used `describe(include='all')` to get summary statistics.

### Activity 4: Visualization of 'total_bedrooms' Distribution
- **Description:** Visualized the distribution of 'total_bedrooms'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Created a histogram using `seaborn.distplot`.
  - Filled missing values in 'total_bedrooms' with the median.

### Activity 5: Checking Remaining Missing Values
- **Description:** Checked for remaining missing values.
- **Time Spent:** 10 minutes
- **Notes:**
  - Confirmed no missing values remain after imputation.

### Activity 6: Histograms of Numerical Features
- **Description:** Created histograms for all numerical features.
- **Time Spent:** 30 minutes
- **Notes:**
  - Plotted histograms using `housing_data.hist`.

### Activity 7: Visualization of 'median_income' Distribution
- **Description:** Visualized the distribution of 'median_income'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Created a distribution plot for 'median_income'.

### Activity 8: Bar Plot for 'ocean_proximity'
- **Description:** Created a bar plot for 'ocean_proximity'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Visualized the counts of different categories in 'ocean_proximity'.

### Activity 9: Scatter Plot of 'median_house_value' vs. 'median_income'
- **Description:** Visualized the relationship between 'median_house_value' and 'median_income'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Created a scatter plot showing the correlation.

### Activity 10: One-Hot Encoding for 'ocean_proximity'
- **Description:** Applied one-hot encoding to 'ocean_proximity'.
- **Time Spent:** 30 minutes
- **Notes:**
  - Used `pd.get_dummies` to encode categorical variable.
  - Dropped original 'ocean_proximity' column after encoding.

### Activity 11: Heatmap of Correlation Matrix
- **Description:** Created a heatmap of the correlation matrix.
- **Time Spent:** 20 minutes
- **Notes:**
  - Visualized correlations using `sns.heatmap`.

### Activity 12: Filtering Outliers in 'median_house_value'
- **Description:** Filtered out outlier values in 'median_house_value'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Removed specific outlier values from the dataset.

### Activity 13: Scatter Plot After Outlier Removal
- **Description:** Visualized 'median_house_value' vs. 'median_income' after removing outliers.
- **Time Spent:** 20 minutes
- **Notes:**
  - Created a scatter plot to confirm the data cleanup.

### Activity 14: Box Plots for 'median_house_value' vs. 'ocean_proximity'
- **Description:** Created box plots to show 'median_house_value' against 'ocean_proximity'.
- **Time Spent:** 20 minutes
- **Notes:**
  - Visualized distribution of house values across different proximities.

### Activity 15: Feature Engineering
- **Description:** Created new features for rooms, bedrooms, and population per household.
- **Time Spent:** 30 minutes
- **Notes:**
  - Calculated and added new columns for ratios.

### Activity 16: Dropping Redundant Columns
- **Description:** Dropped redundant columns after feature engineering.
- **Time Spent:** 15 minutes
- **Notes:**
  - Removed 'total_rooms', 'total_bedrooms', 'population', 'households' columns.

### Activity 17: Filtering 'ISLAND' Category from 'ocean_proximity'
- **Description:** Removed 'ISLAND' category from 'ocean_proximity'.
- **Time Spent:** 10 minutes
- **Notes:**
  - Filtered out the 'ISLAND' category from the dataset.

### Activity 18: Final Data Preparation
- **Description:** Final DataFrame preparation.
- **Time Spent:** 15 minutes
- **Notes:**
  - Dropped unnecessary columns and reset index.

### Summary
- **Description:** Completed data preprocessing and exploratory data analysis for house price prediction.
- **Time Spent:** 6 hours 5 minutes in total
- **Notes:**
  - Dataset is now clean and ready for machine learning model training.
 
Model Training
-

**Model Implementation:** Training various machine learning models including:
- **Linear Regression**
- **Decision Tree**Decision Tree
- **Random Forest**
- **XGBoost**
**Hyperparameter Tuning:** Optimizing model parameters to enhance performance.
  
Model Evaluation
-
**Performance Metrics:** Comparing models using:
- **R² (R-squared)**
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
Feature Importance: Identifying key features that most influence house prices.

