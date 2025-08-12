# 🚢 Titanic Survival Analysis & Prediction

## 📌 Project Overview
The Titanic disaster is one of the most infamous shipwrecks in history. This project analyzes passenger data to identify factors that influenced survival rates and builds machine learning models to predict survival outcomes.

## 🎯 Objectives
- Perform **Exploratory Data Analysis (EDA)** to understand patterns in survival.
- Identify the most important features affecting survival.
- Build predictive models to classify passengers as survived or not survived.
- Evaluate and compare model performance.

## 📂 Dataset
**Source:** [Kaggle - Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)  
**Features include:**
- **PassengerId**: Unique ID of the passenger
- **Survived**: 0 = No, 1 = Yes
- **Pclass**: Passenger class (1 = First, 2 = Second, 3 = Third)
- **Name**: Passenger name
- **Sex**: Gender
- **Age**: Age in years
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Ticket**: Ticket number
- **Fare**: Passenger fare
- **Cabin**: Cabin number
- **Embarked**: Port of embarkation (C, Q, S)

## 🔍 Exploratory Data Analysis (EDA)
Key steps performed:
1. **Missing Data Handling**
   - Filled missing `Age` with median values.
   - Filled missing `Embarked` with mode.
   - Dropped `Cabin` due to excessive missing values.
2. **Univariate Analysis**
   - Distribution of age, fare, and survival rates.
3. **Bivariate Analysis**
   - Survival rates by **gender**: Women had significantly higher survival rates.
   - Survival rates by **class**: First-class passengers had the highest survival chance.
   - Age groups: Children had better survival chances.
4. **Correlation Heatmap**
   - Identified relationships between numerical features.

## ⚙️ Feature Engineering
- Converted `Sex` and `Embarked` into numeric codes.
- Created `FamilySize = SibSp + Parch + 1`.
- Created `IsAlone` feature for passengers traveling alone.
- Created categorical age groups.

## 🤖 Model Building
Implemented and evaluated the following models:
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVM)
- Gradient Boosting Classifier

**Model Evaluation Metrics:**
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix

## 📊 Key Insights
- **Gender:** Women had ~74% survival rate vs. ~19% for men.
- **Passenger Class:** Higher classes had better chances of survival.
- **Family Size:** Very large families and solo travelers had lower survival rates.
- **Fare:** Higher fares were associated with better survival chances.

## 📈 Results
| Model | Accuracy | F1-Score |
|-------|----------|----------|
| Logistic Regression | 0.81 | 0.78 |
| Random Forest | 0.84 | 0.82 |
| SVM | 0.82 | 0.79 |
| Gradient Boosting | 0.85 | 0.83 |

**Best Model:** Gradient Boosting Classifier with 85% accuracy.

## 📦 Dependencies
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
