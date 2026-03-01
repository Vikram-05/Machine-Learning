
# I bulid an AI model that will predict that patient suffer from any `HEART DISEASE` or not

## Heart Disease Prediction Project

This project employs machine learning classification techniques to predict heart disease status based on various health and lifestyle indicators. The analysis utilizes **5 different machine learning models** for comprehensive performance comparison.

## 1. Data Loading and Exploration
- Loaded heart disease dataset from CSV file using `pandas`.
- Examined dataset structure, shape, and column information.
- Initial data inspection to identify missing values and data types.

## 2. Missing Value Handling
- **Numeric columns** (`Age`, `Blood Pressure`, `Cholesterol Level`, `BMI`): Filled with column means.
- **Categorical columns** (`Gender`, `Exercise Habits`, `Smoking`, `Family Heart Disease`, `Diabetes`, `High Blood Pressure`, `Low HDL Cholesterol`, `High LDL Cholesterol`, `Stress Level`, `Sleep Hours`, `Sugar Consumption`, `Triglyceride Level`, `Fasting Blood Sugar`, `CRP Level`, `Homocysteine Level`): Dropped rows with missing values.
- **`Alcohol Consumption`**: Filled with the mode (most frequent value).

## 3. Feature Encoding
- Applied `LabelEncoder` to convert categorical variables into numeric format.
- Encoded columns: `Gender`, `Exercise Habits`, `Smoking`, `Family Heart Disease`, `Diabetes`, `High Blood Pressure`, `Low HDL Cholesterol`, `High LDL Cholesterol`, `Alcohol Consumption`, `Stress Level`, `Sugar Consumption`, and target `Heart Disease Status`.

## 4. Feature Scaling
- Applied `StandardScaler` to normalize all numeric features (excluding target variable).
- Scaling ensures features are on the same scale, improving model performance.

## 5. Train-Test Split
- Split data into training (80%) and testing (20%) sets.
- Used `random_state=45` for reproducibility.

## 6. Model Comparison: 5 Different Models

This project trains and evaluates **5 distinct machine learning models**:

### 1. **Logistic Regression**
- Linear classification model using logistic function.
- Ideal for binary classification problems.

### 2. **K-Nearest Neighbors (KNN)**
- Instance-based learning algorithm.
- Classifies based on nearest neighbors in feature space.

### 3. **Decision Tree**
- Tree-based model using recursive binary splitting.
- Provides interpretable decision rules.

### 4. **Naive Bayes**
- Probabilistic classifier based on Bayes' theorem.
- Assumes feature independence.

### 5. **Support Vector Machine (SVM)**
- Finds optimal hyperplane to separate classes.
- Effective for high-dimensional data.

## 7. Model Evaluation Metrics

For each model, the following metrics are computed:
- **Accuracy**: Overall correctness of predictions.
- **Recall**: Proportion of actual positives correctly identified.
- **F1 Score**: Harmonic mean of precision and recall.
- **Classification Report**: Detailed breakdown of precision, recall, and F1 per class.

## 8. Results and Comparison
- All 5 models are trained on the same training data.
- Predictions are made on the test set.
- Models are compared side-by-side using accuracy, recall, and F1 score.
- Classification reports provide detailed performance insights per class label.

## 9. Conclusion
- The comparative analysis reveals which model performs best for heart disease prediction.
- Trade-offs between model complexity, interpretability, and performance are evaluated.

*This documentation outlines the complete workflow of the heart disease prediction project with multiple machine learning approaches.*