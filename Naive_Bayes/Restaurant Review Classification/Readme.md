# Restaurant Reviews Classification

This machine learning model is designed to help restaurant owners and managers to better understand and prioritize their strengths and weaknesses based on customer feedback. The model classifies reviews into positive and negative categories to provide valuable insights into the restaurant's performance.

## Model Used
**Gaussian Naïve Bayes:**
Gaussian Naive Bayes is a probabilistic classification algorithm that applies Bayes' theorem with strong independence assumptions. It helps classify reviews as positive or negative based on their text content.

## Data Loading
The model uses a dataset in TSV (Tab Separated Value) format, imported and processed using Pandas DataFrame.

## Exploring the Data
The dataset is explored to understand its characteristics. It consists of a DataFrame with 2 columns and 1000 rows. Data visualization, particularly using Seaborn, reveals that half of the reviews are positive and half are negative. The length of reviews ranges from 11 to 149 characters.

## Data Preprocessing
Stopwords in English are removed using the NLTK library. Stopwords are words that do not significantly affect the meaning of a sentence. Additionally, the words are stemmed to reduce them to their base form (e.g., 'wanted' to 'want').

## Feature Extraction
The preprocessed data is then passed through CountVectorizer, a common feature extraction technique in Natural Language Processing (NLP) that converts text data into numerical features suitable for machine learning models.

## Model Training
The reviews, represented as bags of words, are split into a 3:1 ratio for training and testing. The Gaussian Naïve Bayes Classifier is fitted to the data and predictions are made. The model outputs '1' for positive reviews and '0' for negative reviews.

## Performance Metrics
Performance metrics, including accuracy, true positives, true negatives, false positives, and false negatives, are calculated using the scikit-learn library. The model achieved an accuracy of 73%, with 55% true positives, 91% true negatives, 42% false positives, and 12% false negatives.

## Model Deployment
The trained model can be deployed by loading it through a pickle file, making it ready for use by restaurant owners, managers, and customers.

This NLP-based Gaussian Naïve Bayes classifier provides a valuable tool for classifying restaurant reviews as either positive or negative, helping the restaurant industry make informed decisions based on customer feedback.
