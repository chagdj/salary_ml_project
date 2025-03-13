# 🚀 Salary Prediction Using Machine Learning

## 📌 Project Overview
This project aims to predict salary ranges based on various job-related features using machine learning models. The models used include **🌲 Random Forest, 🚀 XGBoost, ⚡ LightGBM, and 🤖 SVM**, with hyperparameter tuning and **📊 SMOTE** to handle class imbalances. 

## 🔢 Features and Encoding
The dataset contains the following key features:
- 📆 **Years of Experience** (binned every 3 years)
- 🇩🇪 **Years of Experience in Germany** (binned every 2 years)
- 📊 **Seniority Level** (Ordinal encoding: Junior, Mid-level, Senior, etc.)
- 🏢 **Company Size** (Categorical encoding: 0-50, 50-100, etc.)
- 🤖 **AI Use** (Binary: Yes/No)
- 📍 **Position and City** (One-hot encoded)
- 💰 **Salary Range** (Binned and encoded for classification)

## 🔧 Data Preprocessing
1. 🛠 **Feature Engineering**: Encoding categorical variables, binning years of experience, and handling missing values.
2. 📏 **Scaling**: Standardizing numerical features for models like SVM and Logistic Regression.
3. ⚖️ **Class Balancing**: Using **SMOTE** to oversample underrepresented salary ranges.

## 🏋️‍♂️ Model Training
### **🧠 Models Implemented**:
- 🌲 **Random Forest**
- 🚀 **XGBoost**
- ⚡ **LightGBM**
- 🤖 **SVM**
- 🔍 **Logistic Regression** (Baseline)

### **🛠 Hyperparameter Tuning**:
- 🎯 **GridSearchCV**: Optimized hyperparameters for better performance.
- 🔄 **Cross-validation**: Used K-Fold cross-validation for robust evaluation.

## 📊 Model Evaluation
- ✅ **Accuracy**: Measures the overall correctness of predictions.
- 🧩 **Confusion Matrix**: Evaluates the model’s classification performance for different salary classes.
- 🎯 **Precision, Recall, F1-score**: Helps assess model strengths and weaknesses per salary class.

## 🏆 Key Results
- Best performing model: **[🏅 Random Forest]** with **[📈 55%]**.
- Accuracy improved by **[🚀 14%]** after feature engineering and SMOTE.
- Model struggles with **salary class 2**, requiring further balancing strategies.

## 🚀 Improvements & Next Steps
- ⚖️ **Better Handling of Class Imbalances**: Adjust SMOTE strategy.
- 🎯 **Feature Selection**: Reduce less significant features for better generalization.
- 🔧 **Hyperparameter Optimization**: Fine-tune learning rate and regularization parameters.
- 🤝 **Try Ensemble Learning**: Combining multiple models for better performance.

## ▶️ How to Run the Project
### **📌 Requirements**:
Install dependencies using:
```bash
pip install -r requirements.txt
```
### **🚀 Run the Model**:
```bash
python train_model.py
```




