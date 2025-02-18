# Car Acceptability Prediction Using Machine Learning

### Project Overview

This project involves analyzing the Car Evaluation Dataset to predict car acceptability using machine learning techniques. The dataset contains categorical variables describing attributes of cars, such as Buying Price, Maintenance Cost, Number of Doors, Seating Capacity, Luggage Space, and Safety Level, along with the target variable Acceptability. 

The objective is to preprocess the data, apply one-hot encoding, train classification models, and evaluate their performance.

### Dataset

Car Evaluation Database was derived from a simple hierarchical decision model originally developed for the demonstration of DEX, M. Bohanec, V. Rajkovic: Expert system for decision making. Sistemica 1(1), pp. 145-157, 1990.). The model evaluates cars according to the following concept structure:

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
- Apply one-hot encoding for categorical variables.
- Ensure no missing or inconsistent values in categorical features.

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

5. Fairness Considerations:

- Investigated the class imbalance issue and its impact on model predictions, particularly for the rare classes: "good" and "vgood".
- Analyzed potential bias in model predictions, such as the tendency to classify high-priced cars as "unacceptable".
- Evaluated fairness with respect to important features like Safety and Price, highlighting biases in favor of lower-price and higher-safety cars.

### Key Results

- Logistic Regression achieved the highest accuracy (89.60%) with strong performance in predicting the "unacc" (unacceptable) class, but faced challenges in predicting the less frequent classes, "good" and "vgood".
- Random Forest performed slightly lower (87.28%) in terms of accuracy but provided valuable insights into feature importance and was more precise in predicting the "unacc" class.
- Safety and Capacity were identified as key features influencing car acceptability, with cars having low safety ratings being most often classified as "unacceptable".
- Price was also a significant factor, with high-priced cars overwhelmingly classified as "unacceptable", raising potential concerns about model fairness.

##### Feature Importance for Car Evaluation

![screenshot-github com-2025 01 27-12_32_47](https://github.com/user-attachments/assets/44674afc-6901-46f5-96f3-159b5c98711c)
- Safety emerged as one of the most influential features, indicating a strong relationship between higher safety ratings and acceptability.
- Price, especially high-price cars, consistently showed a bias towards being classified as "unacceptable," suggesting a need for further investigation into pricing-related biases.

### Future Improvements

- Hyperparameter Tuning: Experiment with tuning model parameters (e.g., for Random Forest) to improve model performance.
- Advanced Models: Test more sophisticated algorithms such as Gradient Boosting or Neural Networks to enhance prediction accuracy, particularly for the minority classes.
- Model Interpretability: Utilize techniques like SHAP or LIME to explain the model's predictions, offering more insight into the decision-making process.
- Fairness Adjustments: Implement strategies to address class imbalance, such as oversampling or undersampling, and explore model adjustments to reduce bias in predicting certain classes, especially for high-priced cars.

### Source

Dataset: [Car Evaluation Dataset](https://www.kaggle.com/datasets/elikplim/car-evaluation-data-set)
