# Battery Electrode Capacity Prediction Model
This repository contains a machine learning pipeline for predicting the gravimetric capacity of battery electrodes using various regression models. The model is trained on material features including crystallographic data and Magpie-derived elemental properties.

![ppt_results](https://github.com/user-attachments/assets/9b30240e-f1d8-4b92-b158-f73a0638ae2f)


# Project Overview
The project aims to predict battery electrode capacity (capacity_grav) using various material properties and structural features. Multiple machine learning models are evaluated to identify the best-performing algorithm for accurate capacity prediction.

# Features
- Data Preprocessing: Handles missing values, removes constant features, and applies feature scaling
- Multiple ML Models: Implements and compares 6 different regression algorithms
- Feature Importance Analysis: Identifies key features influencing capacity prediction
- Prediction Pipeline: Enables predictions on new material data
- Comprehensive Evaluation: Includes multiple metrics (MAE, MSE, R²) and visualizations

# Requirements
 
pandas
numpy
scikit-learn
matplotlib
seaborn
xgboost
catboost

# Data Preprocessing
- The pipeline performs the following preprocessing steps:
- Data Cleaning: Removes specified columns and handles missing values
- Target Filtering: Filters capacity values between 150-600 mAh/g
- Feature Selection: Removes constant features using VarianceThreshold
- Categorical Encoding: Converts categorical variables to numeric
- Feature Scaling: Applies StandardScaler for normalization
- Train-Test Split: 70-30 split with random_state=1 for reproducibility

# Machine Learning Models
The following regression models are implemented and compared:

- Random Forest Regressor
- Decision Tree Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
- CatBoost Regressor (Best performer)
- K-Nearest Neighbors Regressor

# Output Files
The notebook generates several output files:
- catboost_data.csv: Contains actual vs predicted values for train and test sets
- catboost_predictions_formatted.csv: Full predictions with formatting
- catboost_predictions_simple.csv: Simplified prediction output
- capacity_grav_prediction_models.png: Comparative plot of all models
- feature_importance1.png: Visualization of feature importance 
