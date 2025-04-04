# National-Poll-on-Healthy-Aging-NPHA-

# NPHA Doctor Visits Project

![Build Status](https://img.shields.io/travis/parisazeynaly/NPHA-doctor-visits?style=flat-square)
![License](https://img.shields.io/github/license/parisazeynaly/NPHA-doctor-visits?style=flat-square)

This repository contains an analysis of the National Poll on Healthy Aging (NPHA) dataset. The dataset explores various aspects of health in aging populations, including doctor visits, mental health, sleep medication, and stress.

In this project, various machine learning techniques are applied to:

Preprocess the data

Explore correlations and visualize patterns

Build regression and classification models

Perform feature selection and evaluate model performance

Dataset
The NPHA dataset is publicly available from the UCI Machine Learning Repository. You can access it here:
NPHA Dataset - UCI Repository

Data Preprocessing
Missing Value Handling: Checked and handled missing values in the dataset.

Outlier Detection & Capping: Identified and capped outliers in numeric columns using IQR.

Feature Selection: Dropped columns with low variance (e.g., Age column).

Data Scaling: Applied standard scaling to numeric features for better model performance.

Exploratory Data Analysis (EDA)
Correlation Heatmap: Visualized relationships between numeric features.

Boxplots: Detected and visualized outliers in key features like doctor visits, mental health, and sleep medications.

Pairplots: Visualized feature distributions and pairwise relationships.

Regression Models
Random Forest Regressor: Used for predicting the number of doctors visited based on other features.

Feature Importance: Identified important features influencing the prediction model.

Linear Regression: Applied for comparison with the Random Forest model.

Classification Models
Random Forest Classifier: Applied for classifying the number of doctors visited.

Gradient Boosting Classifier: Used to improve classification accuracy.

SMOTE: Applied Synthetic Minority Over-sampling Technique (SMOTE) to handle class imbalance.

Usage
Download the dataset and place it in the project directory (or provide the path in the code).

Run the Python scripts to perform preprocessing, EDA, and model training.

python preprocess_data.py
python train_models.py
python evaluate_models.py

Requirements
pandas

matplotlib

seaborn

scikit-learn

imblearn


Conclusion
Feature Importance: Key features influencing doctor visits were identified using the Random Forest model.

Model Evaluation: Regression and classification models were evaluated based on their performance metrics (MSE, R², accuracy).

Future Work
Investigate more sophisticated models like XGBoost or neural networks.

Handle categorical variables (if any) and experiment with other preprocessing techniques.


