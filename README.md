# Tweets Sentiment Analysis using Naive Bayes Classifier

## Introduction

Sentiment analysis is a natural language processing task that predict the sentiment expressed in a piece of text. The goal is to understand the information in the text and classify it into predefined sentiment categories, such as positive, negative or neutral.

In sentiment analysis, a model is trained on a labeled dataset where each piece of text is associated with a sentiment label. The model learns to recognize patterns in the text that are indicative of specific sentiments. Once trained, the model can predict the sentiment of new unlabeled text by applying the learned patterns.

**Objective**

In the context of this project, the objective is to train a naive Bayes classifier model using a dataset of tweets ("Tweets.csv") with labeled sentiments. The accuracy of the model's predictions on the test dataset will be evaluated. Then, the trained model will be used to predict the sentiment of another dataset of tweets ("ChatGPT_tweets.csv") where the labels are unknown. 

**Dataset**

The 2 datasets used in this project are downloaded from Kaggle and contain tweets from the social media X.
There are two CSV files:
- **Tweets**: This file contains labeled tweets used for training and testing the model.
- **ChatGPT_tweets**: This file contains tweets without labels, which will be used to predict sentiment using the trained model.


## Setting up a virtual environment in VS Code

A virtual environment is an isolated Python environment that allows you to install packages and manage dependencies specific to your project without affecting other projects or the global Python environment. 

Steps:
- Make a new directory
- Open the integrated terminal in VS Code
- Create a virtual environment `python3 -m venv myenv`
- Activate the virtual environment `source myenv/bin/activate`
- Create a new directory inside the main directory and import **sentiment_analysis_tweets.ipynb**, **Tweets.csv** and **ChatGPT_tweets.csv**


## Sentiment analysis

### 1. "Tweets" data preprocessing

- Column Selection: Select the relevant columns from the "Tweets" dataset.
- Text Cleaning: Clean the text data by removing special characters, URLs, and stopwords to ensure that only meaningful words are kept.
- Tokenization and Stemming: Tokenize the cleaned text, breaking it down into individual tokens and apply stemming to reduce words to their root form.
- Data joining: Join the tokenized and stemmed words back together. The text is now a list of strings, ready for further analysis.

### 2. Model training

Split the labeled dataset into training and testing sets.
Convert it into numerical features using techniques like Bag-of-Words.
Train a Naive Bayes classifier model using the training data.

### 3. Model evaluation
Evaluate the trained model's accuracy and performance on the testing dataset.

### 4. "ChatGPT_tweets" preprocessing

Same steps as "Tweets" data preprocessing

### 5. "ChatGPT_tweets" sentiment prediction

Use the trained model to predict the sentiment of tweets in the ChatGPT_tweets.csv dataset.

### 6. Bonus analyses

**Most common hashtags:** Identify and extract the most common hashtags in "ChatGPT_tweets". This analysis provides insights into trending topics or themes within the tweets.

**Most similar words:** Use word embedding techniques to represent words as vectors and explore semantic relationships between words by finding the most similar words in "ChatGPT_tweets".
