# Machine Learning Model using Logistic Regression (Titanic Project)

This project demonstrates a logistic regression model to predict whether a passenger on the Titanic would survive based on their attributes. The notebook `Untitled2.ipynb` in this folder contains the full data exploration, preprocessing, training, and evaluation code.

## 📁 Dataset

The dataset for this project is the classic [Titanic passenger dataset]  sns.load_dataset("titanic") containing information such as age, sex, ticket class, and fare. It is available within the repository or can be downloaded from Kaggle.

## 🔍 Data Exploration & Preprocessing

- Inspect `Survived`, `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, and `Fare` features.
- Handle missing values, convert categorical variables (e.g. `Sex`, `Embarked`) to numeric.
- Feature engineering (e.g. family size, title extraction).
- Split data into training and test sets.

## 🧠 Model Training

A logistic regression classifier is trained on the processed features. Key steps include:

1. Scaling numeric features (StandardScaler).
2. Fitting `LogisticRegression` from scikit-learn.
3. Hyperparameter tuning via cross-validation (optional).

## 📊 Evaluation

- Accuracy, precision, recall, F1-score on test set.
- Confusion matrix and ROC curve for visual assessment.
- Discussion of model performance and potential improvements.

## 🚀 Usage

1. Open `Untitled2.ipynb` and run the cells sequentially.
2. Modify preprocessing or model parameters as needed.
3. Use the trained model to make predictions on new passenger data.

## 🧾 References

- Kaggle Titanic Competition
- scikit-learn documentation for logistic regression

---

Feel free to adapt this notebook for similar binary classification tasks!  