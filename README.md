# 🤖 Machine Learning Projects

A collection of practical **Machine Learning projects implemented in Python**, covering regression, classification, exploratory data analysis, model evaluation, and statistical analysis.

This repository demonstrates the application of Machine Learning algorithms to real-world datasets, with a focus on understanding the complete workflow from **data preprocessing → model building → prediction → evaluation → interpretation**.

---

## 📌 Projects

### 🏠 1. House Price Prediction

A regression-based Machine Learning project that predicts the **median value of houses** using the Boston Housing dataset.

#### 🔍 Techniques Used

* Exploratory Data Analysis
* Data visualization
* Simple Linear Regression
* Multiple Linear Regression
* Model prediction
* R² evaluation
* Regression coefficient analysis
* Ordinary Least Squares (OLS)

#### 📊 Features Used

* `RM` — Average number of rooms
* `LSTAT` — Lower-status population percentage
* `PTRATIO` — Pupil-teacher ratio

#### 📈 Results

| Model                      | Features             | R² Score |
| -------------------------- | -------------------- | -------: |
| Simple Linear Regression   | RM                   |   0.5525 |
| Multiple Linear Regression | RM + LSTAT + PTRATIO |   0.6509 |
| OLS                        | RM + LSTAT + PTRATIO |    0.679 |

The project demonstrates how adding relevant features can improve predictive performance compared with using a single feature.

---

### 📞 2. Telco Customer Churn Prediction

A **classification project using Logistic Regression** to predict whether a telecom customer is likely to churn.

The project works with a Telco Customer Churn dataset and demonstrates how Machine Learning can be applied to customer-retention problems.

#### 🎯 Objective

Predict customer churn based on customer-related information and identify patterns associated with customers leaving a telecom service.

#### 🔍 Techniques

* Data loading
* Data exploration
* Data preprocessing
* Feature analysis
* Logistic Regression
* Classification
* Model prediction
* Model evaluation

#### 💡 Business Use Case

Customer churn prediction can help telecom companies:

* Identify customers at risk of leaving
* Understand customer behavior
* Improve customer retention
* Develop targeted offers
* Reduce customer acquisition costs

---

# 🧠 Machine Learning Workflow

Both projects follow a structured Machine Learning workflow:

```text
                ┌─────────────────┐
                │     Dataset     │
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Data Exploration│
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Preprocessing   │
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Feature         │
                │ Selection       │
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Train/Test Split│
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Model Training  │
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │   Prediction    │
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Model Evaluation│
                └────────┬────────┘
                         ↓
                ┌─────────────────┐
                │ Interpretation  │
                └─────────────────┘
```

---

# 🛠️ Technologies Used

| Technology          | Usage                     |
| ------------------- | ------------------------- |
| 🐍 Python           | Programming               |
| 🐼 Pandas           | Data manipulation         |
| 🔢 NumPy            | Numerical computation     |
| 📊 Matplotlib       | Visualization             |
| 🎨 Seaborn          | Statistical visualization |
| 🤖 Scikit-learn     | Machine Learning          |
| 📈 Statsmodels      | Statistical analysis      |
| 📓 Jupyter Notebook | Development environment   |

---

# 📂 Repository Structure

```text
ML-project/
│
├── 📓 Logistic_Regression_on_Telco_Dataset.ipynb
│   └── Telco Customer Churn Classification
│
├── 📓 Machine Learning Project — House Price Prediction
│   └── House Price Regression Analysis
│
└── 📄 README.md
    └── Project documentation
```

> The notebook filenames currently present in the repository are visible on the `main` branch.

---

# 📊 Machine Learning Concepts Covered

This repository provides hands-on experience with:

### Regression

* Simple Linear Regression
* Multiple Linear Regression
* Regression prediction
* Regression coefficients
* R² evaluation
* OLS regression

### Classification

* Logistic Regression
* Binary classification
* Customer churn prediction
* Classification model evaluation

### Data Science

* Data loading
* Data exploration
* Feature selection
* Data visualization
* Train/test splitting
* Model interpretation

---

# 📈 House Price Prediction

The House Price project predicts `MEDV`, the median value of owner-occupied homes.

The Multiple Linear Regression model uses:

```text
MEDV ~ RM + LSTAT + PTRATIO
```

The model achieved an R² of approximately **0.651** on the evaluated test split, while the OLS analysis reports an R² of **0.679**.

---

# 📞 Telco Customer Churn

The Telco project applies **Logistic Regression** to a customer churn problem.

The notebook contains approximately **6,977 lines / 1 MB** of notebook content, indicating a substantially detailed analysis rather than a minimal demonstration.

The main goal is to classify customers into:

```text
                 Customer
                    │
          ┌─────────┴─────────┐
          ↓                   ↓
       Churned            Not Churned
          │                   │
          └─────────┬─────────┘
                    ↓
             Retention Strategy
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/KishanHP1808/ML-project.git
```

## 2. Navigate to the Project

```bash
cd ML-project
```

## 3. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn statsmodels jupyter
```

## 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open either notebook and execute the cells sequentially.

---

# 💻 Run with Google Colab

You can also upload the `.ipynb` files to **Google Colab** and run them without setting up a local Python environment.

---

# 🔮 Future Improvements

This repository can be expanded with more advanced Machine Learning techniques.

### 📊 Model Improvements

* [ ] Cross-validation
* [ ] Hyperparameter tuning
* [ ] Feature scaling
* [ ] Feature engineering
* [ ] Handling class imbalance
* [ ] Outlier detection
* [ ] Missing-value treatment

### 🤖 Advanced Models

* [ ] Decision Tree
* [ ] Random Forest
* [ ] XGBoost
* [ ] Gradient Boosting
* [ ] Support Vector Machine
* [ ] K-Nearest Neighbors
* [ ] Neural Networks

### 📈 Evaluation

* [ ] Accuracy
* [ ] Precision
* [ ] Recall
* [ ] F1-score
* [ ] ROC-AUC
* [ ] Confusion Matrix
* [ ] MAE
* [ ] MSE
* [ ] RMSE

### 🚀 Deployment

* [ ] Streamlit application
* [ ] Flask API
* [ ] REST API
* [ ] Interactive prediction interface
* [ ] Model serialization with Joblib
* [ ] Cloud deployment

---

# 🎓 Learning Outcomes

Through these projects, the following practical skills are demonstrated:

* Understanding Machine Learning workflows
* Working with real-world datasets
* Data preprocessing and exploration
* Regression modeling
* Classification modeling
* Feature selection
* Model training
* Making predictions
* Evaluating model performance
* Interpreting Machine Learning models
* Statistical analysis
* Python-based data science

---

# 👨‍💻 Author

**Kishan H.P**

Machine Learning & Web Development Enthusiast

### 🔗 GitHub

https://github.com/KishanHP1808

---

## ⭐ Support

If you find this repository useful, consider giving it a ⭐ on GitHub.

---

## 📄 License

This repository is intended for **educational and learning purposes**.
