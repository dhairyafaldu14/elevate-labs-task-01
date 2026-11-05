# elevate-labs-task-01
Data Cleaning and Preprocessing using Python and Pandas

# Task 1: Data Cleaning & Preprocessing

**AI & ML Internship – Elevate Labs**

## Objective
To clean and preprocess a raw dataset using Python and its data science libraries, making it suitable for Machine Learning applications.

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Dataset
**Titanic Dataset**

The dataset contains passenger information such as age, gender, ticket fare, family members, passenger class and survival status.

## Activities Performed

### 1. Data Loading and Exploration
- Imported the Titanic dataset using Pandas.
- Explored the dataset using `head()`, `shape()`, `info()` and `describe()`.
- Identified missing values and examined data types.

### 2. Handling Missing Values
- Filled missing values in the `Age` column using median imputation.
- Filled missing values in the `Embarked` column using mode imputation.
- Dropped the `Cabin` column because it contained a large number of missing values.
- Verified that no missing values remained.

### 3. Categorical Data Encoding
- Converted the `Sex` column into numerical values using mapping:
  - Male = 0
  - Female = 1
- Applied One-Hot Encoding to the `Embarked` column, creating:
  - `Embarked_C`
  - `Embarked_Q`
  - `Embarked_S`

### 4. Feature Scaling
Applied two feature scaling techniques to numerical features (`Age`, `Fare`, `SibSp` and `Parch`):

- **Normalization:** Used MinMaxScaler to scale values between 0 and 1.
- **Standardization:** Used StandardScaler to transform values to approximately zero mean and unit standard deviation.

### 5. Outlier Detection and Treatment
- Used boxplots to visualize potential outliers.
- Applied the Interquartile Range (IQR) method to identify outliers.
- Used IQR-based capping for the `Age` and `Fare` columns.
- Retained `SibSp` and `Parch` because their values represent valid passenger family counts.

## Project Structure

```text
Task-1-Data-Cleaning-Preprocessing/
│
├── Task_1_Data_Cleaning.ipynb
├── Titanic-Dataset.csv
├── Titanic_Cleaned_Dataset.csv
├── README.md
└── Task_1_Screenshots.pdf
