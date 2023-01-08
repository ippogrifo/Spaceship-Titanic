# Spaceship-Titanic
Dataset: Spaceship Titanic (https://www.kaggle.com/competitions/spaceship-titanic/data) Task: Predict the column "Transported" Model unsed: Logistic Regression Average Score: 78.8 achieved on X_test dataset

# Procedure highlights:

- Filled the "CryoSleep" column's Nulls leveraging the sum of the expenses columns. This because Cryosleep showed the highest correlation with the target column, and it had a high negative correlation with the expenses columns
- To optimise performance, I ordered the columns based on their absolute-value correlation with the Transported column. Then, I recursively dropped the columns starting from the one with the lowest correlation, then ran logistic regression on the remaining, and finally picking the column combination that gave me the highest score (function: find_best_model).

# Next steps:

- Improve data cleaning: fill more Nulls
- Try the option of getting read of the highly correlated parameters
- Apply a different model
