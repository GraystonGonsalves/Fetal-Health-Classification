# Fetal-Health-Classification
Assess a fetus's health using CTG data as Normal, Suspect, or Pathological

In this dataset, 2126 feature extractions from cardiotocogram exams are shared, and they were classified into 3 classes by three expert obstetricians: • Normal • Suspect • Pathological

Project Solution

In order to handle NA values and duplicate records, I use the .isna() function and data.drop_duplicated()
Data Imbalance - Using the oversampling technique, I was able to solve the problem of the variable having very high value counts in one class compared to the other so we could handle the data imbalance.
Multicollinearity - In this case, some of the independent variables are highly correlated to each other, and they must be removed from the dataset when predicting the dependent variable, I used the VIF technique to do this.
For the final step, I tested the model on the test dataset using Logistic Regression and LDA. First, I split the data into a training and test set. Now that the model accuracy has been improved, I have used GridSearchCV to tune the hyperparameters. After that I tested LGBM (Light Gradient Boosted Machine) algorithm on the data to see how it performed. Final Results - Logistic Regression 78% accuracy , LDA 81% accuracy , LGBM - 94 % accuracy.
