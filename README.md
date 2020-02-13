# House-Prices-Advanced-Regression-Techniques
Predict sales prices and practice using feature engineering, RFs, and gradient boosting
# Competition Description from Kaggle
With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.
# My Approach
Following approaches and techniques i applied:
EDA with Pandas and Seaborn.<br/>
Find features with strong correlation to target.<br/>
Data Wrangling, convert categorical to numerical.
Apply the basic Regression models of sklearn
use gridsearchCV to find the best parameters for each model
compare the performance of the Regressors and choose best one

# My notebook is organized as follows:

Part 0: Imports, Settings and switches, Global functions
import libraries
settings for number of cross validations
define functions that are used often

# Part 1: Exploratory Data Analysis
## 1.1 Get an overview of the features (numerical and categorical) and first look on the target variable SalePrice
shape, info, head and describe
Distribution of the target variable SalePrice
Numerical and Categorical features
List of features with missing values and Filling missing values
log transform
## 1.2 Relation of all features to target SalePrice
Seaborn regression plots for numerical features
List of numerical features and their correlation coefficient to target
Seaborn boxplots for categorical features
List of categorical features and their unique values
## 1.3 Determine the columns that show strong correlation to target
Correlation matrix 1 : all numerical features
Determine features with largest correlation to SalePrice_Log

# Part 2: Data wrangling
Dropping all columns with weak correlation to SalePrice
Convert categorical columns to numerical
Checking correlation to SalePrice for the new numerical columns
use only features with strong correlation to target
Correlation Matrix 2 (including converted categorical columns)
create datasets for ML algorithms
One Hot Encoder
StandardScaler

# Part 3: Scikit-learn basic regression models and comparison of results
implement GridsearchCV with RMSE metric for Hyperparameter tuning
for these models from sklearn:
Linear Regression
Ridge
Lasso
Elastic Net
Stochastic Gradient Descent
DecisionTreeRegressor
Random Forest Regressor
KNN Regressor
baed on RMSE metric, compare performance of the regressors with their optimized parameters,
then explore correlation of the predictions and make submission with mean of best models
Comparison plot: RMSE of all models
Correlation of model results
Mean of best models
