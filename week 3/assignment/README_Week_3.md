# Week 3 – Unsupervised Learning

This repository contains the **Week 3 Machine Learning & AI assignments** based on the provided Week 3 worksheet.

## 📌 Week 3 Focus

- K-Means Clustering
- PCA (Principal Component Analysis)
- Clustering Visualization
- Dimensionality Reduction

## 📝 Assignments

### Assignment 1: K-Means Clustering on Iris Dataset

Perform K-Means clustering on the Iris dataset and visualize the clusters.

**Dataset:** `Iris.csv`

**Numerical features used:**
- `SepalLengthCm`
- `SepalWidthCm`
- `PetalLengthCm`
- `PetalWidthCm`

**Number of clusters:**
- `k = 3`

**Steps performed:**
1. Load the Iris dataset.
2. Select the four numerical features.
3. Apply K-Means clustering with 3 clusters.
4. Add the predicted cluster labels to the dataset.
5. Display the cluster labels.
6. Visualize the clusters using a scatter plot.

### Assignment 2: PCA – Dimensionality Reduction

Apply PCA to reduce the dimensions of the Iris dataset.

**Dataset:** `Iris.csv`

**Original dimensions:**
- 4 numerical features

**Reduced dimensions:**
- Principal Component 1
- Principal Component 2

**Steps performed:**
1. Load the Iris dataset.
2. Select the four numerical features.
3. Standardize the features using `StandardScaler`.
4. Apply PCA with 2 components.
5. Display the reduced dataset.
6. Display the explained variance ratio.
7. Visualize the PCA-transformed data.

## 🛠️ Technologies Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## 📦 Installation

Install the required libraries:

```bash
pip install pandas matplotlib scikit-learn jupyter
```

## 📁 Project Structure

```text
Week-3/
│
├── Iris.csv
├── Week_3.ipynb
└── README.md
```

## ▶️ How to Run

1. Download or clone the repository.
2. Install the required libraries.
3. Open the notebook in Jupyter Notebook or VS Code.
4. Make sure `Iris.csv` is available.
5. Update the dataset path if required.
6. Run the notebook cells in order.

## 📊 Visualizations

### K-Means Clustering
A scatter plot is used to visualize the clusters created by the K-Means algorithm.

### PCA
A scatter plot is used to visualize the Iris dataset after reducing its four numerical dimensions to two principal components.

## 🎯 Learning Outcomes

After completing these assignments, you will understand:

1. How K-Means clustering works on an unlabeled dataset.
2. How to select numerical features for clustering.
3. How to visualize clustering results.
4. How PCA reduces the number of dimensions.
5. How standardization is used before PCA.
6. How to visualize data after dimensionality reduction.

## 👨‍💻 Author

**Ram Krishna**

Machine Learning & AI Student
