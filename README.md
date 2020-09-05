Analytics-Vidya-Hackaton--Loan-Prediction
Loan prediction is a popular hackaton in Analytics vidya where a solution has to be provided to predict whether the loan will be provided or not. The dataset has 13 categories and was a binary classification problem.

Missing values:

Missing values are visualized using Missingno libraries and are imputed with the median in case of Loan amount , mode for categorical values.

Outlier detection:

Outlier are detected using Box plot where the 1.5 quadratile difference are used from the median are used to set a baseline for above and below the median. These points are classified as an outlier and are later removed from the datasets.

Preprocessing:

Loan amount are not normally distributed and these are the primary assumptions for SVM, regression models.So, a log normal is applied to normalize the data for better prediction results.

Encoding:

Label encodings and onehot encodings are tried but later dropped the onhot encoding in the final model as it increases the computation time but no change in accuracy. All the categorical values are converted into labels using lable encoding,

Test and Train Split: Train dataset was splited as two datasets while one been used as a training data set and using the other as a test dataset to validate the model. Stratified K fold is used to split the data as the datasets are imbalanced with higher class 1 variable and lower class 2 target variable.

Modeling:

Models such as Logistic regression, Gaussian, Random forrest, ensembling and stacking was built and tested. Of which logistic regression performed better than other models in public leaderboards with an accuracy of 78.88% and voting classifier performed well in private leader board with an accuracy of 81%.

Overall my model stood at top 15% of all the registered participants in both public and private leaderboard.
