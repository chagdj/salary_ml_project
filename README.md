# Salary Prediction Model

## Project Overview
This project focuses on predicting salary ranges based on various job-related features using machine learning models. The dataset includes factors such as years of experience, seniority level, company size, and AI usage, among others. The goal is to develop an optimized classification model that accurately predicts salary brackets.

## Dataset
- **Number of rows:** ~3,000
- **Features:**
  - Years of experience
  - Seniority level
  - Company size
  - AI usage
  - Job position
  - City
  - Salary in euros (target variable categorized into salary ranges)

## Data Preprocessing
1. **Encoding:**
   - Ordinal encoding for `Seniority` and `Company Size`.
   - One-hot encoding for `Position` and `City`.
   - Binary encoding for `AI Usage`.
2. **Salary Range Encoding:**
   - The salary was binned into discrete ranges for classification.
3. **Feature Scaling:**
   - StandardScaler was used to normalize features.
4. **Handling Imbalanced Data:**
   - Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to increase the representation of underrepresented salary categories.

## Model Selection & Hyperparameter Tuning
### Models Tested:
- **Random Forest**
- **XGBoost**
- **LightGBM**
- **Support Vector Classifier (SVC)**

### Hyperparameter Tuning:
- Used **GridSearchCV** with **5-fold Cross-Validation**.
- Tuned parameters such as `n_estimators`, `max_depth`, `min_samples_split`, `learning_rate`, etc.
- Adjusted `class_weight='balanced'` for handling imbalance in classification.

## Performance Evaluation
### Metrics Used:
- **Accuracy**
- **Log-Loss**
- **Confusion Matrix**
- **Precision, Recall, F1-score**

### Best Performing Model:
- **Random Forest**
  - Train Accuracy: **0.5520**
  - Test Accuracy: **0.4965**
  - Train Log-loss: **1.1204**
  - Test Log-loss: **1.1528**

## Key Insights & Improvements
- The model suffered from **overfitting**, as training accuracy was much higher than test accuracy.
- Increasing the dataset size or using better feature engineering could help improve generalization.
- Additional techniques such as **Ensembling** or **Stacking** may enhance performance.
- Further hyperparameter tuning could optimize the final results.

## How to Run the Project
### Requirements:
- Python 3.x
- Libraries: `pandas`, `numpy`, `sklearn`, `xgboost`, `lightgbm`, `imblearn`

### Steps:
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`.
3. Run the Jupyter Notebook or script: `python salary_prediction.py`.
4. Review model performance outputs.

## Future Work
- Fine-tuning hyperparameters further.
- Implementing deep learning approaches (e.g., Neural Networks).
- Adding new features for better salary range estimation.

---
📌 **Author:** [Your Name]  
📌 **Date:** March 2025  
📌 **Contact:** [Your Email]

