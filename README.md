# House_Price_Prediction_Kaggle
The aim of the project is to build a machine learning model to predict the sale price of homes based on different variables describing aspects of residential houses

## PART A. EXPLORATORY DATA ANALYSIS
- Created a list of the variables that contain missing values and determining percentage of missing values
- Analysed relationship between values being missing and the targe label (Sale Price)
- Evaluated the median Sale price of the house in those observations where the information is missing and comparing it with observations where value is available, for each variable
- Explored whether there is a relationship between the year variables and SalePrice
- Determine descrete variables taking threshold as 2% of total data size
- Analysed distribution of contiuous variables
- Determined rare variables taking threshold as 1% of total observation per category 

![alt text](https://github.com/ravigupta5/House_Price_Prediction_Kaggle/blob/master/Missing_values_importance.PNG?raw=true)


## PART B. FEATURE ENGINEERING
1. MISSING VALUES
- Replaced missing values in categorical features with new label: "Missing"
- Engineered missing values in numerical variables by adding a binary missing value indicator variable and then replacing the missing values in the original variable with the mode
2. TEMPORAL FEATURES
- Captured the time elapsed between these variables and the year in which the house was sold
3. NUMERICAL VARIABLE TRANSFORMATION
- Introduced log transformation for numerical variables in order to get a more Gaussian-like distribution
4. CATEGORICAL FEATURES
- Grouped those categories within variables that are present in less than 1% of the observations by the string "Rare"
- Applied mean-encoding to categorical features to obtain monotonic relationship between features and target
- Stored the ordinal_label in nested dictionary which can be mapped to test dataset
5. FEATURE SCALING
- Applied MinMax feature scaling

![alt text](https://github.com/ravigupta5/House_Price_Prediction_Kaggle/blob/master/Mean_Encoding.PNG?raw=true)
![alt text](https://github.com/ravigupta5/House_Price_Prediction_Kaggle/blob/master/Variable_transformation2.png?raw=true)
## PART C. FEATURE SELECTION
- Selected variables using the Lasso regression

## PART D. MODEL BUILDING
- Implemented Regularised linear regression model: Lasso

### Model performance:
- This submission to Kaggle yielded RMSE = 0.17522
