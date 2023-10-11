# Laptop Price Predictor

Are you looking to buy a laptop? We've developed an ML model trained with XGBRegressor that can predict the price of the laptop you want based on your specifications. This model allows you to easily evaluate the price of a laptop with the specific features you desire, all from the comfort of your chair. Please note that this is a prototype model with certain limitations related to data accuracy due to changes over time and currency formats.

## Dataset

The model is trained on the "Laptop Price Prediction" dataset, which includes various laptop brands and models, along with specifications such as RAM, Storage, Screen size, Operating System (OS), GPU, and Weight.

## Preprocessing and Training

- The dataset is loaded using the Pandas library.
- The 'price' column is dropped, and the remaining data is stored in a DataFrame called `X`.
- Data visualization techniques, including box plots and violin plots from Matplotlib, are used to identify the most influential features for price prediction.

### Feature Insights

- **RAM:** A strong positive correlation is observed between RAM size and laptop price, making RAM an excellent feature for price prediction.
- **Operating System (OS):** It is found that the laptop's price is not solely determined by the OS. Even laptops with no OS cost the same. As a result, the OS feature is dropped from consideration.

## Data Preprocessing

- Unnecessary information, such as 'GB' and 'TB' labels in the Storage column, is removed. TB is converted to GB.
- The 'inch' postfix in the screen size column is removed.
- The Storage class, which contains various storage categories, is one-hot encoded.
- Columns with null values are evaluated, and the OS-related columns are removed.

## Training the Model

- The dataset is split into training and test sets in an 80:20 ratio.
- Categorical columns are one-hot encoded for both training and test data.
- The model is trained using XGBRegressor with 2000 estimators, a learning rate of 0.005, and early stopping rounds set to 10.
- Predictions are made, and the Mean Absolute Error (MAE) of the trained model is determined to be 1,851,231.

## Future Considerations

- Future improvements include training the model with more accurate and up-to-date data, as well as datasets that consider prices for different countries and real-time data.
- This model can currently be used to compare laptop prices, including in different currency formats.
- Fine-tuning model parameters can further improve accuracy.

Please note that this is a simplified representation of the model's development process. Further details and code can be found in the accompanying Python script and Jupyter Notebook.

---

**Disclaimer:** This model is intended for educational and comparative purposes and should be used with awareness of its limitations regarding data accuracy and currency conversion.

