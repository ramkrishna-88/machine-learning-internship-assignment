# Customer Segmentation using Clustering — Project Report

## 1. Introduction

Customer segmentation is the process of dividing customers into groups with similar characteristics or behavior. It can help organizations understand customer patterns and design more targeted business strategies.

This project applies the K-Means clustering algorithm to customer information such as age, annual income and spending score.

## 2. Problem Statement

A business has customer-level demographic and spending information but needs a simple way to identify groups of customers with similar behavior.

The objective is to build an unsupervised machine learning solution that groups customers and presents the groups through an interactive dashboard.

## 3. Dataset

The Week 4 project brief specifies the **Kaggle – Mall Customers Dataset**.

The expected attributes are:

- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

## 4. Objectives

- Load and inspect customer data.
- Clean missing or invalid numerical values.
- Select relevant clustering features.
- Standardize the features.
- Apply K-Means clustering.
- Inspect K using the elbow method and silhouette score.
- Visualize customer groups using age, income and spending score.
- Label clusters using spending behavior.
- Present business-oriented interpretations.
- Export segmented customer data.

## 5. Methodology

### Step 1 — Data Cleaning

Numerical fields are converted to numeric values and rows with missing values in the clustering features are removed. Duplicate rows are also removed.

### Step 2 — Feature Selection

The model uses:

- Age
- Annual Income (k$)
- Spending Score (1-100)

### Step 3 — Feature Scaling

StandardScaler is used before K-Means because the features have different numerical ranges.

### Step 4 — Choosing K

The project calculates:

**Inertia** for the elbow method.

**Silhouette Score** for an additional clustering-quality view.

### Step 5 — K-Means

For the assignment's three spending-level labels, the default final model uses:

```text
K = 3
```

K-Means assigns each customer to the nearest learned centroid.

### Step 6 — Segment Labels

Clusters are ordered by their mean spending score:

```text
lowest average spending → Low Spenders
middle average spending → Medium Spenders
highest average spending → High Spenders
```

The labels are descriptive names for the resulting clusters.

## 6. Visualizations

The application contains:

1. Age distribution
2. Income vs Spending Score
3. Age vs Spending Score
4. Elbow curve
5. Silhouette score curve
6. 3D Age-Income-Spending visualization
7. PCA two-dimensional visualization

## 7. Business Interpretation

### Low Spenders

This group has the lowest average spending score among the identified clusters.

Possible business uses include:
- retention campaigns
- introductory discounts
- product education
- personalized recommendations

### Medium Spenders

This group shows intermediate spending behavior.

Possible business uses include:
- cross-selling
- product bundles
- targeted promotions

### High Spenders

This group has the highest average spending score among the identified clusters.

Possible business uses include:
- loyalty programs
- premium product recommendations
- personalized customer engagement

## 8. Limitations

- Clustering results depend on the selected features.
- K-Means requires choosing K.
- Results can change when the dataset changes.
- Spending score is a dataset variable and should not automatically be treated as future spending.
- The segment labels are descriptive rather than predictive.

## 9. Future Scope

- Add purchase frequency and transaction value.
- Compare K-Means with hierarchical clustering and DBSCAN.
- Add automated model selection.
- Connect the dashboard to a live database.
- Add customer-level recommendations.
- Deploy the Streamlit application.
- Add authentication and role-based access for business users.

## 10. Conclusion

The project demonstrates a complete unsupervised machine learning pipeline for customer segmentation. K-Means is applied after data cleaning and feature scaling, and the resulting groups are analyzed using clustering diagnostics and visualizations.

The final Streamlit dashboard converts the ML workflow into an interactive business analytics application.
