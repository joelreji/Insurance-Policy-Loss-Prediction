# Insurance-Policy-Loss-Prediction
Insurance Policy Loss Ratio Prediction based on policy sets.

These notebooks outline the data processing steps used to predict loss ratios of varying policy "portfolios".

Loss ratio is the number of policies in a portfolio that has losses.
Portfolios are a collection of policies with varying sizes, loss ratios, and samples.

**Below is the flow of the prediction algorithm:**

1. **Cleaning.ipynb:** does basic data clean up and picks the input variables
2. **Generate_train_portfolios-summary.ipynb:** takes the cleaned data and creates varying sample portfolios. Creates a new data set which summarizes each portfolio based on input variable type.
3. **Generate_test_portfolios_summary.ipynb:** creates a new data set which summarizes each testing sample portfolio.
4. **Modeling_traindata_only.ipynb:** builds various models on the training data only to find the best matching model. Here are some models tried: Linear Regression, Ridge Cross Validation, Lasso Cross Validation, XGBoost etc.
5. **Modeling.ipynb:** takes the best model from the train data set and apply them and run a Root Mean Squred Error comparison on the testing set. Builds kaggle submission.

The final model built was built using Support Vector Regression, which won first place on the Kaggle competition! 
