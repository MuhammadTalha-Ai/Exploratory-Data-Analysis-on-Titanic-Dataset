# Exploratory-Data-Analysis-on-Titanic-Dataset

# 🚢 Titanic Dataset – Exploratory Data Analysis (EDA) Report

## 📁 Dataset Overview

**Source**: [Kaggle – Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/)  
**Description**: Classic binary classification dataset where the goal is to predict survival based on passenger attributes.

---

## 🧾 1. Initial Data Exploration

- **Rows**: 891  
- **Columns**: 12  
- **Target variable**: `Survived` (0 = No, 1 = Yes)

### 🔍 Data Preview

| PassengerId | Survived | Pclass | Name | Sex | Age | SibSp | Parch | Ticket | Fare | Cabin | Embarked |
|-------------|----------|--------|------|-----|-----|--------|--------|--------|------|--------|----------|

### 📊 Data Types and Missing Values

- `Age`: 177 missing values  
- `Cabin`: 687 missing (dropped)  
- `Embarked`: 2 missing values

---

## 🧹 2. Data Cleaning

- `Age`: Filled with median  
- `Embarked`: Filled with mode  
- `Cabin`: Dropped due to excessive missing values  
- Categorical conversion applied to:
  - `Pclass`, `Survived`, `Sex`, `Embarked`

---

## 📊 3. Univariate Analysis

### 🎯 Survival Distribution
- ~38% Survived, ~62% Did not survive

### 🛳 Passenger Class Distribution
- Class 3 had the most passengers
- Class 1 had the least

### 🙋 Gender Distribution
- Male passengers: 65%
- Female passengers: 35%

---

## 🔁 4. Bivariate Analysis

### 👩‍🦰 Survival by Gender

- **Females**: ~74% survival  
- **Males**: ~19% survival

### 💼 Survival by Passenger Class

- **Class 1**: ~63% survived  
- **Class 2**: ~47% survived  
- **Class 3**: ~24% survived

### ⚓ Survival by Embarked Port

- **Cherbourg (C)** passengers had highest survival  
- **Southampton (S)** passengers had the lowest

---

## 🧮 5. Group-Based Insights

### 📌 Survival Rate by Gender
```
female: 0.74
male:   0.19
```

### 📌 Survival Rate by Class
```
1st Class: 0.63
2nd Class: 0.47
3rd Class: 0.24
```

### 📌 Survival Rate by Gender and Class
```
female, 1st: 0.97
female, 2nd: 0.92
female, 3rd: 0.50

male, 1st: 0.37
male, 2nd: 0.15
male, 3rd: 0.13
```

---

## 🔥 6. Correlation Heatmap (Numerical Features)

| Feature        | Correlation with Survived |
|----------------|----------------------------|
| Sex (female)   | **+0.54**                  |
| Pclass         | **–0.34**                  |
| Fare           | +0.26                      |
| Age            | –0.08                      |

**Interpretation**:  
Being **female**, in a **higher class**, or paying a **higher fare** increased survival chances.  
**Age** showed weak correlation but can be helpful when combined with class or gender.

---

## ✅ 7. Conclusion & Insights

- **Gender is the strongest predictor**: females had a much higher survival rate.
- **1st class passengers** had the highest survival.
- **Cherbourg embarkation** and **higher fare** values were also associated with better survival.
- **Age** had weak correlation but may still be useful in combination with other features.

---
