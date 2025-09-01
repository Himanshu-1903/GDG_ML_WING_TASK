📌 GDG ML Wing Task – Classification Models
🚀 Project Overview

This project is a part of the GDG ML Wing Task, where the goal is to preprocess a dataset and build a hierarchy of machine learning models for classification.

We implement and compare three supervised learning models:

Base Model → K-Nearest Neighbors (KNN)

Middle Model → Support Vector Machine (SVM)

Top Model → Logistic Regression

Each model is trained on the same preprocessed feature matrix to ensure fairness in evaluation.

⚙️ Features

End-to-end data preprocessing pipeline

Conversion of categorical features into sparse one-hot encoded matrix

Standardization of numeric features

Implementation of KNN, SVM, and Logistic Regression classifiers

🛠️ Tech Stack

Language: Python 🐍

Libraries:

pandas, numpy – Data handling

scikit-learn – ML models & preprocessing

matplotlib, seaborn – Visualization

🔄 Workflow

Data Preprocessing

Handle missing values

Encode categorical features using OneHotEncoder

Scale numeric features using StandardScaler

Split dataset into train and test sets

Model Implementation

Train KNN as the baseline model

Train SVM with linear kernel

Train Logistic Regression with maximum iterations set to 1000

Evaluation

Calculate Accuracy, Precision, Recall, F1-score

Plot Confusion Matrix for each model

Compare performance across models

📊 Results (Example)

Model	Accuracy

KNN (Base Model)	48%

SVM (Middle Model)	85%

Logistic Regression	96%


▶️ How to Run

Clone the repository:

git clone https://github.com/Himanshu-1903/GDG_ML_WING_TASK.git
cd GDG_ML_WING_TASK


Install dependencies:

pip install -r requirements.txt


Run the notebook or Python scripts in src/

Evaluation metrics: Accuracy, Precision, Recall, F1-score, and Confusion Matrix

Model comparison to analyze performance improvements
