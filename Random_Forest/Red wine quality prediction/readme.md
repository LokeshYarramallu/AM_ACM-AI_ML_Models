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
1.Import libraries
2.Read dataset
3.Determine the dimensions of dataframe
4.Check for null values
5.Viewed summary statistics and correlation matrix
6.Dropped column quality.X variable now contains independent variables and y contains target variables.
7.Splitted dataset, 80% for training and 20% for testing
9.Used the random forest classifier on training data and to make predictions on the testing data
10.Tested accuracy
