# Crop Prediction Using Soil Metrics

This project predicts the most suitable crop based on soil metrics, such as **Nitrogen (N)**, **Phosphorus (P)**, **Potassium (K)** levels, and **pH value**. It utilizes Logistic Regression and Random Forest classifiers, employing hyperparameter tuning and cross-validation to ensure robust performance.

---

## Features
- **Dataset**: Includes soil metrics (`soil_measures.csv`) with crop recommendations.
- **Model Comparison**:
  - Logistic Regression with hyperparameter tuning.
  - Random Forest Classifier for comparative analysis.
- **Cross-validation**: Evaluates model generalizability.
- **Feature Importance**: Identifies the most influential soil metrics.
- **Custom Crop Prediction**: A function for predicting crops based on new soil data.

---

## Requirements
Install the required libraries:
```bash
pip install pandas scikit-learn
```

---

## Dataset
The dataset contains:
- **Features**:
  - `N`: Nitrogen level
  - `P`: Phosphorus level
  - `K`: Potassium level
  - `ph`: pH value
- **Target**: `crop` (categorical variable representing the recommended crop)

---

## Workflow
1. **Data Preprocessing**:
   - Handle missing values.
   - Split the dataset into training (80%) and test (20%) sets.
   - Scale features using `StandardScaler`.

2. **Logistic Regression**:
   - Perform hyperparameter tuning using `GridSearchCV` to optimize `C` (regularization) and solver.
   - Evaluate using accuracy, F1-score, and cross-validation scores.

3. **Random Forest Classifier**:
   - Train a Random Forest model as a comparison.
   - Evaluate using accuracy and F1-score.

4. **Feature Importance**:
   - Analyze the contribution of each soil metric to the model.

5. **Crop Prediction Function**:
   - Accepts soil metrics (N, P, K, pH) as input.
   - Outputs the most suitable crop.

---

