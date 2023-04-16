# Portfolio-Project

This repo was created to showcase the results of my final project for the Professional Certificate in Machine Learning & Artificial Intelligence course.

## Project Introduction

 Two machine learning methods were chosen to help predict movies revenue based on a number of input variables:
* Regression Decision Trees
* Multiple Regression

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

The second model that I tried was a Multiple Regression model. This again is a supervised machine learning model. Some of the positives of this model are:
* it can handle many input variables 
* it can identify important features - this is because it looks at the importance of each feature on the output variable.
* it is a widely known and understood method - it's a method that stakeholders trust.

## Regression Decision Tree Results

A reggression decision tree model was trained to predict the revenue of a movie based on various factors such as budget, runtime, emotion of movie overview, and language of movie. The results showed that the model had a perfect training accuracy, but it was not performing well on unseen data, with a 47% accuracy for the unseen data. To improve the model, hyperparameter tuning was done, which improved the model's accuracy by 13%. However, the error rates suggested that the model was not very accurate in predicting the revenue of the movies.


## Multiple Regression Results

The second model was trained to predict movie revenue using various factors. The model had a training accuracy of 60%, which is a good result. However, the error rates were high, suggesting that important factors were missing from the analysis. Hyperparameter tuning was done to improve the accuracy, which improved the R-squared value to 63%. However, the error rates remained high, suggesting that additional factors may be important or that the model may be overfitting the training data.
