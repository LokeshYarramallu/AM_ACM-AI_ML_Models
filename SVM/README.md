The link for dataset: https://www.kaggle.com/code/pierra/credit-card-dataset-svm-classification/input
The dataset is related to credit card fraud classification. There are columns like Time, Amount, Class, etc. which are present in the dataset.
Firstly, the dataset is imported and read using pandas.
Then, there are some visualizations which represent the distribution across time, amount, etc. These plots show the scatter plot and the barplot for amount across time.

A correlation matrix is plotted in the notebook. This correlation matrix shows the relation between different variables. 
Then, the dataset is divided into training and testing samples. The training sample is consists of first 1500000 rows and the testing sample consists of remaining half.

The SVM model is created having linear kernel. The model is trained on this SVM model. 
When a confusion matrix is plotted for this predictions, we see that 115757 out of 134807 data rows were classified correctly.

Then we try to optimize the SVM model, by assigning class weights as 0.60 for 0 and 0.40 for 1.

After this optimization, the number of correct classifications increased to 117945 out of 134807.
