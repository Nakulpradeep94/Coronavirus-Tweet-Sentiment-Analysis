# Coronavirus-Tweet-Sentiment-Analysis

## Problem Description

This challenge asks you to build a classification model to predict the sentiment of COVID-19 tweets.The tweets have been pulled from Twitter and manual tagging has been done then.
The names and usernames have been given codes to avoid any privacy concerns.
You are given the following information: Location, Tweet At, Original Tweet and Label

## Data dictionary
* Username : gives the name of the user (coded)
* Screenname: gives the screen name of the user (coded)
* Location: gives information regarding the location from which tweet is sent
* Tweet At: gives the date of the Tweet
* Original Tweet : Tweet Content

## Exploratory Data Analysis (Basic)
* The data has 41157 rows and 6 columns or features.
* The data set does not contain duplicate values.
* The dependent variable is ‘Sentiment column’ and it has 5 distinct features namely Neutral, Positive, Extremely Negative, Negative and Extremely Positive.
* The independent variable is ‘OriginalTweet’ column and it has no null or duplicate values.
* There are null values present in the location column as there are only 32567 non null values for location with rows of 41157 values but there is no need for
null value treatment as it is not part of the independent variable.

## Exploratory Data Analysis (Insights)
* The tweets in the dataset are from 16Th March 2020 to 14th April 2020. i.e. for a period of 30 days.
* People tweeted most during 20-03-2020 and least during 28-03-2020.
* All of top 5 tweets come from parts of UK and USA.

# Process
The Sentiment analysis of Tweet are to be done, before doing so several steps are to be done i.e. cleaning of the Original tweet or text are to be done before transformation of the data to vectorized form.
For the given data the following transformations are done like
* Removing URLs,
* Removing values with username attached,
* Tokenize the text (split the text into words) 
* Removing punctuations and special character
* Removing words with length less than or equal to 2
* Removing useless stop words like ‘the’, ‘a’,’ this’ etc.
* Lemmatize the text and stemming.
Dataset is split into two: train dataset and test dataset for the classification analysis. Then the text was converted from words into numbers by the process called Vectorization. The two types of vectorizations used are Count Vectorizer and TF-IDF Vectorizer. The dataset is then experimented with various models like Logistic Regression, Naive Bayes Classifier (both Bernoulli’s and Multinomial), XG Boost, Random Forest and SVM. The evaluation metrics used here for checking the predicted model accuracy are Accuracy score, recall, precision and F1 score. 

# Conclusion

* Logistic Regression and SVM gives the best accuracy, recall, precision and F1 score compared to all other models in multiclass (5 sentiment) dataset. Both of them gives a 0.62 F1 score. 
* Logistic Regression gives a best accuracy, recall, precision and F1 score compared to all other models in multiclass (3 sentiment) dataset. It gives a 0.80 F1 score.
