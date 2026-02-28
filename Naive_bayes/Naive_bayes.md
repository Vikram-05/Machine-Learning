# Naive Bayes Classification

This notebook demonstrates a Naive Bayes classifier applied to the Titanic dataset using `scikit-learn`. The goal is to predict passenger survival based on available features.

## 1. Libraries and Data Loading
- Imported common data science libraries: `numpy`, `pandas`, `seaborn`, `matplotlib`, etc.
- Loaded the Titanic dataset via `sns.load_dataset('titanic')`.

## 2. Data Cleaning and Preprocessing
- Dropped irrelevant columns: `who`, `deck`, `alive`.
- Encoded categorical variables (`sex`, `embarked`, `class`, `adult_male`, `embark_town`, `alone`) using `LabelEncoder`.
- Scaled numerical features (`pclass`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `class`, `embark_town`) using `StandardScaler`.
- Filled missing `age` values with the column mean.

## 3. Feature Selection and Splitting
- Created `X` by dropping the target column `survived`.
- Set `Y` as the `survived` column.
- Split data into training and testing sets (80/20) with `random_state=45`.

## 4. Model Training
- Initialized a `GaussianNB` model.
- Trained the model on the training data.

## 5. Prediction and Evaluation
- Predicted survival on the test set.
- Calculated accuracy score.
- Generated confusion matrix and classification report to assess performance.

## 6. Results
- Discuss accuracy and insights from confusion matrix / report.

*This markdown file mirrors the steps performed in the associated notebook.*