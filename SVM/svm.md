# Support Vector Machine (SVM) Classification

This notebook demonstrates using a Support Vector Machine classifier (with an RBF kernel) on the Titanic dataset.  The objective is to predict passenger survival using features from the dataset and evaluate the model’s performance.

## 1. Importing Libraries and Data
- Loaded standard data analysis libraries (`numpy`, `pandas`, `seaborn`, `matplotlib`, etc.).
- Imported Titanic dataset via `sns.load_dataset('titanic')`.

## 2. Data Cleaning and Encoding
- Dropped columns not needed for prediction: `who`, `deck`, `alive`.
- Converted categorical variables (`sex`, `embarked`, `class`, `adult_male`, `embark_town`, `alone`) using `LabelEncoder`.
- Applied `StandardScaler` to numeric features (`pclass`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `class`, `embark_town`).
- Imputed missing `age` values with the column mean.

## 3. Preparing Features and Target
- Defined feature matrix `X` by excluding the `survived` column.
- Target vector `Y` set to `survived`.
- Split data into training and testing sets (80/20 split) with `random_state=45`.

## 4. Model Building
- Initialized `SVC` with an RBF kernel.
- Trained the model on the training dataset.

## 5. Predictions and Evaluation
- Predicted survival outcomes on the test set.
- Computed accuracy score.
- Generated a confusion matrix and classification report for detailed metric analysis.

## 6. Summary of Results
- Discuss accuracy and insights from confusion matrix and report, highlighting performance characteristics of the SVM model.

*The markdown reflects the steps executed in the associated notebook.*