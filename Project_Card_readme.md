## Model Description:
The machine learning models explored in this project are the Regression Decision Tree and Multiple Regression, both of which aim to predict movie revenue based on various input variables. 
The input variables used include:
* budget
* runtime
* average vote of movie
* emotion of movie overview
* language of movie
* movie overview length 
* tagline (whether the movie had a tagline or not)

Genre was initially included as well but the impact on the model was insignificant so it was taken out.
 
The dataset used is The Movies Dataset, which has some limitations:
* movie ID and reviews ID - these variables are not consistent and as such, they are not very useful. There are a few other datasets that can be used to increase the number of features in the movies dataset. I planned to include IMDB reviews and cast information (actors/directors rank) however, the IDs present in the movie dataset are not consistent with the IDs in the other datasets which was quite a shame as it limited the amount of features included in the model.
* the format of some of the variables again limited the amount of information included in the model - one of the variables in the movies dataset was 'production_countries'. I wanted to extract the country and see if this had an impact on the revenue, however the information was not consistent and extraction was very difficult, so I gave up on this idea.
* this is not necesarily a negative of the dataset but I was hoping to find some pre-trained classification models to create more variables for my model such as: type of movie (whether it was 18+ or for children), actors ranking (A/B/C/D list), production company ranking (A/B/C/D). However there aren't such pre-trained models (as of yet!).
* information available on actors/production - this links with the above statement. As I couldn't find pre-trained models I thought I could still find some lists that rank actors/production/directors/movies. However this information is not public. 

## Input:
As mentioned above, the input variables I included were:
* budget
* runtime
* average vote of movie
* emotion of movie overview
* language of movie
* movie overview length 
* tagline (whether the movie had a tagline or not)

## Output:
The output of the models is a prediction of movie revenue.

## Model Architecture:
The Regression Decision Tree and Multiple Regression models are both supervised machine learning models that aim to predict a numeric outcome variable. The Regression Decision Tree model has strong interpretability and handles non-linear relationships well, while the Multiple Regression model can handle many input variables and identify important features.

## Performance:
The Regression Decision Tree model had perfect training accuracy but only 47% accuracy for unseen data. After hyperparameter tuning, the model's accuracy improved by 13%. However, the error rates still suggest that the model is not very accurate in predicting movie revenue. The Multiple Regression model had a training accuracy of 60%, which improved to 63% after hyperparameter tuning. However, the error rates remained high, suggesting that important factors may be missing from the analysis or that the model is overfitting the training data.

## Limitations:
One limitation of the models is that the features used were quite limited. As I mentioned above, I wanted to create more features, and use the extra datasets that come with 'The Movies', however due to ID inconsistencies, and limited information online for ranking, this was the best I could do. I found pros and cons for a few datasets on Kaggle, and found this one to be acceptable for the amount of time I had for the portfolio. As a result of the previous points, the models may not be capturing all of the important features that contribute to movie revenue, which led to high error rates, even after using Grid Search for hyperparameter tunning.


## Trade-offs:
One trade-off of the models is that they may not be accurate enough to make reliable predictions about movie revenue. This could be a limitation in situations where accurate revenue predictions are necessary, such as in the film industry. Additionally, the models may require additional feature engineering or more sophisticated modeling techniques to capture all of the important factors that contribute to movie revenue.
