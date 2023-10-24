# Abalone Age Predictor:

## DataSet: 
 - The given dataset is [Abalone](https://archive.ics.uci.edu/dataset/1/abalone).
 - This dataset contains 8 attributes and a target varibale. It has 1 nominal value and 7 continous values. The detailed description of all these features/attributes are as follows:<br>
        &emsp;&emsp;&emsp;1) Sex: Gender (Male : M, Female : F, Infant : I).<br>
        &emsp;&emsp;&emsp;2) Lenght: Longest shell measurement.<br>
        &emsp;&emsp;&emsp;3) Diameter: Perpendecular to lenght.<br>
        &emsp;&emsp;&emsp;4) Height: with meat in shell.<br>
        &emsp;&emsp;&emsp;5) Whole wieght: weight of the whole abalone.<br>
        &emsp;&emsp;&emsp;6) Shucked weight: weight of the meast in abalone.<br>
        &emsp;&emsp;&emsp;7) Viscera weight: weight of gut(after bleeding).<br>
        &emsp;&emsp;&emsp;8) Shell weight: weight of abalone after being dried.<br>
 - Each attribute describes the physical condition of the abalone which helps in predicting it's age.<br>
 - "Rings" attribute is out target attribute which  tells the age of the abalone.<br>

## Aim of the model:
 - The model should be able to predict the age of abalone by analyzing the 8 attributes of the abalone.<br>
 - "df.drop" function helps in dropping a column in the dataset.<br>
 - We need to drop the "Target" attribute from the dataframe hence we can train our model to predict it after training the model.<br>
 - After dropping it is assigned to new variable and the dataframe with the remaining attributes is assigned into another new variable.<br>

## Test Train Split:
 - Splitting of the data is done using a python library "sklearn" also known as Scikit-Learn. It is used to implement machiene learning models and statistical modelling.<br>
 - **Purpose :** When building a machine learning model, we need to know how it performs on new, unseen data. To do this, we split our available dataset into two parts:<br>
                &emsp;&emsp;&emsp;1)Training set.<br>
                &emsp;&emsp;&emsp;2)Testing set.<br>

 - **Training Set :** The model is trained using the training set. It learns patterns and relationships between the input features and the corresponding target variable in order to make accurate predictions.<br>
 - **Testing Set :** Once the model is trained, it is evaluated using the testing set. The model makes predictions on the testing set based on what it learned during training. The predicted values are compared to the actual target values in the testing set to assess the model's performance.<br>
 - **Performance Assessment :** Various evaluation metrics such as accuracy, precision, recall, or F1 score are used to measure how well the model performs on the testing set. These metrics provide insights into the model's ability to generalize and make accurate predictions on unseen data.<br>
 - By splitting the dataset into training and testing sets, the test-train split helps in estimating the model's performance on new, unseen data and assists in identifying any issues such as overfitting or underfitting before deploying the model in real-world scenarios.<br>

## Model Creation :
 - **Selecting the Model :** We can choose different types of machine learning model based on the problem. There are various models, such as Linear Regression, Random Forests, Support Venture Machines(SVM), etc..<br> 
 - **Data Preprocessing :** It is the process of preparing the raw data before feeding it into a machine learning model. It involves handling missing values, encoding categorical variables, and scaling numerical features. The goal is to clean and transform the data into a suitable format that the model can understand and learn from effectively.<br>
 - **Model Evaluation :** It is the process of assessing how well a machine learning model performs on unseen data. It involves comparing the model's predictions to the actual values or labels and calculating evaluation metrics such as accuracy, precision, recall, or mean squared error. The goal is to understand how accurately the model can make predictions and to determine its effectiveness in solving the problem at hand.<br>
 - I used 6 different Regressors: <br>
            &emsp;&emsp;&emsp;1) Decision Tree Regressor.<br>
            &emsp;&emsp;&emsp;2) K-Nearest Neighbhors Regressor.<br>
            &emsp;&emsp;&emsp;3) Linear Regressor.<br>
            &emsp;&emsp;&emsp;4) Ridge Regressor.<br>
            &emsp;&emsp;&emsp;5) Lasso Regressor.<br>
            &emsp;&emsp;&emsp;6) Support Vector Machine Regressor.<br>

## Model Evaluation:
 - After creating the model with six different regressors. Each regressor have different Mean Squared Error(MSE) and R-Sqaured(R2) score.
 - The MSE for different Regressors are: <br>
            &emsp;&emsp;&emsp;1) Decision Tree Regressor: 8.641<br>
            &emsp;&emsp;&emsp;2) K-Nearest Neighbhors Regressor: 5.384<br>
            &emsp;&emsp;&emsp;3) Linear Regressor: 5.211<br>
            &emsp;&emsp;&emsp;4) Ridge Regressor: 5.204<br>
            &emsp;&emsp;&emsp;5) Lasso Regressor: 7.284<br>
            &emsp;&emsp;&emsp;6) Support Vector Machine Regressor: 5.111<br>
 - The R2 score for different Regressors are: <br>
            &emsp;&emsp;&emsp;1) Decision Tree Regressor: 0.138<br>
            &emsp;&emsp;&emsp;2) K-Nearest Neighbhors Regressor: 0.463<br>
            &emsp;&emsp;&emsp;3) Linear Regressor: 0.480<br>
            &emsp;&emsp;&emsp;4) Ridge Regressor: 0.480<br>
            &emsp;&emsp;&emsp;5) Lasso Regressor: 0.274<br>
            &emsp;&emsp;&emsp;6) Support Vector Machine Regressor: 0.490<br>
 - Based on these two score I have decided to go with Support Vector Machine Regressor(SVR).

## Graphs:
 - I used matplotlib.pyplot and seaborn libraries for plotting graphs.
 - I used a pie chart for representing the percentage of abalones which are Male, Female or Infant.
 - I used a histogram for knowing the no.of abalone with a particular age.
 - I also plotted a scatter graph between lenght and diameter of the abalone.
 - I also plotted a scatter graph between lenght and height of the abalone.
 - I also plotted a scatter graph between height and diameter of the abalone.
 - I also plotted a scatter graph between whole weight and shucked weight of the abalone.
