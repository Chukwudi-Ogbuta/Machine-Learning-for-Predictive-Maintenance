# Predictive Maintenance for Generators

## Overview
This project focuses on predictive maintenance for generators using machine learning techniques. Sensor data collected from generators is analyzed to predict potential failures and schedule preventive maintenance. The project involves data preprocessing, model building, and evaluation using PySpark.

## Data Generation
Synthetic sensor data is generated for a specified number of machines and historical rows. Each machine produces sensor readings such as voltage, current, frequency, temperature, and more. The data includes timestamps, maintenance dates, failure dates, and failure reasons, simulating real-world scenarios.

## Data Preprocessing
- **Data Cleaning**: Duplicates and null records are removed from the dataset.
- **Feature Engineering**: Certain columns are rounded off to two decimal places for consistency.
- **Feature Selection**: Relevant features for predictive modeling are selected, including numerical sensor readings and failure reasons.

## Model Building
- **Label Encoding**: Categorical failure reasons are converted to numerical labels using StringIndexer.
- **Feature Vectorization**: Numerical features are assembled into a single feature vector using VectorAssembler.
- **Feature Scaling**: Features are scaled using StandardScaler to normalize the data.
- **Logistic Regression**: A logistic regression model is trained using the scaled features to predict failure probabilities.

## Model Evaluation
- The dataset is split into training and testing sets using a 70:30 ratio.
- The logistic regression model is trained on the training data and evaluated on the testing data.
- Model performance metrics such as accuracy, precision, recall, and F1-score are calculated using MulticlassClassificationEvaluator.

## Model Performance
- **Accuracy**: 98.26%
- **Precision**: 96.73%
- **Recall**: 98.26%
- **F1-score**: 97.48%

## Model Deployment
- The trained pipeline model is saved for future use in predicting generator failures and scheduling maintenance.

By leveraging machine learning techniques on sensor data, this project enables proactive maintenance strategies, reducing downtime and improving operational efficiency in generator systems.
