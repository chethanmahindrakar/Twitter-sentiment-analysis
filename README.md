#Twitter Sentiment Analysis

  This project is only an exploratory analysis on the performance of different classifiers and machine learning models for twitter sentiment analysis.
  The sentiment of a tweet is restricted to either positive or negetive.

 ##The dataset

  The dataset used in this project is the training corpus of the sentiment 140 dataset produced by standford. The dataset can be found here - http://help.sentiment140.com/for-students . 
  The original dataset consists of 1.6 million records which is computatinally heavy; hence custom datasets for training and testing were produced using the original dataset. 100 thousand records were taken for the training dataset and 20 thousand were taken for testing with no repetitions among each other.

 ##The Approach
  A word-based approach is taken where the probaility of a word being positive or negative is calculated. For all the words occuring in a particular tweet,(obviously bi-grams are produced where recquired) the majority of words classifying as either of the sentiments determine the overall sentiment of the tweet.

 ##In this repo
  - Dataset generation.ipynb : Produces a smaller dataset from the stanford dataset. Parameters can be easily tuned to change the size of each training and testing dataset produced. The produced datasets have positive and negative tweets in the same ratio.

  - Pre-Processing and Visualization.ipynb : Selects only the required columns of the datasets and cleans the data by removing stopwords, hastags, user-ids, punctuations and URL's from the tweets. Also generates a few Word-cloud visualizations for both positive and negative tweets on both the training and testing corpus. Stores the cleaned data in the form of a json file.

  - All models.ipynb : Performs normalizations, one hot encoding and vectorization on the data and trains the different models used. Also calculates the accuracy of each of the models.

 ##The ML models
  - Naive Bayes classifer : Accuracy of about 76%
  - Random Forest Classifier : Accuracy of about 73%
  - Logicstic Regression model : Highest Accuracy of 76% for c = 0.75 (c represents inverse of    regularization)