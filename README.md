# HousingRegression Analysis
January 2018

Housing Regression analysis on the Ames Housing set from Kaggle. Used python, pandas, Sci Kit learn in a Jupyter Notebook.

1) Data:
  This data was obtain from Kaggle's "House Prices: Advanced Regression Techniques" competition. Kaggle provided a data set with 79 features of houses in Ames, Iowa in order to predict the prices of homes. Examples of features include the lot of the area, its slope, utilities available, year build, if there is a fire place, number of bedrooms, etc. The data was already split into training and test data sets.
  
2) Methods:
  After reading in the data set, I deleted features that had mostly missing data. Next, I approximated missing data for features that were mostly filled. For example, for houses without the year the garage was built, a numerical feature, I used the mean year of all houses. For categorical features such as utility type, I used the mode of utiltiy types. 
  
  For categorical data, I needed to create dummy features that were binary. For each possible value within a categorical feature, I created another binary feature corresponding to that value.
  
  Next, I saw that the data is skewed and took the log to normalize the sale price and any other skewed features.
  
  I then tried out a number of models including ridge regression, lasso regression, elastic nets, random forests, gradient boosting regression, and extreme gradient boosting. Using GridSearchCV, I was able to find the optimal parameters for each model.
  
  Rather than pick the best model, I combined all of the best models together into an ensemble model to avoid any bias in model selection. I applied this ensemble model to the test set and made predictions on the test set.
  
  3) Results:
   My prediction submission to Kaggle received a log loss of 0.11820, placing me 572 out of 3428, in the top 17% of submissions. To improve upon this model, I could have tried other methods of preprocessing the data such as using principle componenet analysis (PCA). 
 
