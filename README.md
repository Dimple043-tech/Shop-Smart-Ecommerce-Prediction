# Shop Smart E-Commerce Purchase Prediction

## Project Overview

This project aims to predict whether an online visitor will make a purchase based on their browsing behavior during an e-commerce session.

The dataset contains user interaction metrics such as page visits, time spent on different pages, bounce rates, exit rates, visitor type, and other session-related information.

A Decision Tree Classification model was developed to classify visitors into:

* Purchase (Revenue = True)
* No Purchase (Revenue = False)

The project includes Exploratory Data Analysis (EDA), data preprocessing, handling class imbalance, model training, pruning, and performance evaluation using the F1 Score.

---

## Problem Statement

Online retailers often struggle to identify which visitors are likely to make a purchase.

The objective of this project is to build a machine learning model that predicts purchase intent based on user session behavior.

---

## Dataset Information

The dataset contains 12,330 records and 18 features.

### Key Features

| Feature                 | Description                            |
| ----------------------- | -------------------------------------- |
| Administrative          | Number of administrative pages visited |
| Administrative_Duration | Time spent on administrative pages     |
| Informational           | Number of informational pages visited  |
| Informational_Duration  | Time spent on informational pages      |
| ProductRelated          | Number of product pages visited        |
| ProductRelated_Duration | Time spent on product pages            |
| BounceRates             | Percentage of single-page sessions     |
| ExitRates               | Exit probability from pages            |
| PageValues              | Value assigned to visited pages        |
| SpecialDay              | Closeness to a special shopping day    |
| Month                   | Month of visit                         |
| OperatingSystems        | Operating system used                  |
| Browser                 | Browser used                           |
| Region                  | User region                            |
| TrafficType             | Source of traffic                      |
| VisitorType             | New or Returning visitor               |
| Weekend                 | Weekend visit indicator                |
| Revenue                 | Target variable                        |

---

## Machine Learning Workflow

### 1. Data Understanding

* Loaded dataset
* Checked structure and feature types
* Identified target variable

### 2. Exploratory Data Analysis

* Distribution analysis
* Correlation analysis
* Target class distribution visualization

### 3. Data Preprocessing

* Encoded categorical variables
* Converted boolean features into numerical format
* Checked for missing values
* Checked for duplicate records

### 4. Handling Imbalanced Data

The dataset is imbalanced:

* Non-Purchase ≈ 84.5%
* Purchase ≈ 15.5%

To address this issue:

* Used `class_weight='balanced'`
* Evaluated model using F1 Score

### 5. Model Development

Implemented:

* Decision Tree Classifier
* Hyperparameter Tuning
* Cost Complexity Pruning

### 6. Model Evaluation

Performance metrics used:

* Confusion Matrix
* Recall
* F1 Score

Target Benchmark:

F1 Score ≥ 0.55

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Project Structure

```text
Shop-Smart-Ecommerce-Prediction/
│
├── shop_smart_ecommerce.csv
├── shop_smart.ipynb
├── README.md

```

---

## Results

The Decision Tree model successfully predicts purchase intent based on user session behavior.

Important features influencing purchase decisions include:

* PageValues
* ProductRelated
* ProductRelated_Duration
* BounceRates
* ExitRates

---

## Business Insights

* Users spending more time on product pages are more likely to purchase.
* Higher PageValues strongly indicate buying intent.
* Returning visitors have a higher probability of conversion.
* High Bounce Rates negatively affect purchases.

---

## Future Improvements

* Random Forest Classifier
* XGBoost Classifier
* Feature Engineering
* SMOTE for class imbalance
* Hyperparameter Optimization using GridSearchCV

---

## Author

Dimple Saxena

B.Tech Student | Machine Learning Enthusiast

