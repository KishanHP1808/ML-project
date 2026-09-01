# ML-project
# 🏠 Machine Learning Project — House Price Prediction

A practical Machine Learning project demonstrating **Exploratory Data Analysis, Simple Linear Regression, Multiple Linear Regression, prediction, model evaluation, and Ordinary Least Squares (OLS) statistical analysis** using Python.

The project uses the **Boston Housing dataset** to understand how different housing and socioeconomic factors influence house prices.

---

## 📌 Project Overview

This project explores the application of regression techniques to predict the **median value of owner-occupied homes (`MEDV`)**.

The analysis focuses on important variables such as:

* 🏡 Average number of rooms (`RM`)
* 📊 Lower status population percentage (`LSTAT`)
* 🏫 Pupil-teacher ratio (`PTRATIO`)

The project also demonstrates fundamental data analysis and visualization techniques using Python.

---

## 🎯 Objectives

The main objectives of this project are to:

* Understand and explore a real-world dataset
* Perform basic data analysis using Pandas
* Visualize relationships between variables
* Apply Simple Linear Regression
* Apply Multiple Linear Regression
* Generate house-price predictions
* Evaluate regression performance using R²
* Analyze model coefficients
* Perform statistical analysis using OLS
* Understand how individual features affect house prices

---

## 🗂️ Project Structure

```text
ML-project/
│
├── 📓 Untitled4.ipynb
│   └── Complete Machine Learning analysis
│
└── 📄 README.md
    └── Project documentation
```

---

## 🧰 Technologies & Libraries

| Technology      | Purpose                        |
| --------------- | ------------------------------ |
| 🐍 Python       | Programming language           |
| 🐼 Pandas       | Data manipulation and analysis |
| 🔢 NumPy        | Numerical computation          |
| 📊 Matplotlib   | Data visualization             |
| 🎨 Seaborn      | Statistical visualization      |
| 🤖 Scikit-learn | Machine Learning models        |
| 📈 Statsmodels  | Statistical / OLS analysis     |
| ☁️ Google Colab | Notebook execution             |

---

## 📊 Dataset

The project uses the **Boston Housing dataset** containing **506 observations and 14 columns**.

The target variable is:

```text
MEDV
```

`MEDV` represents the median value of owner-occupied homes.

### Important Features

| Feature   | Description                                          |
| --------- | ---------------------------------------------------- |
| `CRIM`    | Per-capita crime rate                                |
| `ZN`      | Proportion of residential land                       |
| `INDUS`   | Proportion of non-retail business acres              |
| `CHAS`    | Charles River dummy variable                         |
| `NOX`     | Nitric oxide concentration                           |
| `RM`      | Average number of rooms per dwelling                 |
| `AGE`     | Proportion of owner-occupied units built before 1940 |
| `DIS`     | Distance to employment centres                       |
| `RAD`     | Accessibility to radial highways                     |
| `TAX`     | Property-tax rate                                    |
| `PTRATIO` | Pupil-teacher ratio                                  |
| `B`       | Demographic-related variable                         |
| `LSTAT`   | Lower-status population percentage                   |
| `MEDV`    | Median house value — target                          |

The notebook loads the Boston Housing data directly from a public dataset URL.

---

# 🔬 Machine Learning Workflow

The project follows a basic Machine Learning workflow:

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Data Visualization
   ↓
Feature Selection
   ↓
Train/Test Split
   ↓
Simple Linear Regression
   ↓
Multiple Linear Regression
   ↓
Prediction
   ↓
Model Evaluation
   ↓
