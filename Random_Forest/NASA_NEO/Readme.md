# NEO(Near Earth Oject)  NASA Data Analysis 

This repository contains code and data for analyzing Near-Earth Object (NEO) data and building a machine learning model to classify potentially hazardous NEOs.

## Dataset

The dataset used in this project is sourced from [(https://www.kaggle.com/datasets/shivd24coder/nasa-neo-near-earth-object-dataset)]. It includes information about NEOs such as their names, designations, sizes, velocities, and whether they are potentially hazardous.

## Data Preprocessing

- The dataset is loaded into a Pandas DataFrame.
- Date columns are parsed to enable date-based analysis.
- A new 'year' column is created to extract the year from the 'Close Approach Date.'

## Exploratory Data Analysis (EDA)

- Basic statistics and information about the dataset are obtained using `.info()` and `.nunique()` functions.
- A stacked histogram is created to visualize the distribution of hazardous and non-hazardous NEOs.

## Machine Learning

- A RandomForestClassifier is used for building a machine learning model.
- The dataset is split into training and test sets.
- The model is trained on the training set and used to make predictions on the test set.
- The accuracy of the model's predictions is calculated using `accuracy_score`.

