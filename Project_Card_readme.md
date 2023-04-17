## Model Description:
The machine learning models explored in this project are the Regression Decision Tree and Multiple Regression, both of which aim to predict movie revenue based on various input variables. The input variables used include budget, runtime, emotion of movie overview, and language of movie, among others. The dataset used is The Movies Dataset, which has some limitations, such as inconsistent 'id' columns and messy data formatting.

## Input:
The input variables used in the models include budget, runtime, emotion of movie overview, language of movie, and other factors such as director, cast, and genre.

## Output:
The output of the models is a prediction of movie revenue.

## Model Architecture:
The Regression Decision Tree and Multiple Regression models are both supervised machine learning models that aim to predict a numeric outcome variable. The Regression Decision Tree model has strong interpretability and handles non-linear relationships well, while the Multiple Regression model can handle many input variables and identify important features.

## Performance:
The Regression Decision Tree model had perfect training accuracy but only 47% accuracy for unseen data. After hyperparameter tuning, the model's accuracy improved by 13%. However, the error rates still suggest that the model is not very accurate in predicting movie revenue. The Multiple Regression model had a training accuracy of 60%, which improved to 63% after hyperparameter tuning. However, the error rates remained high, suggesting that important factors may be missing from the analysis or that the model is overfitting the training data.

## Limitations:
One limitation of the models is that the dataset used has some limitations, such as inconsistent 'id' columns and messy data formatting. Additionally, the models may not be capturing all of the important features that contribute to movie revenue, which could lead to high error rates.

## Trade-offs:
One trade-off of the models is that they may not be accurate enough to make reliable predictions about movie revenue. This could be a limitation in situations where accurate revenue predictions are necessary, such as in the film industry. Additionally, the models may require additional feature engineering or more sophisticated modeling techniques to capture all of the important factors that contribute to movie revenue.
