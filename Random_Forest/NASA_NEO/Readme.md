# Asteroid Hazard Prediction

This repository contains a Python script for analyzing asteroid data and predicting whether an asteroid is potentially hazardous. The "Is Potentially Hazardous" feature serves as our target variable for classification.

## Code Explanation

1. **Import Required Libraries:**
   - Import the `pandas` and `numpy` libraries for data manipulation.

2. **Parse Dates and Load Data:**
   - Specify the date columns in the CSV file.
   - Read the CSV file "neo_data.csv" into a Pandas DataFrame.
   - Extract the year from the 'Close Approach Date' and store it in a new 'year' column.

3. **Display DataFrame Information:**
   - Use `df.info()` to display information about the DataFrame, including data types and non-null counts.

4. **Display Unique Value Counts:**
   - Use `df.nunique()` to display the count of unique values for each column.

5. **Create a Bar Chart:**
   - Import the `bar` function from Plotly Express.
   - Create a bar chart with 'Limited Name' on the x-axis and 'Orbiting Body' as colors.

6. **Create Histograms:**
   - Import the `histogram` function from Plotly Express.
   - Create two histograms:
     - One to visualize the distribution of 'year' values.
     - Another to visualize the distribution of potentially hazardous asteroids by year.

7. **Prepare Data for Machine Learning:**
   - Import the `RandomForestClassifier` from scikit-learn.
   - Prepare the feature matrix `X` and target variable `y` by removing irrelevant columns.

8. **Build a Random Forest Classifier:**
   - Create a `RandomForestClassifier` model with specific parameters.
   - Fit the model to the feature matrix and target variable.

9. **Analyze Feature Importances:**
   - Calculate and retrieve feature importances.
   - Visualize feature importances using a bar chart.

## Conclusion

This README explains the purpose and functionality of each line of code in the Python script. The script analyzes asteroid data and predicts potential hazards. It demonstrates data manipulation, visualization, and machine learning with a random forest classifier.

