# Portfolio-Project

This repo was created to showcase the results of my final project for the Professional Certificate in Machine Learning & Artificial Intelligence course.

## Project Introduction

I wanted to explore a fun topic for my project, so after exploring a few datasets on Kaggle, I settled on 'The Movies' dataset. My aim was to predict movies revenues. A few of my research questions were:

Which genres tend to have the highest revenue? Are there any genres that consistently perform poorly?

1. What is the relationship between budget and revenue? 

2. Does the language of the movie have an impact on revenue?

3. How do ratings (e.g., IMDb or Rotten Tomatoes scores) impact revenue? 

4. Can a model using genre, ratings, budget, languages, and countries accurately predict movie revenue? Which input variables are most important in predicting revenue?

 Two machine learning methods were chosen to help predict movies revenue based on a number of input variables:
* Regression Decision Trees
* Random Forest

To further improve accuracy and reduce errors, I used GridSearch to tune my hyperparameters.

## Dataset Used

The dataset used is The Movies Dataset, a popular dataset on Kaggle for those of us who enjoy applying data & AI methods to fun topics. The dataset  can be found in the 'data' folder. However, for a more in-depth description of the data please follow the link : https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset

I found some important weaknesses with the data, the biggest one being that the 'id' column is not consistent. This limited the number of variables I considered to include in my model. Secondly, the format of the data is a bit messy - I was planning to extract the country of where the movie comes from, and cast information, but I was unsuccesful in retrieving the information from those due to the format.

## Machine Learning Models Explored

As my outcome variable is numeric (revenue), the first model I chose was the Regression Decision Tree. This is a supervised machine learning model which has strong positive points:
* ease of interpretability - for both the data scientist and a non-technical audience as results can be easily visualised.
* handles non-linear relationships - relationships between features and the output variable can be captured because unlike regression models, decision trees don't assume a straight line between features and output.
* doesn't require feature scaling - this saves time and effort.
* can easily show the most important features in the model.

The second model that I tried was a Random Forest model. This again is a supervised machine learning model. Some of the positives of this model are:
* high accuracy - compared to other linear regression models, random forest is known be produce high-accuracy models.
* roboustness - it is less sensitive to outliers and noise in the data compared to other models.
* can easily show the most important features in the model.

## Regression Decision Tree Results

The results show that the decision tree regressor model has a training accuracy of 100%, which suggests that it might have overfit the training data. However, the testing accuracy was 67%, indicating that the model is performing fine on unseen data. To improve the model's performance, hyperparameter tuning is done using grid search with cross-validation. The best model from the grid search has a training accuracy of 74% and a testing accuracy of 65%, which suggests that the hyperameter tunning did not have a significant impact on the model. Overall, the model can be used to predict the revenue of a movie based on its budget, runtime, vote average, overview length, binary tagline, original language, and the emotion of the movie overview, but further analysis is needed to determine if the model is suitable for practical use. The error rates suggest that the model is not very accurate in predicting the revenue of the movies. The mean absolute error (MAE) of 7862301.0 suggests that, on average, the model's revenue predictions are off by that amount ($). The mean squared error (MSE) and root mean squared error (RMSE) are also quite large, which further confirms that the model is not very accurate.

## Random Forest Model Results and Recommendation

Based on the results, after using hyperparameter tunning, the random forest model has an accuracy of 69% . This accuracy is higher than the accuracy from the Regression Decision Tree model, which was 64%. The Random Forest Model also shows slightly lower errors than the Regression Decision Tree Model. With a MAE of 7789857.1, MSE of 1045625509849571 and RMSE of 32336133, compared to the Regression Decision Tree which had a MAE of 7862301, a MSE of 1158305350430807.0 and RMSE of 34033885.3. However, the error rates are still high, which indicates that important features might be missing from the analysis. Based on the two models, I recommend the random forest model as it gives a higher accuracy and a lower error rate. Emsemble techniques are better than decision trees as they can capture the complexity of the data or where the data is noisy or uncertain.
