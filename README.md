<body>

# High Demand Prediction

## Project Overview

This project focuses on analyzing operational data and predicting whether a record represents **high demand**.

The project combines **data analysis, data preprocessing, supervised machine learning, unsupervised learning, and deep learning** to understand the dataset and build predictive models.

The project uses **Logistic Regression** and an **Artificial Neural Network (ANN)** for high-demand classification, while **K-Means Clustering** is used to identify groups of similar records.

---

## Objectives

- Analyze the available operational data.
- Understand the distribution and characteristics of the `load` variable.
- Handle missing and duplicate data.
- Create an additional feature to improve the representation of the data.
- Prepare numerical and categorical data for machine learning.
- Predict whether demand is high or not.
- Identify groups of similar records using clustering.
- Build an ANN for binary classification.
- Evaluate and compare the predictive models.

---

## Dataset

The project uses the dataset:

**`set_e.csv`**

The dataset contains **305 records** and the following attributes:

| Feature | Description |
|---|---|
| `record_id` | Unique identifier for each record |
| `temperature` | Temperature measurement |
| `occupancy` | Occupancy measurement |
| `runtime` | Runtime information |
| `load` | Load measurement |
| `group` | Categorical group information |
| `high_demand` | Target indicating whether the demand is high |

The dataset contains missing values in the `temperature` and `occupancy` features.

---

## Data Preparation

The project performs the following data preparation steps:

- Removal of the record identifier from the modeling data.
- Detection and removal of duplicate records.
- Handling of missing numerical values.
- Encoding of categorical information.
- Scaling of numerical features.
- Creation of an additional `engineered_feature` using the available `load` and `runtime` information.

These steps prepare the dataset for the machine learning and deep learning models.

---

## Exploratory Data Analysis

The project analyzes the `load` variable using descriptive statistics such as:

- Mean
- Median
- Standard deviation
- Sample size

A histogram with a KDE curve is also used to visualize the distribution of the load values.

---

## Feature Engineering

An additional feature called:

**`engineered_feature`**

is created from the relationship between:

- `load`
- `runtime`

This provides the models with an additional representation of the operational data.

---

## Machine Learning

### Logistic Regression

Logistic Regression is used as a supervised classification model to predict the `high_demand` target.

The model predicts two possible classes:

- High demand
- Not high demand

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## Unsupervised Learning

### K-Means Clustering

K-Means clustering is used to discover groups of similar records without using the target as the clustering objective.

Different numbers of clusters are examined using:

- Elbow Method
- Silhouette Score

The clustering analysis helps identify different patterns or groups present in the operational data.

---

## Deep Learning

### Artificial Neural Network

An Artificial Neural Network is developed for the same binary high-demand prediction task.

The network contains:

- Input layer
- Two hidden layers
- Output layer

The hidden layers use **ReLU** activation, while the output layer uses **Sigmoid** activation for binary classification.

The model is trained using:

- Adam optimizer
- Binary cross-entropy loss
- Accuracy as a training metric
- Validation data
- Early stopping

---

## Model Evaluation

The predictive models are evaluated using common classification metrics.

### Accuracy

Measures the overall percentage of correctly classified records.

### Precision

Measures how many records predicted as high demand are actually high demand.

### Recall

Measures how many actual high-demand records are correctly identified.

### F1-Score

Provides a combined measure of precision and recall.

### Confusion Matrix

Shows the number of:

- True Positives
- True Negatives
- False Positives
- False Negatives

The Logistic Regression and ANN models are compared using these evaluation metrics.

---

## Project Workflow

```text
Dataset
   ↓
Data Analysis
   ↓
Data Cleaning
   ↓
Missing Value Handling
   ↓
Duplicate Removal
   ↓
Feature Engineering
   ↓
Data Preprocessing
   ↓
   ┌───────────────────────┐
   │                       │
   ↓                       ↓
Logistic Regression    K-Means Clustering
   │
   ↓
Model Evaluation
   │
   ↓
Artificial Neural Network
   │
   ↓
Model Evaluation
   │
   ↓
Model Comparison
