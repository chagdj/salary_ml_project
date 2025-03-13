# Salary Prediction Model

## 📌 Project Overview
This project aims to develop a machine learning model that predicts salary ranges based on various job-related factors. The model leverages different machine learning techniques, including feature engineering, class balancing (SMOTE), and hyperparameter tuning to optimize performance.

## 📂 Dataset
The dataset contains approximately **3000 rows** with the following key features:
- `years_of_xp`: Total years of experience
- `years_of_xp_germany`: Experience in Germany
- `vacation_days`: Number of vacation days
- `company_size`: Size of the company
- `seniority`: Job seniority level
- `ai_use`: Whether AI is used in the role
- `year`: Year of the salary record
- `position`: Job position (One-Hot Encoded)
- `city`: Location of the job (One-Hot Encoded)
- `salary_euros`: Actual salary (used to derive salary range)

## 🔍 Preprocessing and Feature Engineering
1. **Encoding Categorical Variables**
   - `seniority` and `company_size` were mapped to ordinal values.
   - `position` and `city` were one-hot encoded.
   - `ai_use` was converted to binary (1 for Yes, 0 for No).
2. **Salary Range Encoding**
   - Salaries were binned into **discrete categories** for classification.
3. **Feature Scaling**
   - Standardization was applied using `StandardScaler`.
4. **Handling Imbalance with SMOTE**
   - SMOTE was applied to increase the sample size of underrepresented salary classes to improve model performance.

## 🏆 Models Implemented
The following models were trained and evaluated:
- **Random Forest**
- **Support Vector Machine (SVM)**
- **XGBoost**
- **LightGBM**

## ⚙️ Hyperparameter Tuning
GridSearchCV was used to optimize key parameters such as:
- `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf` for Random Forest
- `learning_rate`, `num_leaves`, `max_depth` for XGBoost & LightGBM
- `C`, `kernel` for SVM

## 📊 Model Evaluation
The models were evaluated using:
- **Accuracy**: Overall correctness of predictions
- **Log-loss**: Measures confidence of predictions
- **Precision, Recall, F1-score**: To balance false positives & false negatives
- **Confusion Matrix**: Visualizing classification performance

### 🔹 Best Model Selection
After comparing **train & test accuracy, log-loss, and classification reports**, the best model was selected based on:
- **Balanced accuracy across salary classes**
- **Generalization to unseen data (avoiding overfitting)**
- **Higher F1-score and recall for underrepresented salary classes**

## 🚀 Future Improvements
- **Feature Engineering**: Explore additional features such as industry, remote work status, or education level.
- **Ensemble Learning**: Combine multiple models to improve robustness.
- **Data Augmentation**: Enhance the dataset with more salary samples.

## 💡 Key Takeaways
1. **SMOTE helped balance the dataset but required fine-tuning to prevent over-sampling.**
2. **Hyperparameter tuning improved model performance, but overfitting remained a challenge.**
3. **Log-loss proved useful in evaluating confidence in classification predictions.**
4. **Choosing the best model required considering both accuracy and class-specific metrics.**

