# Titanic Survival Prediction

## Overview
This project predicts whether a passenger survived the Titanic disaster using machine learning models.  
We preprocess the Titanic dataset, perform feature engineering, and train classification models such as **Random Forest** and **Gradient Boosting** to achieve strong predictive accuracy.

---

## Dataset
The dataset used is the [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data) with the following key columns:
- `Survived` — Target variable (0 = No, 1 = Yes)
- `Pclass` — Passenger class (1, 2, 3)
- `Sex` — Passenger gender
- `Age` — Passenger age
- `SibSp` — Number of siblings/spouses aboard
- `Parch` — Number of parents/children aboard
- `Fare` — Ticket fare
- `Embarked` — Port of Embarkation (C, Q, S)

---

## Preprocessing Steps
1. **Drop unnecessary columns:**
   - `PassengerId`, `Name`, `Ticket`, `Cabin`
2. **Handle missing values:**
   - Fill missing `Age` with mean age
   - Drop rows with missing `Embarked`
3. **Convert categorical to numerical:**
   - `Sex` → 0 (female), 1 (male)
   - `Embarked` → 0 (S), 1 (C), 2 (Q)
4. **Feature scaling** (optional)

---

## Models Used
- **Random Forest Classifier** (baseline)
- **Gradient Boosting Classifier** (best performer)

---

## Results

### Random Forest (Tuned)
- Train Accuracy: 86.24%
- Test Accuracy: 79.33%
- Recall for survivors: 66%

### Gradient Boosting
- Train Accuracy: 89.75%
- Test Accuracy: 81.01%
- Recall for survivors: 69%

---

## Dependencies
Install the required libraries:
```bash
pip install pandas scikit-learn

