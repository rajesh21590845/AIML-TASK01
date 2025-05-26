# AIML-TASK01
# Titanic Dataset - Data Cleaning and Preprocessing

This project involves cleaning and preprocessing the Titanic dataset from Kaggle for machine learning tasks like survival prediction.

## 📂 Dataset Source

- **Kaggle Titanic Competition**  
  [https://www.kaggle.com/competitions/titanic/data](https://www.kaggle.com/competitions/titanic/data)
- Includes:
  - `train.csv`
  - `test.csv`
  - `gender_submission.csv` (sample submission)

## 🧼 Data Cleaning Steps

1. **Handling Missing Values:**
   - `Age`: Filled with median or predicted using other features.
   - `Cabin`: Dropped or filled with 'Unknown'.
   - `Embarked`: Filled with mode ('S').
   - `Fare`: Filled with median (in test set).

2. **Dropping Irrelevant Features:**
   - Removed columns such as:
     - `PassengerId`
     - `Ticket`
     - `Cabin` (if too sparse)

3. **Feature Engineering:**
   - Extracted `Title` from `Name` and grouped rare titles.
   - Created `FamilySize` = `SibSp` + `Parch` + 1
   - Created `IsAlone` = 1 if `FamilySize == 1`, else 0
   - Binned `Fare` and `Age` into categorical ranges.

4. **Encoding Categorical Variables:**
   - `Sex`, `Embarked`, `Title`, etc. encoded using:
     - Label Encoding or
     - One-Hot Encoding (depending on model choice)

## 🔍 Exploratory Data Analysis (EDA)

- Analyzed survival rate based on:
  - Gender
  - Pclass
  - Age bins
  - Family size
  - Title

## 🧠 Preprocessing for Machine Learning

- Standardized or normalized features as needed.
- Split dataset into features (`X`) and target (`y`).
- Ready for use with models like:
  - Logistic Regression
  - Random Forest
  - Support Vector Machine
  - XGBoost, etc.

## 🛠 Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib / seaborn (for EDA)
  - scikit-learn

## 🚀 Usage

```bash
# Clone repo
git clone https://github.com/rajesh21590845/AIML-TASK01.git
cd AIML-TASK01

# Run preprocessing script
python titanic_preprocessing.py
