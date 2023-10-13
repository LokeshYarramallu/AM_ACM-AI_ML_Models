# K.SriKausik_S2

This task demonstrates the process of loading a dataset, selecting a target column, splitting it into training and testing sets, and using various classifiers to create a machine learning model for predicting the target.

 # DataSet :

 - The given dataset was [heart-disease-prediction](https://www.kaggle.com/datasets/ritwikb3/heart-disease-statlog).
 - This database contains 13 attributes and a target variable. It has 8 nominal values and 5 numeric values. The detailed description of all these features are as follows:<br>
        &emsp;&emsp;&emsp;1)Age: Patients Age in years (Numeric) <br>
        &emsp;&emsp;&emsp;2)Sex: Gender (Male : 1; Female : 0) (Nominal)<br>
        &emsp;&emsp;&emsp;3)cp: Type of chest pain experienced by patient.This term categorized into 4 category.<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;0: typical angina<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;1: atypical angina<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2: non- anginal pain<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;3: asymptomatic (Nominal)<br>
        &emsp;&emsp;&emsp;4)trestbps: patient's level of blood pressure at resting mode in mm/HG (Numerical)<br>
        &emsp;&emsp;&emsp;5)chol: Serum cholesterol in mg/dl (Numeric)<br>
        &emsp;&emsp;&emsp;6)fbs: Blood sugar levels on fasting > 120 mg/dl represents as 1 in case of true and 0 as false (Nominal)<br>
        &emsp;&emsp;&emsp;7)restecg: Result of electrocardiogram while at rest are represented in 3 distinct values<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;0: Normal <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;1: having ST-T wave abnormality  <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2: showing probable or definite left ventricular hypertrophyby Estes' criteria.<br>
        &emsp;&emsp;&emsp;8)thalach: Maximum heart rate achieved (Numeric)<br>
        &emsp;&emsp;&emsp;9)exang: Angina induced by exercise 0 depicting NO 1 depicting Yes (Nominal)<br>
        &emsp;&emsp;&emsp;10)oldpeak: Exercise induced ST-depression in relative with the state of rest (Numeric)<br>
        &emsp;&emsp;&emsp;11)slope: ST segment measured in terms of slope during peak exercise<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;0: up sloping <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;1: flat<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2: down sloping(Nominal)<br>
        &emsp;&emsp;&emsp;12)ca: The number of major vessels (0–3)(nominal)<br>
        &emsp;&emsp;&emsp;13)thal: A blood disorder called thalassemia<br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;0: NULL <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;1: normal blood flow <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2: fixed defect (no blood flow in some part of the heart) <br>
                &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;3: reversible defect (a blood flow is observedbut it is not normal)(nominal)<br>
        &emsp;&emsp;&emsp;14)target: It is the target variable which we have to predict 1 means patient is suffering from heart disease and 0 means patient is normal.<br>
 - Each attribute describes the medical condition of an individual.<br>
 - "Target" attribute tells us whether the individual is suffering or not suffering from heart disease.<br>

# Aim of the model :
 - The model should be able to predict whether an individual is suffering or not suffering from heart disease by analyzing the first 13 attributes.<br>
 - "df.drop" function helps in dropping a column in the dataset.<br>
 - We need to drop the "Target" attribute from the dataframe hence we can train our model to predict it after training the model.<br>
 - After dropping it is assigned to new variable and the dataframe with the remaining attributes is assigned into another new variable.<br>

 # Test Train Split :
 - Splitting of the data is done using a python library "sklearn" also known as Scikit-Learn. It is used to implement machiene learning models and statistical modelling.<br>
 - **Purpose :** When building a machine learning model, we need to know how it performs on new, unseen data. To do this, we split our available dataset into two parts:<br>
                &emsp;&emsp;&emsp;1)Training set.<br>
                &emsp;&emsp;&emsp;2)Testing set.<br>

 - **Training Set :** The model is trained using the training set. It learns patterns and relationships between the input features and the corresponding target variable in order to make accurate predictions.<br>
 - **Testing Set :** Once the model is trained, it is evaluated using the testing set. The model makes predictions on the testing set based on what it learned during training. The predicted values are compared to the actual target values in the testing set to assess the model's performance.<br>
 - **Performance Assessment :** Various evaluation metrics such as accuracy, precision, recall, or F1 score are used to measure how well the model performs on the testing set. These metrics provide insights into the model's ability to generalize and make accurate predictions on unseen data.<br>
 - By splitting the dataset into training and testing sets, the test-train split helps in estimating the model's performance on new, unseen data and assists in identifying any issues such as overfitting or underfitting before deploying the model in real-world scenarios.<br>

# Model Creation :
 - **Selecting the Model :** We can choose different types of machine learning model based on the problem. There are various models, such as Linear Regression, Random Forests, Support Venture Machines(SVM), etc..<br> 
 - **Data Preprocessing :** It is the process of preparing the raw data before feeding it into a machine learning model. It involves handling missing values, encoding categorical variables, and scaling numerical features. The goal is to clean and transform the data into a suitable format that the model can understand and learn from effectively.<br>
 - **Model Evaluation :** It is the process of assessing how well a machine learning model performs on unseen data. It involves comparing the model's predictions to the actual values or labels and calculating evaluation metrics such as accuracy, precision, recall, or mean squared error. The goal is to understand how accurately the model can make predictions and to determine its effectiveness in solving the problem at hand.<br>
 - I used five different classifiers :<br>
                &emsp;&emsp;&emsp;1) Decision Tree Classifier.<br>
                &emsp;&emsp;&emsp;2) Logistic Regression Classifier.<br>
                &emsp;&emsp;&emsp;3) Gradient Boosting Classifier.<br>
                &emsp;&emsp;&emsp;4) K-Nearest Neighbors Classifier.<br>
                &emsp;&emsp;&emsp;5) Naive Bayes Classifier.<br>

# Model Evaluation:

 - After creating the model with four different classifiers. Each classifier have different accuracy in predicting the value.
 - The accuracy scores for differant classifiers are :<br>
                &emsp;&emsp;&emsp;1) Decision Tree Classifier = 0.630<br>
                &emsp;&emsp;&emsp;2) Logistic Regression Classifier = 0.926<br>
                &emsp;&emsp;&emsp;3) Gradient Boosting Classifier = 0.741<br>
                &emsp;&emsp;&emsp;4) K-Nearest Neighbors Classifier = 0.963<br>
                &emsp;&emsp;&emsp;5) Naive Bayes Classifier = 0.926<br>
 - Based on the accuracy scores K-Nearest Neighbors Classifier has performed better with a accuracy score of 0.963(96.3%).
 - This indicated it did better than the other classifier.
# Graphs:

 - I used matplotlib.pyplot and seasborn library for plotting graphs.
 - I represented no.of indidividuals with and without heart disease using a pie-chart.
 - I plotted a scatter plot with "BP" on x-aixs and "Cholesterol" on y-axis with "target" as my hue. From this plot we can the  relationship between Cholesterol and BP of those who are suffering or not suffering with heart disease.
 - I plotted a scatter plot with "BP" on x-aixs and "age" on y-axis with "target" as my hue. From this plot we can the  relationship between age and BP of those who are suffering or not suffering with heart disease.
 - I plotted a scatter plot with "Cholesterol" on x-aixs and "age" on y-axis with "target" as my hue. From this plot we can the  relationship between age and Cholesterol of those who are suffering or not suffering with heart disease.
 - I plotted a histogram along with kde(Kernel Density Estimation) to indicate the relationship of age and BP.
 - I plotted a histogram along with kde(Kernel Density Estimation) to indicate the relationship of age and Cholesterol.