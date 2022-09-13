# 2020_US_election_tweets_analysis
Sentiment analysis of 2020 Election tweets

### Context
We used tweets from Kaggle and Twitter API to get a dataset on tweets 1 month prior to the 2020 US elections.

### Motivation
We wanted explore how tweets reflect the public sentiment in the event of a significant event such as the 2020 US elections. 
How can we use Machine Learning to find better predictions of the upcoming future elections that already have a lot of data on people's sentiments in the public domain?

### Data Preprocessing
1. We have joebiden.csv and donaldtrump.csv with tweets related to each presidential candidate.
Preprocessing/ cleaning involved including removal of hashtags, retweets, tweets outside the USA.
2. We filtered tweets for English language & also within a period of 1 month before election day.

### Model Used for NLP(getting the sentiment of the tweet)
1. TextBlob is a Python library for Natural Language Processing (NLP). TextBlob actively employed Natural Language ToolKit (NLTK) to accomplish its tasks. NLTK is a library that provides easy access to many lexical resources and allows users to deal with categorization, classification, and a variety of other tasks. TextBlob is a basic package that allows for lexicon based sentiment analysis.
2. Google cloud NLP API, Using Google's superior text analysis algorithm. Google Cloud Natural Language API is a cloud-based collection of strong machine learning models. It can do Sentiment Analysis, Entity Analysis, Syntax Analysis, Entity Sentiment Analysis, and Text Classification without labeled or training data. These models have been pre-trained on somewhat large datasets.

### Using the NLP Result
We use the NLP results from both texblob and GCP NLP API and provide it as the final label(sentiment) of the tweet and then create classification algorithms to predict the sentiment using actual tweets.

### Machine Learning Models Used
1. Logistic Regression, with the best success rate of 85.4%, is the Model used in the final prediction of the outcome.
2. Naive Bayes, using the Bayesian algorithm to predict the classification of the votes
3. Random Forest it's a combination of hundreds of decision trees that gives a representation of the most important feature
4. Gradient Boost Algorithm, Ensemble Learning technique that combines several weak learners(predictors with poor accuracy) into a strong learner(a model with factual accuracy). This works by each Model paying attention to its predecessor's mistakes.
5. Factorization Machines (FM) is a generic yet robust model framework especially well-suited to collaborative filtering recommendation problems
6. Support Vector Machines SVM is based on the idea of finding a hyperplane that best separates the features into different domains.
7. Decision Tree, these classifiers provide a direct value of the most critical parameter and then divide the parameters tree-wise and use Gini Index to get the most critical parameter.


### Visualization
1. After getting the best result via Logistic Regression as our top priority model, we display the results of each candidate's votes and prediction counts.
2. We are now using the prediction of our Model to get the winner in a single state by using (positive references-negative references).


### Final Results
1. We have predictions of state-wise winners, visualized using pyplotexpress
2. Joe Biden seems like a clear winner, however our predictions differ from the actual results and we've included our hypotheses  for the inaccuracy in predictions in the report.
