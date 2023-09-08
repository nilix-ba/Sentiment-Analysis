# Sentiment Analysis

## Introduction
This project focuses on sentiment analysis of textual data, aiming to classify the sentiment of tweets as either positive or negative. It leverages various natural language processing (NLP) techniques and machine learning algorithms to achieve this classification.

## Setup
Before running the code, make sure you have the required libraries installed. 

## Data Preparation
The project begins with data loading and preprocessing. Two datasets, 'SandersPosNeg.csv' and 'OMD.csv,' are used. Data from 'SandersPosNeg.csv' initially requires reformatting.

- `pd.read_csv("SandersPosNeg.csv")`: Load the Sanders dataset.
- `pd.read_csv("OMD.csv")`: Load the OMD dataset and apply data formatting.

## Text Preprocessing
Text preprocessing is a crucial step in preparing the data for sentiment analysis. The following preprocessing steps are applied to both datasets:

1. **Lowercasing**: Convert all text to lowercase.
2. **Removing Numbers**: Remove numerical digits from the text.
3. **Removing Punctuation**: Eliminate punctuation marks from the text.
4. **Tokenization**: Tokenize the text using the NLTK library.
5. **Stopword Removal**: Remove common stopwords from the text using NLTK's stopwords list.
6. **Stemming**: Reduce words to their root form using the Porter Stemmer algorithm.

## Data Transformation
After preprocessing, the text data is transformed into a suitable format for machine learning models.

- `TfidfVectorizer()`: Convert the preprocessed text data into numerical features using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization.

## Model Training and Evaluation
Two datasets, 'Sanders' and 'OMD,' are used to train and evaluate the sentiment analysis model.

- Multinomial Naive Bayes (MultinomialNB) is chosen as the classification algorithm.
- 10-fold cross-validation is employed to assess model performance.

## Results
The project outputs the accuracy of the sentiment analysis model for both datasets.

- 'accuracy sandres': Accuracy of sentiment analysis on the 'Sanders' dataset.
- 'accuracy omd': Accuracy of sentiment analysis on the 'OMD' dataset.

## Visualization
The project includes visualizations to illustrate the distribution of positive and negative tweets in the test samples.

- `sns.countplot()`: Visualize the count of positive and negative tweets for both datasets.

## Conclusion
This project showcases the entire process of sentiment analysis, from data preprocessing to model training and evaluation. It provides insights into classifying tweets as positive or negative sentiment using NLP techniques and machine learning.
