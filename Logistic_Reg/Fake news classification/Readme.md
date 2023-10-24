# 📰 Fake News Detection

Fake news detection is a crucial application of natural language processing (NLP) and machine learning. It involves the classification of news articles or text documents into two categories: "genuine" or "true" news and "fake" or "misleading" news. The most common logistic regression model models a binary outcome, which can take two values such as true/false, yes/no, and so on. Logistic Regression can be a useful algorithm for this task, especially when combined with NLP techniques. Here's an explanation of how you can use Logistic Regression and NLP for fake news detection:

## 📖 Reading the Data

The data were read differently. All the fake news are stored in 'fake' dataframe and true news are stored in 'genuine' dataframe. A new column was created as target that stores the value as 0 and 1 denoting the fake and true news.

## 📊 Data Visualization
### 🌐 Word Cloud for Both Types of News

Word clouds provide a visual representation of the most frequent words in each class, giving insights into the key terms associated with each type of news. The word's size displayed depends on the number of times the word is repeated. The more the word repeats, the larger its size. As the word 'said' is repeated a large number of times, it is shown in a big size.

## 🛠️ Preprocessing the Data

The dataset has a bunch of strings that determine the output, i.e., news stored as a string defines an output, which is neither categorical data nor an integer. For this, we will apply the following steps:

### 🧹 Concatenating Both Datasets

The datasets of true and fake news, which are stored in two dataframes as 'fake' and 'genuine,' are concatenated using the `concat` function of pandas. Now 'df' is a dataframe that contains both datasets.

*The dataset doesn't have any null values, as we have already confirmed from info. No preprocessing step is required to handle null values.*

### 🗑️ Removing Less Important or Unnecessary Columns

The less important or unnecessary columns are now removed. As the news is classified by text, other features are dropped down.

### 📝 Tokenizing Words

Tokenizing words is an essential step in any natural language processing (NLP) task, including fake news classification. Tokenization is the process of breaking down a text into its individual words or tokens. For example, the sentence "I am a student" is tokenized to get a list of words as ['I', 'am', 'a', 'student'].

### 🌱 Stemming Words Using SnowballStemmer

Stemming is the process of reducing words to their root or base form. Snowball stemmer (also known as the Porter2 stemmer) is a popular stemming algorithm that you can use to perform stemming in various programming languages.

#### Example words for stemming

Words = ["jumping", "jumps", "jumped", "jumping", "happily", "stemmer"] are converted into ['jump', 'jump', 'jump', 'jump', 'happili', 'stemmer'] using the stemmer.

It can be useful in text processing and natural language processing tasks like information retrieval, text classification, and search.

### 🛑 Stopword Removal

Stopwords are words that are commonly used in a language but are generally considered to be of little value in text analysis because they don't carry significant meaning. Examples of stopwords in English include "the," "and," "is," "in," and "it." That's why we can remove it. But here we are removing the words with less than 3 letters.

*Note*: We can use the predefined set of stopwords by importing them from the nltk library.

### 🤝 Joining Text

Using the `join` function, we can join the tokenized words to get back a sentence with stopwords removed and stemmed words.

## 🧩 Splitting into Train and Test Data

The data was split into train and test data. As no parameters were given for splitting the data, the data will automatically be split in the ratio 3:1, i.e., 75 and 25 percent, respectively.

## 📊 Vectorization

Also, we need to convert the data into numerical format in order to train the model. For this, we are using a text feature extraction feature named 'TfidfVectorizer'.

Tfidf (Term Frequency-Inverse Document Frequency Vectorizer) is used to convert a collection of raw text documents into a matrix of numerical features, where each feature represents the importance of a word in a document relative to its importance in a collection of documents (corpus). The higher values represent words that are more important in the context of the entire corpus.

The `max_df` parameter specifies the maximum document frequency for a term (word) in the entire corpus. Document frequency refers to the number of documents in which a term appears. As we have set `max_df=0.7`, the vectorizer will ignore terms that appear in more than 70% of the documents in the corpus.

## 🚀 Training the Model
### 📊 Logistic Regression

Logistic Regression is a popular machine learning algorithm for binary classification tasks like news classification (e.g., distinguishing between fake and real news). It's a simple and interpretable algorithm that served as a good baseline model for this classification task.

The `max_iter` parameter specifies the maximum number of iterations for the solver to converge to a solution. If the specified number of iterations is not sufficient for convergence, you may need to increase it. Conversely, if your model converges quickly, you can reduce `max_iter` to save training time.

## 📈 Performance Metrics

The "accuracy score" is a commonly used metric for evaluating the performance of a classification model. It measures the proportion of correctly predicted instances (or samples) out of the total instances in the dataset. In other words, it tells you how many of the predictions made by your model were correct. From our model, we got an accuracy of 98.35%, which is very high. This means the model has the capability to distinguish things nicely.

## 📊 Visualizing Feature Importance for News Classification

At last, we are visualizing the feature importance for a news classification task. We first retrieve the feature names (words) used in the TF-IDF vectorizer and the coefficients (importance) assigned by the logistic regression model to each feature. The coefficients indicate how important each word is in the classification. We then sort the coefficients in descending order and select the top N important features, in this case, the top 30. We create a horizontal bar chart to display these top features, with the most important ones at the top. This visualization helps us understand which words are highly influential in classifying news articles as either "fake" or "genuine," based on the TF-IDF features and the logistic regression model.

## 👍 Advantages of Logistic Regression

Logistic Regression offers several advantages that make it a valuable choice for binary classification tasks. It provides easily interpretable results, handles irrelevant features well, and is efficient in terms of computation and memory usage. It's suitable for linearly separable data and doesn't assume normality in the residuals. With its probabilistic output and regularization options, Logistic Regression is a versatile and robust method applicable in various fields and works even with small sample sizes.

## 👎 Limitations of Logistic Regression

Logistic Regression has a few downsides. It's not great at handling very complicated, curvy patterns in data; it works better when the relationship between features and outcomes is more straightforward and linear. For complex situations, fancier models can do a better job. Logistic Regression can also struggle if you have lots of features compared to the amount of data you have, which might lead to overfitting. For cases where you're trying to classify things into more than two categories, there are better options out there like Random Forest or Support Vector Machines. But, despite its limitations, Logistic Regression is still a good choice for many simpler classification problems when the data matches its requirements.

## 📚 Get Started with Logistic Regression
- [Greekforgreeks Logistic Regression](https://www.geeksforgeeks.org/understanding-logistic-regression/)
- [Logistic Regression- Wikipedia](https://en.wikipedia.org/wiki/Logistic_regression)
