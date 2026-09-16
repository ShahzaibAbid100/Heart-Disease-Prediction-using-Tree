# Heart Disease Prediction Using Decision Tree

## Project Overview

This project uses a **Decision Tree Classifier** to predict whether a person has heart disease based on different health-related features.

The project demonstrates the complete machine learning workflow from data preprocessing to model evaluation.

> **Disclaimer:** This project is created for educational and machine learning practice purposes only. It is not intended for medical diagnosis.

## Objective

The objective of this project is to classify patients into two categories:

* `0` → No Heart Disease
* `1` → Heart Disease

## 🛠️ Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
* Decision Tree Classifier

##  Dataset

The project uses a Heart Disease dataset containing patient-related features such as:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Maximum Heart Rate
* Exercise-related measurements
* Other health-related features

The target column indicates whether heart disease is present.

## Project Workflow

1. Import required libraries
2. Load the Heart Disease dataset
3. Explore the dataset
4. Check missing values and duplicates
5. Separate features (`X`) and target (`y`)
6. Split data into training and testing sets
7. Train a Decision Tree Classifier
8. Tune `max_depth`
10. Make predictions
11. Evaluate model performance
12. Visualize the Decision Tree

## 🌳 Model

The project uses a Decision Tree Classifier:

```python id="v4s8c1"
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(
    max_depth=4,
    random_state=42
)

model.fit(X_train, y_train)
```

##  Model Evaluation

The final model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* Classification Report

```python id="g5n2q8"
print("Accuracy:", accuracy_score(y_test, y_pred))
print("Precision:", precision_score(y_test, y_pred))
print("Recall:", recall_score(y_test, y_pred))
print("F1 Score:", f1_score(y_test, y_pred))
```

## 🌳 Decision Tree Visualization

The trained Decision Tree can be visualized to understand how it makes predictions.

```python id="x7c3m9"
from sklearn.tree import plot_tree
import matplotlib.pyplot as plt

plt.figure(figsize=(20, 10))

plot_tree(
    model,
    feature_names=X.columns,
    class_names=["No Disease", "Disease"],
    filled=True
)

plt.show()
```

## ⭐ Feature Importance

##  What I Learned

Through this project, I practiced:

* Decision Tree Classification
* Data preprocessing
* Train-test splitting
* Gini impurity
* Tree depth and `max_depth`
* Overfitting
* Model evaluation
* Confusion Matrix
* Tree visualization


Machine Learning & AI Learner
