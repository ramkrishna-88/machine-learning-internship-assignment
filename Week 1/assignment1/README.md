# Titanic Survival Prediction – Data Cleaning Project

## 📌 Overview

This project is part of **Week 1 – Machine Learning Fundamentals + Data Preprocessing**.  
The main goal is to clean and preprocess the **Titanic dataset** so that it can be used for further machine learning tasks.

The project focuses on:

- Loading and exploring a dataset using Pandas
- Understanding basic statistics
- Handling missing data
- Encoding categorical variables
- Visualizing the age distribution
- Saving the cleaned dataset as a CSV file

## 🎯 Objectives

1. Load the Titanic dataset using Pandas.
2. Explore the dataset using `.info()` and `.describe()`.
3. Identify and handle missing values.
4. Apply median/mean imputation where appropriate.
5. Encode the `Sex` column using `LabelEncoder`.
6. Encode the `Embarked` column using `OneHotEncoder`.
7. Visualize the distribution of passenger ages.
8. Export the cleaned dataset as a new CSV file.

## 📂 Dataset

The project uses the **Titanic Dataset** from Kaggle.

The dataset commonly contains columns such as:

- `PassengerId`
- `Survived`
- `Pclass`
- `Name`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Ticket`
- `Fare`
- `Cabin`
- `Embarked`

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / VS Code

## 📦 Installation

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/titanic-data-cleaning.git
```

### 2. Open the project folder

```bash
cd titanic-data-cleaning
```

### 3. Place the Titanic dataset in the project folder

Make sure the dataset file is named:

```text
train.csv
```

### 4. Run the notebook or Python file

Open the project in Jupyter Notebook or VS Code and run the code cells from beginning to end.

## 🔄 Data Preprocessing Steps

### 1. Load Dataset

```python
df = pd.read_csv("train.csv")
```

### 2. Explore Dataset

```python
df.info()
df.describe()
```

### 3. Handle Missing Values

`Age` is filled using median imputation:

```python
df["Age"] = df["Age"].fillna(df["Age"].median())
```

`Embarked` is filled using its mode:

```python
df["Embarked"] = df["Embarked"].fillna(
    df["Embarked"].mode()[0]
)
```

Missing `Cabin` values are represented as:

```python
df["Cabin"] = df["Cabin"].fillna("Unknown")
```

### 4. Encode Categorical Variables

`Sex` is encoded using `LabelEncoder`:

```python
from sklearn.preprocessing import LabelEncoder

encoder = LabelEncoder()
df["Sex"] = encoder.fit_transform(df["Sex"])
```

`Embarked` is encoded using `OneHotEncoder`:

```python
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder(
    sparse_output=False,
    handle_unknown="ignore"
)

encoded = encoder.fit_transform(df[["Embarked"]])
```

The resulting encoded columns are added to the dataset and the original `Embarked` column is removed.

### 5. Visualize Age Distribution

```python
plt.figure(figsize=(10, 6))

sns.histplot(
    df["Age"],
    bins=30,
    kde=True
)

plt.title("Age Distribution of Titanic Passengers")
plt.xlabel("Age")
plt.ylabel("Number of Passengers")

plt.show()
```

## 📊 Output

After preprocessing, the cleaned dataset is saved as:

```text
titanic_cleaned.csv
```

The project also produces an age-distribution visualization.

## 📁 Project Structure

```text
titanic-data-cleaning/
│
├── train.csv
├── titanic_cleaned.csv
├── Titanic_Data_Cleaning.ipynb
├── README.md
└── requirements.txt
```

## 📚 Learning Outcomes

After completing this project, you will understand:

- Basic machine learning data preprocessing
- Dataset exploration with Pandas
- Missing-value detection and imputation
- Label encoding
- One-hot encoding
- Basic data visualization
- Saving processed datasets for machine learning

## 👨‍💻 Author

**Your Name**

GitHub: `https://github.com/your-username`

## 📄 Project Type

**Machine Learning & AI – Week 1 Assignment**

**Topic:** ML Fundamentals + Data Preprocessing

**Mini Project:** Titanic Survival Prediction – Data Cleaning Project
