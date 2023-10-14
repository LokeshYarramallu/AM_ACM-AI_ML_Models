                               Red wine quality prediction
Aim: To predict the quality of red wine using random forest

Model Used:
  Random Forest: A Random Forest is an ensemble machine learning algorithm widely used for classification and regression tasks. It is based on the concept of bagging (Bootstrap Aggregating) and builds multiple decision trees during training to improve predictive accuracy and reduce overfitting.

Contents of dataset:


1 - fixed acidity


2 - volatile acidity


3 - citric acid


4 - residual sugar


5 - chlorides


6 - free sulfur dioxide


7 - total sulfur dioxide


8 - density


9 - pH


10 - sulphates


11 - alcohol


12 - quality (score between 0 and 10)






Steps:


1.Import libraries such as pandas,numpy,seaborn,matplotlib.pyplot and from  sklearn.model_selection imported train_test_split and from sklearn.ensemble import RandomForestClassifier


2.Read dataset using pd.read_csv


3. Displayed the first few rows of a DataFrame and determined the dimensions of dataframe using df.head() and df.shape


4.Check for null values using df.isnull().sum() for data cleaning.From that we arrived at the conclusion there are no null values.


5.Viewed summary statistics and correlation matrix using df.describe() and df.corr(). Statistics can be very helpful in understanding the distribution of your data, identifying outliers, and making informed decisions during the data analysis and preprocessing stages of a machine learning project.correlation matrix is used to understand the linear relationship between numerical variables in your dataset. Correlation is a statistical measure that quantifies the degree to which two variables are related to each other.


6.Dropped column ' quality'.X variable now contains independent variables and y contains target variables.


7.Splitted dataset, 80% for training and 20% for testing


9.Used the random forest classifier on training data and to make predictions on the testing data.Random Forest models are popular for their ability to provide robust and accurate predictions while requiring minimal feature preprocessing.It  builds multiple decision trees during training to improve predictive accuracy and reduce overfitting


10.Tested accuracy