OLS Statistical Analysis
```

---

## 1️⃣ Data Exploration

The notebook performs several exploratory operations including:

```python
df.head()
df.tail()
df.shape
df.columns
df.dtypes
df.info()
```

These operations help understand:

* Dataset dimensions
* Feature names
* Data types
* Number of observations
* Dataset structure

---

# 📈 Simple Linear Regression

Simple Linear Regression is implemented using:

```text
RM → MEDV
```

Where:

* `RM` = Average number of rooms
* `MEDV` = Median house value

The dataset is divided into training and testing sets using:

```python
test_size = 0.30
```

The model is trained using:

```python
LinearRegression()
```

### Result

The Simple Linear Regression model achieved:

```text
R² Score: 0.5525
```

This means that the number of rooms alone explains approximately **55.25% of the variation** in the target variable for the evaluated test split.

A regression-line visualization is also generated to compare the actual observations with the fitted relationship.

---

# 📊 Multiple Linear Regression

The project then improves the prediction by using multiple features:

```text
RM
LSTAT
PTRATIO
```

The model can be represented conceptually as:

```text
MEDV = β₀ + β₁(RM) + β₂(LSTAT) + β₃(PTRATIO)
```

The model is implemented using:

```python
mlr = LinearRegression()
mlr.fit(X_train, y_train)
```

### Model Performance

```text
R² Score: 0.6509
```

The Multiple Linear Regression model explains approximately **65.09% of the variation** in the test data.

---

## 📌 Model Coefficients

The trained model produced the following coefficients:

| Feature   | Coefficient |
| --------- | ----------: |
| `RM`      |     +4.4616 |
| `LSTAT`   |     -0.6082 |
| `PTRATIO` |     -0.8629 |

### Interpretation

**RM → Positive effect**

More rooms are associated with higher predicted house values.

**LSTAT → Negative effect**

Higher `LSTAT` values are associated with lower predicted house values.

**PTRATIO → Negative effect**

Higher pupil-teacher ratios are associated with lower predicted house values in this model.

> Note: These coefficients represent associations learned by the regression model and should not automatically be interpreted as causal effects.

---

# 📋 Prediction Analysis

The project creates a prediction table containing:

```text
Actual | Predicted
```

Example:

| Actual | Predicted |
| -----: | --------: |
|   23.6 |     26.92 |
|   32.4 |     30.94 |
|   13.6 |     16.48 |
|   22.8 |     25.25 |
|   16.1 |     18.28 |

The notebook generates predictions for the test set and compares them against actual values.

---

# 📐 OLS Statistical Analysis

In addition to Scikit-learn regression, the project uses **Statsmodels OLS** for a statistical interpretation of the model.

The formula used is:

```text
MEDV ~ RM + LSTAT + PTRATIO
```

The OLS model achieved:

```text
R²           = 0.679
Adjusted R²  = 0.677
F-statistic  = 353.3
```

### OLS Coefficients

| Variable  | Coefficient | Interpretation        |
| --------- | ----------: | --------------------- |
| Intercept |     18.5671 | Baseline model value  |
| RM        |     +4.5154 | Positive relationship |
| LSTAT     |     -0.5718 | Negative relationship |
| PTRATIO   |     -0.9307 | Negative relationship |

All three predictors have very small reported p-values in the fitted OLS model, indicating strong statistical evidence of association within this model.

---

# 📊 Model Comparison

| Model                      | Features             |         R² |
| -------------------------- | -------------------- | ---------: |
| Simple Linear Regression   | RM                   | **0.5525** |
| Multiple Linear Regression | RM + LSTAT + PTRATIO | **0.6509** |
| OLS                        | RM + LSTAT + PTRATIO | **0.6790** |

The results demonstrate that using multiple relevant features provides a better fit than relying on `RM` alone.

---

# 🚀 How to Run

### Option 1 — Google Colab

Open the notebook directly in Google Colab and run the cells sequentially.

### Option 2 — Run Locally

Clone the repository:

```bash
git clone https://github.com/KishanHP1808/ML-project.git
```

Navigate into the project:

```bash
cd ML-project
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
Untitled4.ipynb
```

and execute the cells.

---

# 📁 Repository

**GitHub Repository**

https://github.com/KishanHP1808/ML-project

---

# 🔮 Future Improvements

The project can be extended with:

* [ ] Feature scaling and preprocessing
* [ ] Missing-value handling
* [ ] Outlier detection
* [ ] Correlation heatmap
* [ ] Residual analysis
* [ ] MAE, MSE and RMSE evaluation
* [ ] Cross-validation
* [ ] Ridge Regression
* [ ] Lasso Regression
* [ ] Random Forest Regression
* [ ] Gradient Boosting
* [ ] Hyperparameter tuning
* [ ] Model comparison dashboard
* [ ] Interactive house-price prediction interface
* [ ] Model deployment using Streamlit or Flask
* [ ] Model serialization using Joblib/Pickle

---

# 🧠 Key Learnings

Through this project, the following concepts are demonstrated:

* Data loading and exploration
* Exploratory Data Analysis
* Feature selection
* Train/test splitting
* Regression modeling
* Prediction
* R² model evaluation
* Regression coefficients
* Statistical significance
* OLS regression
* Model interpretation
* Data visualization

---

# 👨‍💻 Author

**Kishan H.P**

Machine Learning & Web Development Enthusiast

GitHub:
https://github.com/KishanHP1808

---

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐ on GitHub.

---

## 📄 License

This project is intended for **educational and learning purposes**.
