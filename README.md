# ElectionSentiment: 2024 U.S. Presidential Race Sentiment Analysis

## Project Overview
This project analyzes social media sentiment data from X (formerly Twitter) related to the 2024 U.S. Presidential Election. Using natural language processing and machine learning techniques, the analysis classifies tweets about presidential candidates as positive, neutral, or negative, providing insights into public perception during the election cycle.

## Dataset
The dataset contains tweets related to the 2024 U.S. Presidential Election candidates, including sentiment labels and engagement metrics.

### Data Source
- **Source:** [2024 U.S. Election Sentiment on X](https://www.kaggle.com/datasets/emirhanai/2024-u-s-election-sentiment-on-x)
- **Description:** This dataset contains tweets about the 2024 U.S. presidential candidates, capturing public sentiment, discussions, and engagement from January to February 2025.

### Data Features
| Feature | Type | Description |
|---------|------|-------------|
| tweet_id | numeric | Unique identifier for each tweet |
| user_handle | string | Anonymized handle of the user who posted the tweet |
| timestamp | datetime | Date and time when the tweet was posted |
| tweet_text | string | Content of the tweet |
| candidate | string | Presidential candidate referenced in the tweet |
| party | string | Political party of the candidate |
| retweets | numeric | Number of retweets |
| likes | numeric | Number of likes |
| sentiment | string | Sentiment label (positive, neutral, negative) |


## Methodology
1. **Data Exploration and Visualization**:
   - Distribution of tweets by candidate
   - Overall sentiment distribution
   - Sentiment breakdown by candidate

2. **Text Preprocessing**:
   - Special character removal
   - Single character removal
   - Multiple space replacement
   - Lowercase conversion

3. **Feature Engineering**:
   - TF-IDF vectorization with 2500 features
   - Stopword removal
   - Document frequency filtering (min_df=7, max_df=0.8)

4. **Model Development**:
   - Random Forest Classifier with 200 estimators
   - 80% training, 20% testing split

## Results
The sentiment analysis model achieved excellent performance:
- **Accuracy**: 97.50%
- **Precision, Recall, and F1-Score**:
  - Negative sentiment: 0.93, 0.93, 0.93
  - Neutral sentiment: 0.92, 1.00, 0.96
  - Positive sentiment: 1.00, 0.98, 0.99

### Sentiment Distribution Highlights
- Distribution varies significantly across candidates
- Visualization of sentiment breakdown shows distinct patterns by political party
- The model successfully identifies nuanced sentiment in political discourse

## Requirements
```
pandas
numpy
matplotlib
seaborn
nltk
scikit-learn
re
```

## Usage
The notebook contains a complete workflow:
1. Load and explore the Twitter dataset
2. Preprocess tweet text
3. Create TF-IDF features
4. Train a Random Forest classifier
5. Evaluate model performance
6. Test on sample tweets


## Conclusion
This analysis demonstrates the effectiveness of machine learning in classifying political sentiment on social media with high accuracy. The results provide valuable insights into public perception of presidential candidates during the 2024 election cycle.
