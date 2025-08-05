# Car Price Prediction Project

This project aims to build a machine learning model to **predict used car prices** based on features such as fuel type, transmission, age, power, and more.

## 📌 Objective

The goal is to develop and evaluate different regression models to find the most accurate one for predicting car prices. This includes:

- Performing **exploratory data analysis (EDA)** to understand data distribution and relationships.
- **Preprocessing** data using pipelines (handling missing values, scaling, encoding).
- Applying a **log transformation** to normalize the target (`selling_price`).
- Using **regression models** (Linear Regression, Random Forest, Gradient Boosting).
- Validating model performance using **K-Fold cross-validation**.
- Comparing models based on **MAE**, **MSE**, and **R²** metrics.

## 📊 Dataset

- The dataset is a CSV file named `car.csv`.
- It includes features such as:
  - `year` (manufacturing year)
  - `fuel`, `transmission`, `seller_type` (categorical)
  - `max_power`, `km_driven`, `Mileage` (numerical)
  - `selling_price` (target)

## 🛠️ Models Used

- **Linear Regression**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

Each model was evaluated using **5-fold cross-validation**, and performance was averaged to reduce variance in evaluation.

## ⚙️ Key Techniques

- **Data Cleaning**: Removed irrelevant columns like `name`, `Unnamed: 0`.
- **Feature Engineering**: Converted `year` to `age`, handled missing values.
- **Preprocessing Pipeline**:
  - `SimpleImputer` for missing values
  - `StandardScaler` for numeric features
  - `OneHotEncoder` for categorical features
- **Performance Metrics**:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - R² Score

## 📈 Results

The models were compared based on their average performance across folds. The results help identify which model generalizes better to unseen data.

---

> This project was built to understand how different regression techniques perform in predicting car prices, how pipelines improve preprocessing, and why proper evaluation (like cross-validation) matters in real-world applications.

