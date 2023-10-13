Objective:- The main aim is to predict the prices of the houses based on certain features
Data Description:-
A total of 16 attributes are present. The attributes(features) are as follows:- 
1. bedrooms
2. bathrooms
3. sqft_living
4. sqft_lot
5. floors
6. waterfront
7. condition
8. sqft_above
9. sqft_basement
10. yr_built
11. yr_renovated
12. view
13. street
14. city
15. statezip
16. country

Procedure:-
1. Firstly downloaded the dataset from kaggle, link to the datset-> https://www.kaggle.com/datasets/shree1992/housedata/data
2. After loading the dataset,loaded the dataset into a pandas dataframe for further analysis and processing.
3. Loaded the dataset using pd.read_csv
4. Here we are droping the attribute "date" along with it's column axis, and the dataset is divided into feature(X) and the target variable(y), the features are stored in X, and the corresponding target variable values are stored in y, allowing for the application of machine learning algorithm.
5. Describing the features X
6. The original cateogorical values are replaced with their corresponding numerical representation.The encoding process assigns a unique numerical label to each unique category within each column, representing the order or rank of the categories.
7. Spliting the data into training and testing, 80% for training and 20% for testing purpose.
8. Now as the dataset contains strings along with integers used "OrdinalEncoder" to modify the data, firstly created an instance of OrdinalEncoder, then used "fit_transform" method of the OrdinalEncoder class which fits the encoder on the specified columns and then transforms those columns into ordinal-encoded values.
9. The original cateogorical values are replaced with their corresponding numerical representation.The encoding process assigns a unique numerical label to each unique category within each column, representing the order or rank of the categories.
10. The four major steps in model training i.e
a. Define
b. Fit
c. Predict
d. Evaluate
are performed
11. The model used here is Linear Regression
12. Mean absolute error is evaluated.
13. Two different types of graphs are plotted, Scatter and Histogram(Residual Histogram).In the graph plots we have plotted a graph of actual vs expected.