# Predicting Readmission Rates of Diabetic Patients with ML

This project focuses on developing predictive models for diabetes classification using machine learning. Two distinct approaches were explored: binary classification and multiclass classification.

### Notebook 1: Binary Classification (SMOTE Applied)

This notebook addresses the binary classification problem: predicting whether a patient is at risk of diabetes.

#### Techniques Used
1. **Data Preprocessing**:
   - **Class Balancing**: SMOTE (Synthetic Minority Oversampling Technique) was employed to balance the minority and majority classes.
   - **Feature Transformation**:
     - Categorical variables were transformed using label encoding and one-hot encoding.
     - Features were normalised using MinMaxScaler to standardise the data range.

2. **Modelling Approach**:
   - A variety of machine learning models were tested, including:
     - Logistic Regression
     - Random Forest
     - Support Vector Machines
   - Hyperparameter tuning was performed via grid search, combined with cross-validation for robust evaluation.

3. **Evaluation Metrics**:
   - **Accuracy**: Overall correctness of predictions.
   - **F1-Score**: A balanced metric considering precision and recall.
   - **ROC-AUC**: Highlighted the discriminative ability of the models.

#### Results
- **Best Model**: Random Forest achieved an ROC-AUC of 0.85, with strong precision and recall scores.
- Feature importance analysis identified key predictors such as age, glucose levels, and prior diagnoses.

---

### Notebook 2: Multiclass Classification

This notebook addresses the complex problem of predicting whether a patient falls into one of three categories: "No Readmission," "Readmitted >30 Days," and "Readmitted <30 Days."

#### Techniques Used
1. **Data Preprocessing**:
   - Extensive feature engineering included merging low-frequency categories and encoding categorical variables.
   - Class imbalance was addressed through upsampling techniques.

2. **Models Tested**:
   - Logistic Regression (One-vs-Rest strategy).
   - Decision Tree and Random Forest classifiers.
   - K-Nearest Neighbours (KNN) and Gaussian Naïve Bayes.

3. **Performance Metrics**:
   - **Accuracy**: Overall success rate of predictions.
   - **Confusion Matrix**: Evaluated class-specific performance.
   - **Macro F1-Score**: Measured performance across imbalanced classes.

#### Results
- **Best Model**: Random Forest achieved the highest accuracy of 62.9%, demonstrating robustness in handling complex multiclass classification.
- **Challenges**: Differentiating between "Readmitted >30 Days" and "Readmitted <30 Days" proved difficult due to overlapping feature distributions.

---

### Conclusion

- The binary classification model provides a reliable approach for identifying at-risk individuals.
- The multiclass classification approach offers more granular insights into patient readmission risks, supporting healthcare providers in resource allocation and treatment planning.

These projects showcase the effective application of statistical and machine learning techniques in healthcare predictive modelling, delivering actionable insights for data-driven decision-making.
