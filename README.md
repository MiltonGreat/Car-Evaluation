# Car Acceptability Prediction Using Machine Learning

### Project Overview

This project involves analyzing the Car Evaluation Dataset to predict car acceptability using machine learning techniques. The dataset contains categorical variables describing attributes of cars, such as Buying Price, Maintenance Cost, Number of Doors, Seating Capacity, Luggage Space, and Safety Level, along with the target variable Acceptability. The objective is to preprocess the data, apply one-hot encoding, train classification models, and evaluate their performance.

### Dataset

- Dataset Name: Car Evaluation Dataset
- Source: UCI Machine Learning Repository
- File Used: car_evaluation.csv

Attributes:

- Buying: Price of the car (categories: vhigh, high, med, low)
- Maint: Maintenance cost (categories: vhigh, high, med, low)
- Doors: Number of doors (categories: 2, 3, 4, 5more)
- Persons: Seating capacity (categories: 2, 4, more)
- Lug_boot: Size of luggage boot (categories: small, med, big)
- Safety: Safety level (categories: low, med, high)
- Acceptability (Target): Acceptability of the car (categories: unacc, acc, good, vgood)

### Project Workflow

1. Data Loading and Preprocessing:
- Loaded the dataset and explored its structure.
- Checked for missing values (none found).
- Renamed columns for clarity.
- Applied one-hot encoding to convert categorical features into numerical format.

2. Feature and Target Separation:
- Extracted feature columns (X) and the target column (y).
- Encoded the target variable using LabelEncoder.

3. Model Training and Evaluation:
- Split the dataset into training (80%) and testing (20%) sets.
- Trained two classification models: (1) Logistic Regression: Achieved an accuracy of 89.60%. (2) Random Forest Classifier: Achieved an accuracy of 87.28%.
- Evaluated models using accuracy, precision, recall, and F1-score.
- Visualized results with confusion matrices.

4. Feature Importance:
- Extracted feature importance from the Random Forest model.
- Visualized the most influential features using a bar plot.

5. Model Deployment:
- Saved the trained Random Forest model to a file (car_acceptability_model.pkl) for future use.

### Key Results

- Logistic Regression achieved the highest accuracy (89.60%) with a strong performance on predicting unacceptable (unacc) cars.
- Random Forest performed slightly lower (87.28% accuracy) but provided valuable insights into feature importance.
- The Safety feature was identified as one of the most influential factors in determining car acceptability.

### Future Improvements

- Hyperparameter Tuning: Experiment with model parameters to improve performance further.
- Additional Models: Test advanced algorithms like Gradient Boosting or Neural Networks.
- Interpretability: Use SHAP or LIME to explain model predictions.
- Feature Engineering: Explore additional transformations or interactions between features.

### Source

https://www.kaggle.com/datasets/elikplim/car-evaluation-data-set
