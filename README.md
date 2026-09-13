# Sales Prediction Using Python

## Project Overview

This project predicts product sales based on advertising spending across three media channels:

* TV
* Radio
* Newspaper

The project uses machine learning regression models to analyze the relationship between advertising spend and sales. It compares multiple models and evaluates their performance to determine which model gives the best predictions.

## Why This Project?

Advertising is an important part of business decision-making. Companies spend money on different advertising channels, but they need to understand which channels have the greatest effect on product sales.

The purpose of this project is to:

* Analyze the relationship between advertising and sales
* Predict future sales based on advertising spending
* Compare different machine learning models
* Identify the most important advertising channel
* Understand how data can support better marketing decisions

## Dataset

The dataset contains advertising spending and sales information.

Features:

| Feature   | Description                           |
| --------- | ------------------------------------- |
| TV        | Amount spent on TV advertising        |
| Radio     | Amount spent on Radio advertising     |
| Newspaper | Amount spent on Newspaper advertising |
| Sales     | Product sales value to be predicted   |

The target variable is:

```text
Sales
```

The input features are:

```text
TV
Radio
Newspaper
```

## Technologies Used

* Python
* pandas
* scikit-learn
* matplotlib
* seaborn
* Jupyter Notebook

## Project Workflow

The project follows these steps:

### 1. Data Loading

The advertising dataset is loaded using pandas.

### 2. Exploratory Data Analysis

The dataset is analyzed using:

* Dataset information
* Null value checking
* Descriptive statistics
* Pairplot
* Individual scatter plots
* Correlation matrix heatmap

The scatter plots analyze the relationship between Sales and:

* TV advertising
* Radio advertising
* Newspaper advertising

### 3. Data Preparation

The dataset is divided into:

* Input features: TV, Radio, Newspaper
* Target: Sales

The data is then split into training and testing sets.

### 4. Model Training

Two regression models are trained:

#### Linear Regression

Linear Regression is used as the baseline model.

It predicts sales by learning a linear relationship between advertising spending and sales.

#### Random Forest Regressor

Random Forest is used as an additional machine learning model.

It can learn more complex relationships in the data and is compared with Linear Regression.

### 5. Model Evaluation

The models are evaluated using:

* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)
* R² Score

A good model should generally have:

* Lower MAE
* Lower RMSE
* Higher R² Score

### 6. Model Comparison

The performance of Linear Regression and Random Forest is compared using the evaluation metrics.

The best model is selected based on its overall prediction performance.

### 7. Residual Analysis

A residual plot is created for the best-performing model.

Residual analysis helps determine whether prediction errors are randomly distributed or whether there is a systematic pattern that the model is not capturing.

### 8. Feature Importance

The project analyzes which advertising channel has the highest impact on sales.

This is done using:

* Linear Regression coefficients
* Random Forest feature importance

## Results

The project compares Linear Regression and Random Forest Regressor.

The model performance is evaluated using MAE, RMSE, and R² Score. Based on the results in the notebook, Random Forest performs better than the Linear Regression baseline.

The project also investigates which advertising channel has the strongest influence on sales.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### 2. Open the Project Folder

```bash
cd your-repository-name
```

### 3. Install Required Libraries

```bash
pip install pandas scikit-learn matplotlib seaborn jupyter
```

### 4. Make Sure the Dataset Is Available

Place the `Advertising.csv` file in the project folder or update the dataset path in the notebook.

Example:

```python
df = pd.read_csv("Advertising.csv")
```

### 5. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the Sales Prediction notebook and run all cells from top to bottom.

## Project Structure

```text
Sales-Prediction/
│
├── Advertising.csv
├── Sales_Prediction_Jupyter.ipynb
└── README.md
```

## What Can Be Improved in the Future?

This project can be improved by adding more features and experiments.

Possible improvements include:

### Additional Machine Learning Models

More regression models can be tested, such as:

* Decision Tree Regressor
* Gradient Boosting Regressor
* XGBoost
* Support Vector Regression
* Polynomial Regression

### Hyperparameter Tuning

Model performance can be improved by tuning parameters using:

* GridSearchCV
* RandomizedSearchCV

### Cross Validation

Cross-validation can provide a more reliable evaluation of model performance.

### Feature Engineering

New features can be created from the existing advertising data to investigate more complex relationships between advertising channels and sales.

### Model Deployment

The trained model can be deployed as a web application using:

* Flask
* FastAPI
* Streamlit

This would allow users to enter TV, Radio, and Newspaper advertising budgets and receive a predicted sales value.

### Save the Trained Model

The best-performing model can be saved using `joblib` or `pickle` and reused later without training the model again.

## Advantages of This Project

This project demonstrates how machine learning can be used to support marketing and business decisions.

Its main advantages are:

* Predicts sales based on advertising spending
* Helps analyze the relationship between advertising channels and sales
* Compares multiple machine learning models
* Uses standard regression evaluation metrics
* Identifies important advertising features
* Demonstrates the complete machine learning workflow from data analysis to model evaluation
* Can be extended into a real-world sales prediction application

## Learning Outcomes

Through this project, the following concepts are practiced:

* Data loading with pandas
* Exploratory Data Analysis
* Data visualization
* Correlation analysis
* Train/test splitting
* Linear Regression
* Random Forest Regression
* Model evaluation
* MAE, RMSE, and R² Score
* Residual analysis
* Feature importance
* Comparing machine learning models

## Conclusion

This project builds a complete regression-based sales prediction system using advertising spending data.

It starts with data analysis and visualization, trains multiple machine learning models, compares their performance, and identifies the relationship between advertising channels and product sales.

The project provides a simple foundation for understanding how machine learning regression can be applied to real-world business and marketing problems.
