# Mobile Price Prediction Using Linear Regression (Machine Learning)

This project builds a **regression** model to predict the **mobile phone price** based on key specifications like **RAM, Storage, and Battery capacity**. It follows the standard ML workflow:

**Problem Statement → Selection of Data → Collection of Data → EDA → Train/Test Split → Model Selection → Evaluation Metric**

---

## Problem Statement
Mobile prices vary based on hardware specifications.  
The goal of this project is to predict the **mobile price (₹)** using phone features.

**Input Features:**
- `RAM_GB`
- `Storage_GB`
- `Battery_mAh`

**Output:**
- Predicted Mobile Price (₹)

---

## Selection of Data
**Dataset Type Used:** Structured tabular dataset (numeric features)

Why this dataset is suitable:
- Clear regression target (`Price`)
- Features are numeric and easy to model
- Good beginner project for understanding regression

---

## Collection of Data
In this project, the dataset is created inside the code as a sample dictionary and converted into a DataFrame using `pandas`.  
(The same workflow works with real datasets loaded using `pd.read_csv()`.)

---

## EDA (Exploratory Data Analysis)
EDA is kept simple to confirm the dataset before training:
- Preview the dataset (`df.head()`)
- Confirm feature columns and target column (`Price`)
- Understand basic value ranges for RAM, storage, battery, and price

---

## Dividing Training and Testing
The dataset is split using `train_test_split`:
- Training set: model learns relationships
- Testing set: model is evaluated on unseen data

---

## Model Selection
**Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)

Why Linear Regression:
- Simple baseline model for numeric regression problems
- Easy to train and interpret for beginners
- Works well when relationships are roughly linear

---

## Evaluation Metric (Used in this Project)
This project uses **R² Score** (`r2_score`) to evaluate model performance.

Simple meaning:
- R² shows how well the model fits the test data
- Higher R² means predictions are closer to actual prices

Used in code:
- `r2_score(y_test, y_pred)`

---

## Main Libraries Used (and why)

1. `pandas`  
   - Creates and manages the dataset as a DataFrame.

2. `numpy`  
   - Supports numerical operations and array handling.

3. `sklearn.model_selection.train_test_split`  
   - Splits the dataset into training and testing sets.

4. `sklearn.linear_model.LinearRegression`  
   - Trains the regression model.

5. `sklearn.metrics.r2_score`  
   - Evaluates model performance using R² score.

---

## Output
- Printed **R² Score** for model performance
- Predicted mobile price for a new phone input (example: `[8, 256, 5000]`)

---

## Developer
Grishma C.D
