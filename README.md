# Sentiment Analysis of Pakistani City Tweets

This project performs sentiment analysis on tweets related to different cities and tourist locations in Pakistan. The notebook combines scraped tweet datasets, cleans the text, assigns sentiment labels using TextBlob, and compares different machine learning models using TF-IDF features.

## Project Overview

The main goal of this project is to analyze public sentiment from tweets and classify each tweet into one of the following categories:

- Negative
- Neutral
- Positive

The project also performs city-wise sentiment analysis to compare public opinion about different Pakistani cities and tourist destinations.

## Dataset

The dataset is created by combining multiple scraped CSV files related to Pakistani cities and tourist locations.

The cities/locations used in this project include:

- Karachi
- Lahore
- Hunza
- Islamabad
- Kaghan
- Neelum Valley
- Peshawar
- Skardu
- Swat

Each dataset contains tweet text related to a specific city/location. These files are merged into one combined dataset for preprocessing, sentiment labeling, model training, and evaluation.

## Features of the Project

- Combines multiple city-based tweet CSV files
- Cleans and preprocesses tweet text
- Removes HTML tags, special characters, numbers, stopwords, and extra spaces
- Applies lemmatization
- Generates sentiment labels using TextBlob polarity
- Converts text into TF-IDF features
- Trains multiple machine learning models
- Compares model performance using accuracy and classification reports
- Generates confusion matrices
- Creates word clouds for text visualization
- Performs city-wise sentiment percentage analysis
- Ranks cities based on positive sentiment percentage

## Machine Learning Models Used

The following machine learning models are used in this project:

- Logistic Regression
- Multinomial Naive Bayes
- Random Forest Classifier
- Multi-Layer Perceptron Classifier
- Stacking Ensemble Classifier

## Methodology

The project follows these main steps:

1. Import required Python libraries
2. Load scraped tweet CSV files
3. Merge all city datasets into one dataframe
4. Clean and preprocess tweet text
5. Apply TextBlob to calculate sentiment polarity
6. Assign sentiment labels as Positive, Negative, or Neutral
7. Encode sentiment labels into numerical classes
8. Split the dataset into training and testing sets
9. Convert tweet text into TF-IDF feature vectors
10. Train machine learning models
11. Evaluate model performance
12. Analyze city-wise sentiment distribution

## Sentiment Labeling

Sentiment labels are assigned using TextBlob polarity scores.

| Polarity Score | Sentiment Label |
|---|---|
| Greater than 0 | Positive |
| Less than 0 | Negative |
| Equal to 0 | Neutral |

## Model Results

The models were evaluated using both unigram and bigram TF-IDF features.

| Model | Feature Type | Accuracy |
|---|---|---|
| Logistic Regression | Unigram TF-IDF | 88.71% |
| Naive Bayes | Unigram TF-IDF | 82.49% |
| Random Forest | Unigram TF-IDF | 91.52% |
| Multi-Layer Perceptron | Unigram TF-IDF | 89.94% |
| Stacking Ensemble | Unigram TF-IDF | 93.90% |
| Logistic Regression | Bigram TF-IDF | 87.89% |
| Naive Bayes | Bigram TF-IDF | 81.14% |
| Random Forest | Bigram TF-IDF | 91.35% |
| Multi-Layer Perceptron | Bigram TF-IDF | 88.60% |
| Stacking Ensemble | Bigram TF-IDF | 92.63% |

The best-performing model was the Stacking Ensemble Classifier using unigram TF-IDF features, achieving an accuracy of approximately 93.90%.

## Visualizations

The notebook includes the following visualizations:

- Overall word cloud
- Positive sentiment word cloud
- Negative sentiment word cloud
- Sentiment distribution chart
- Classification report heatmaps
- Confusion matrices
- City-wise sentiment pie charts
- City ranking based on positive sentiment percentage

## Libraries Used

The main Python libraries used in this project are:

- pandas
- numpy
- nltk
- TextBlob
- BeautifulSoup
- WordCloud
- matplotlib
- seaborn
- scikit-learn
- emoji

## Installation

Install the required libraries using:

```bash
pip install pandas numpy nltk textblob beautifulsoup4 wordcloud matplotlib seaborn scikit-learn emoji lxml
