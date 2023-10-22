# Objective:- 
* The main aim is to predict the chances of heart failure based on a person's age,health etc factors.
# Data Description:- 
- A total of 12 attributes are present, they are as follows:-
    * age
    * anaemia
    * creatinine_phosphokinase
    * diabetes
    * ejection_fraction
    * high_blood_pressure
    * platelets
    * serum_creatinine
    * serum_sodium
    * sex
    * smoking
    * time
# Procedure:-
1) Firstly downloaded the dataset from kaggle, link to the datset-> https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data
2) Importing necessay libraries and modules.
3) Reading the data using pandas dataframe.
4) Based on the following features we determine the "DEATH_EVENT"
5) Here the dataset is divided into feature(X) and the target variable y
6) Describing the feature X
7) Removing the null values from the dataset using the function "dropna()"
8) Spliting the data into training and testing, 80% for training and 20% for testing purpose.
9) Now applying the classifier
    * Define
    * Fit
    * Predict
    * Evaluate
10) The model used here is Decision Tree Classifier.
11) The mean absolute error is very low and they accuracy of the model is quite good, hence this is the best suitable model for this dataset.
12) Finally a graph is plotted( a tree graph).