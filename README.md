# House_Price_Prediction

# Problem Statement:

Estimating house prices is important for buyers, sellers, and real estate companies. The aim of this project is to build a regression model that predicts house prices based on features such as location, size, etc using historical housing data.

# Dataset:

The dataset is taken from Kaggle, which  contains historical housing data with information such as location, size, number of bedrooms and bathrooms, and price. It consists of numerical and categorical features used to predict house prices.

- Rows: 20640
  
- Features: Location, Area, Bedrooms, Bathrooms, etc.

- Target Variable: median_house_value
  
# Tools:

Pandas

Numpy 

Scikit Learn

Natural Language Tool Kit

String

# Approach and Methodology:

## a) Missing/ Null values:

Removed all the null values. 

## b) Data Exploration and Preprocessing: 

- The correlation matrix (heatmap) is visualized.  

- Some numerical features were log-transformed because they were highly skewed, helping to reduce the effect of extreme values and improve model performance.
  
## c) Feature Engineering: 

Additional features were created by combining existing columns, and a correlation heatmap was again used to analyze relationships between variables.

## d) Train Test split:
- The data is split into training and testing data using the Scikitlearn function, train_test_split().

- Training the scaled data using the linear regressor model, followed by a  random forest classifier.

# Models used:

## Linear Regressor: 
The model develops a linear relationship between the variables and fits a straight line to the observed data points to best predict the dependent variable based on the independent variable.

## Random Forest Classifier:
Ensemble model, it combines several decision tree models to get stable predictions. Instead of relying on a single decision tree, a ‘forest’ of multiple trees are built, each trained on a random subset of the data and the features reducing overfitting.

## Grid search:
A technique used to find the best model settings by trying different combinations of parameters using cross validation and selecting the one that gives the highest validation performance. (hyperparameter tuning).

# Evaluation Metrics:

## R^2 score: 

- For regression models, this score is calculated internally by first predicting the target values using the input features, then comparing these predictions to the true target values using the R² formula.
  
- The R² score is defined as 1 - ((the sum of squared differences between actual and predicted values) / (the sum of squared differences between actual values and their mean)). 

- A score of 1 indicates a perfect fit, while a score of 0 means the model performs as bad as the mean

- reg.score for linear regression model is 0.697, random forest model is 0.83 and after hyperparameter tuning it is 0.97.
  
# Insights:

- The model was able to predict house prices with reasonable accuracy using features like area, number of rooms, and location.

- Larger house size and better location were found to have a strong impact on price.
  
- Proper data cleaning and feature scaling improved model performance.
  
# How to run the project:

- Download or clone the repository.
  
- Open the project folder.
  
- Open the Jupyter Notebook file (.ipynb).
  
- Run all the cells from top to bottom.

# Project Structure: 

├── housing.csv       # Datasets used in the project

├── house.prediction.ipynb      # Jupyter Notebook with full code

├── README.md          # Project explanation
