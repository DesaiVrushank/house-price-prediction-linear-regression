# House Price Prediction Using Linear Regression and Regression Metrics

A Machine Learning project that predicts house prices using **Linear Regression** after performing data cleaning, exploratory data analysis, and feature engineering.

## 📌 Project Overview

This project is a continuation of the previous **House Price Analysis Using Exploratory Data Analysis and Feature Engineering** project.

The cleaned and prepared house price dataset is used to build a **Linear Regression** model for predicting house prices.

The project covers the complete basic Machine Learning workflow:

**Data Cleaning → Feature Engineering → Feature & Target Separation → Train-Test Split → Model Training → Prediction → Model Evaluation**

## 🎯 Objective

The objective of this project is to build a Linear Regression model that can predict house prices based on different house characteristics and evaluate the model using standard regression metrics.

## 📊 Dataset

The dataset contains the following features:

| Feature            | Description                          |
| ------------------ | ------------------------------------ |
| `area_sqft`        | Area of the house in square feet     |
| `bedrooms`         | Number of bedrooms                   |
| `age_years`        | Age of the house in years            |
| `distance_city_km` | Distance from the city in kilometers |
| `price_lakh`       | House price in lakhs                 |

Additional features created during feature engineering:

* `price_per_sqft`
* `sqft_per_bedroom`

> **Note:** `price_per_sqft` is created for feature engineering and analysis, but it is not used as an input feature for predicting `price_lakh` because it directly depends on the target variable and would cause target leakage.

## 🧹 Data Preparation

The dataset was checked and cleaned before training the Machine Learning model.

The following operations were performed:

* Missing value detection
* Duplicate detection and removal
* Invalid value detection
* Handling negative area values
* Handling invalid price values
* Missing value imputation
* Feature engineering
* Feature and target separation

After cleaning, the dataset contained **1,000 records**.

## 🔧 Feature Engineering

Two additional features were created:

### 1. Price Per Square Foot

```python
df["price_per_sqft"] = df["price_lakh"] / df["area_sqft"]
```

### 2. Square Feet Per Bedroom

```python
df["sqft_per_bedroom"] = df["area_sqft"] / df["bedrooms"]
```

For the Linear Regression model, `price_per_sqft` is excluded because it is calculated using the target variable `price_lakh`.

## 🤖 Machine Learning Model

### Linear Regression

Linear Regression is used to model the relationship between the input features and the house price.

The dataset is divided into:

* **Training data:** 80%
* **Testing data:** 20%

The model is trained on the training data and then used to predict house prices for unseen test data.

## 📈 Regression Evaluation Metrics

The Linear Regression model is evaluated using:

### MAE — Mean Absolute Error

Measures the average absolute difference between actual and predicted values.

### MSE — Mean Squared Error

Measures the average squared difference between actual and predicted values.

### RMSE — Root Mean Squared Error

Measures the square root of MSE and represents the prediction error in the same unit as the target.

### R² Score — R-squared

Measures how well the model explains the variation in the target variable.

### Adjusted R² Score

Adjusted R² considers the number of input features used by the model and provides a more balanced measure of model performance when multiple features are involved.

## 📊 Model Performance

The final model performance is evaluated using the following metrics:

| Metric            |         Value |
| ----------------- | ------------: |
| MAE               | To be updated |
| MSE               | To be updated |
| RMSE              | To be updated |
| R² Score          | To be updated |
| Adjusted R² Score | To be updated |

> The values above should be updated with the actual results obtained after running the final notebook.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Jupyter Notebook

## 📁 Project Structure

```text
house-price-prediction-linear-regression/
│
├── House_Price_Prediction_Using_Linear_Regression.ipynb
├── 02_house_price.csv
└── README.md
```

## ▶️ How to Run

### Using Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Upload `02_house_price.csv`.
3. Run the notebook cells sequentially.
4. The notebook will perform data preparation, train the Linear Regression model, generate predictions, and calculate regression metrics.

### Using Jupyter Notebook

Clone the repository:

```bash
git clone <your-github-repository-url>
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Open the notebook:

```bash
jupyter notebook
```

Then open:

```text
House_Price_Prediction_Using_Linear_Regression.ipynb
```

## 📚 Key Concepts Learned

* Exploratory Data Analysis (EDA)
* Data Cleaning & Preprocessing
* Missing Value Handling
* Duplicate Removal
* Invalid Value Detection
* Outlier Analysis
* Data Visualization
* Correlation Analysis
* Feature Engineering
* Feature and Target Separation
* Train-Test Split
* Linear Regression
* Model Training
* Model Prediction
* Regression Evaluation
* MAE
* MSE
* RMSE
* R² Score
* Adjusted R² Score
* Basic Machine Learning Workflow

## 🎓 Internship Project

This project was completed as part of my **Machine Learning Internship at Learn Depth Academy**.

The project helped strengthen my practical understanding of how data analysis and feature engineering can be extended into a Machine Learning model for prediction.

## 👨‍💻 Author

**Vrushank Desai**

Computer Engineering Student
Machine Learning & Data Science Learner

## 📄 License

This project is created for educational and internship purposes.
