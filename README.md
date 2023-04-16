# Portfolio-Project

This repo was created to showcase the results of my final project for the Professional Certificate in Machine Learning & Artificial Intelligence course.

## Project Introduction

 I chose to look at predicting movies revenue based on a number of input variables. To increase model accuracy, I used two machine learning techniques:
* Regression Decision Trees
* Multiple Regression

To further improve accuracy I used GridSearch to tune my hyperparameters.

## Dataset Used

The dataset used is The Movies Dataset, a popular dataset on Kaggle for those of us who enjoy applying data & AI methods to fun topics. The dataset  can be found in the 'data' folder. However, for a more in-depth description of the data please follow the link : https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset

I found some important weaknesses with the data, the biggest one being that the 'id' column is not consistent. This limited the number of variables I considered to include in my model. Secondly, the format of the data is a bit messy - I was planning to extract the country of where the movie comes from, and cast information, but I was unsuccesful in retrieving the information from those due to the format.

## Machine Learning Models Explored

As my outcome variable is numeric (revenue), the first model I chose was the Regression Decision Tree. This is a supervised machine learning model which has strong positive points:
* ease of interpretability - for both the data scientist and a non-technical audience as results can be easily visualised.
* handles non-linear relationships - relationships between features and the output variable can be captured because unlike regression models, decision trees don't assume a straight line between features and output.
* doesn't require feature scaling - this saves time and effort.
* can easily show the most important features in the model.

The second model that I tried was a Multiple Regression model. This again is a supervised machine learning model. Some of the positives of this model are:
* it can handle many input variables 
* it can identify important features - this is because it looks at the importance of each feature on the output variable.
* it is a widely known and understood method - it's a method that stakeholders trust.

## Regression Decision Tree Results

The results show that the decision tree regressor model has a training accuracy of 100%, which suggests that it might have overfit the training data. However, the testing accuracy is only 48%, indicating that the model is not performing well on unseen data. To improve the model's performance, hyperparameter tuning is done using grid search with cross-validation. The best model from the grid search has a training accuracy of 74% and a testing accuracy of 60%, which suggests that the model has improved and can now generalize better to new data. Overall, the model can be used to predict the revenue of a movie based on its budget, runtime, vote average, overview length, binary tagline, original language, and the emotion of the movie overview, but further analysis is needed to determine if the model is suitable for practical use. The error rates suggest that the model is not very accurate in predicting the revenue of the movies. The mean absolute error (MAE) of 10,368,118 suggests that, on average, the model's revenue predictions are off by that amount ($). The mean squared error (MSE) and root mean squared error (RMSE) are also quite large, which further confirms that the model is not very accurate.

## Multiple Regression Results

Based on the results, the multiple regression model has a training accuracy of 60% which is a positive result. However, the error rates of the MSE and RMSE are quite high, which indicates that important features might be missing from the analysis. To improve the accurate and the error rate, hyperparameter tunning was done using grid search. The results improved slightly, with an R-squared value of 0.627 on the test set, indicating that 62.7% of the variability in the revenue can be explained by the input features. The MSE of 1539051250395953.8 and the RMSE of 39230743.6 suggest that the model has a high prediction error, indicating that there may be additional important input features that were not included in the model or that the model may be overfitting the training data. 
