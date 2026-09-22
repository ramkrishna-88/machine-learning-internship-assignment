# Week 2 – Machine Learning Assignments

This repository contains the Week 2 Machine Learning assignments implemented in Python using **Scikit-learn, Pandas, Matplotlib, and Seaborn**.

## 📌 Assignments

### 1. Linear Regression – House Price Prediction

A Linear Regression model is trained on a housing dataset to predict house prices.

**Features used:**
- `bedrooms`
- `bathrooms`
- `stories`
- `parking`

**Target:**
- `price`

**Steps performed:**
1. Load the Housing dataset.
2. Select input features and target variable.
3. Split the dataset into training and testing sets.
4. Train a Linear Regression model.
5. Predict house prices.
6. Calculate Mean Squared Error (MSE).
7. Calculate R² Score.
8. Compare actual and predicted prices using a scatter plot.

### 2. Logistic Regression – Titanic Survival Prediction

A Logistic Regression model is used to predict whether a passenger survived the Titanic disaster.

**Features used:**
- `Pclass`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Fare`

**Target:**
- `Survived`

**Steps performed:**
1. Load the Titanic dataset.
2. Handle missing values in `Age` and `Fare`.
3. Convert `Sex` into numerical values.
4. Select input features and target.
5. Split the dataset into training and testing sets.
6. Train a Logistic Regression model.
7. Predict passenger survival.
8. Calculate accuracy.
9. Generate a confusion matrix.
10. Plot the confusion matrix using a heatmap.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📦 Installation

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## 📁 Project Structure

```text
Week-2-Machine-Learning/
│
├── Untitled.ipynb
├── Housing.csv
├── Titanic-Dataset.csv
└── README.md
```

> Keep the dataset files in the appropriate location or update the file paths in the notebook before running it.

## ▶️ How to Run

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open `Untitled.ipynb` in Jupyter Notebook or VS Code.
4. Make sure `Housing.csv` and `Titanic-Dataset.csv` are available.
5. Run the notebook cells in order.

## 📊 Evaluation Metrics

### Linear Regression
- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted house prices.
- **R² Score:** Measures how well the regression model explains the variation in house prices.

### Logistic Regression
- **Accuracy:** Measures the proportion of correct survival predictions.
- **Confusion Matrix:** Shows actual and predicted survival classes.

## 📈 Visualizations

The notebook includes:

- Actual vs Predicted House Prices scatter plot
- Logistic Regression Confusion Matrix heatmap

## 🎯 Learning Outcomes

After completing these assignments, you will understand:

1. How to prepare datasets for machine learning.
2. How to split data into training and testing sets.
3. How to build a Linear Regression model.
4. How to build a Logistic Regression model.
5. How to evaluate machine learning models using appropriate metrics.
6. How to visualize model predictions and classification results.

## 👨‍💻 Author

**Ram Krishna**

Machine Learning & AI Student

---

⭐ If you find this project useful, consider giving the repository a star.
