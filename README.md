# Ames Housing Market

## The goal of this project was to:

### 1.) Examine the Ames real estate data.
### 2.) Clean the data if required.
### 3.) OneHotEncode categorical features and fill missing values.
### 4.) Conduct Exploratory Data Analysis on the data.
### 5.) Create a machine learning model to predict the sale price of home in the Ames housing market.
### 6.) Submit the predictions for the test set to the kaggle competition.
### 7.) Present any findings to stakeholders.

## Breakdown of the code found in P2.ipynb:

### 1.) Conducted exploratory data analysis and verified there were missing values.
### 2.) I created the predictor matrix and target vector using only the training dataset and then train/test split.
### 3.) I created first model, which used a column transformer to OneHotEncode the features with object dtypes. 
### 4.) I then created a pipeline, which used the column transformer mentioned above, KNNImputer, StandardScaler, RFE, and Ridge.
### 5.) This model was then evaluated using a null model, r2 and RMSE.
### 6.) I created a second model, which is very similar to the first model, except: it uses SimpleImputer rather than KNNImputer, and Lasso is the model's estimator instead of Ridge.
### 7.) I then evaluated model 2 the same way as in bullet #5 above.
### 8.) Using this same blueprint, I created the third and final model. This model used KNNImputer to fill missing values and KNeighborsRegressor as an estimator. This model was evalated the same as described in bullets #5 and #7 above.
### 9.) All three models were compared and model 2 was determined to be best because it had the lowest RMSE.
### 10.) The next step was to intepret the coefficients of the model.

## Based on my analysis of the data, I present the following findings:

### 1.) For every 1 standard deviation increase in total square feet on the 2nd floor, we expect to see an increase of $14314 in the sale price
### 2.) For every 1 standard deviation increase in in year built, we expect to see an increase of $9681 in the sale price.
### 3.) For every 1 standard deviation increase in the amount of roofing material used being clay tile, we expect to see a decrease of $17035 in the sale price.
### 4.) The highest correlated variable with sale price was the overall quality of the home. 

## Recommendations to improve home values in Ames housing market:

### 1.) Build additions to the property that increase the overall square footage of the home.
### 2.) If the home has a basement, finish it and maximize the amount of square feet within it.
### 3.) Improve the quality and condition of the garage's exterior.


## Code Notebook:
### ../Project_2/P2.ipynb

## Data Dictionary is available at:
### https://www.kaggle.com/c/dsir-907-project-2/data

## Kaggle Submission is availabe at:
### https://www.kaggle.com/c/dsir-907-project-2/submissions?group=selected&page=1&pageSize=100;

## The training data used for modeling:
### https://www.kaggle.com/c/dsir-907-project-2/data?select=train.csv

## The test data the model used to make predictions. (Excludes the 'SalePrice' column):
### https://www.kaggle.com/c/dsir-907-project-2/data?select=test.csv