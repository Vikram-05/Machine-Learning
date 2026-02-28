# Decision Tree Classification

This notebook applies a Decision Tree classifier to the Titanic dataset using `scikit-learn`. The aim is to predict passenger survival based on available features and evaluate model performance.

## 1. Setup and Data Loading
- Loaded essential libraries (`numpy`, `pandas`, `seaborn`, `matplotlib`, etc.).
- Data sourced from `sns.load_dataset('titanic')`.

## 2. Data Preparation
- Removed redundant columns: `who`, `deck`, `alive`.
- Encoded categorical features (`sex`, `embarked`, `class`, `adult_male`, `embark_town`, `alone`) with `LabelEncoder`.
- Standardized numeric attributes (`pclass`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `class`, `embark_town`) via `StandardScaler`.
- Imputed missing `age` values using the column mean.

## 3. Feature and Target Split
- Defined `X` as features excluding `survived`.
- Set `Y` to the target `survived` column.
- Performed an 80/20 train-test split with a fixed random state for reproducibility.

## 4. Model Training
- Initialized a `DecisionTreeClassifier` (with `random_state=42`).
- Fitted the model on training data.

## 5. Evaluation
- Generated predictions on the test set.
- Calculated accuracy score.
- Created confusion matrix and classification report to inspect precision, recall, and F1-scores.

## 6. Observations
- Summarize how well the decision tree performs and any notable patterns from the metrics.

*This documentation mirrors the code flow present in the notebook.*