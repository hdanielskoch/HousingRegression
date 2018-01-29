# HousingRegression Analysis
January 2018

Housing Regression analysis on the Ames Housing set from Kaggle. Used python, pandas, Sci Kit learn in a Jupyter Notebook.

1) Data:
  This data was obtain from Kaggle's "House Prices: Advanced Regression Techniques" competition. Kaggle provided a data set with 79 features of houses in Ames, Iowa in order to predict the prices of homes. Examples of features include the lot of the area, its slope, utilities available, year build, if there is a fire place, number of bedrooms, etc. The data was already split into training and test data sets.
  
2) Methods:
  After reading in the data set, I deleted features that had mostly missing data. Next, I processed missing information according to feature. For example, for houses without the year the garage was built, a numerical feature, I used the mean year of all houses. For categorical features such as utility type, I used the mode of utiltiy types. 
  
  For categorical data, I need to create dummy features that are binary. Essentially, for each possible option within a categorical feature, I need to create another binary feature corresponding to that option.
  
  Next, I check that the data is skewed and take the log to normalize the sale price and any skewed features.
  
  I then try out a number of models including ridge regression, lasso regression, elastic nets, random forests, gradient boosting regression, and extreme gradient boosting. Using GridSearchCV, I am able to find the optimal paramters for each model.
  
  Rather than pick the best model, I combine all of the best models together into an ensemble model to avoid any bias in model selection. I apply this ensemble model to the test set and make predictions on the test set.
  
  3) Results:
   My prediction submission to Kaggle received a log loss of , placing me out of blank, in the top % of all submissions.
 
