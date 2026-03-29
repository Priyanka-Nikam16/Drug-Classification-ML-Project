# Drug-Classification-ML-ProjectDrug Classification Project
Overview
This project builds a machine learning classification model to predict which drug should be prescribed to a patient based on their medical features. Multiple algorithms were tested, and the best-performing model was selected for prediction.
Problem Statement
We aim to predict the Drug type prescribed to a patient using the following features:
1.	Age
2.	Blood Pressure (BP)
3.	Gender
4.	Cholesterol
5.	Na_to_K (Sodium-to-Potassium ratio)
   
Methodology

1. Data Preprocessing
    - Checked dataset for null values and duplicates (none found).
    - Removed 8 outliers using the IQR method.
    - Encoded categorical variables (Gender, BP, Cholesterol, Drug) using LabelEncoder.

2. Exploratory Data Analysis (EDA)
    - Univariate Analysis: Histograms for Cholesterol, BP, Na_to_K distribution.
    - Bivariate Analysis: Correlation heatmap showed:
    - Strongest correlation between Na_to_K and Drug (0.6).
    - Moderate correlation between BP and Drug (0.4).

3. Model Building
    - Train-test split: 70/30.
    - Models tested:
        - Naive Bayes
        - Random Forest Classifier
        - Decision Tree Classifier

4. Model Evaluation
      - Confusion matrices generated for each model.
      - Accuracy scores:
      - Naive Bayes: ~0.85
      - Random Forest: ~0.95
      - Decision Tree: ~0.97

 Best model chosen: Random Forest Classifier (robust and generalizable).

Results

  - Na_to_K ratio is the most influential factor in drug prediction.
  - BP also contributes significantly.
  - Random Forest achieved high accuracy (~95%).
  - The model successfully predicts drug type for new patients.

Example Prediction
For a patient with:
•	Age = 32
•	BP = NORMAL
•	Gender = M
•	Cholesterol = HIGH
•	Na_to_K = 14.5

Predicted Drug: 
    - DrugY (based on trained Random Forest model).

Future Enhancements
  - Hyperparameter tuning for Random Forest.
  - Try ensemble methods (XGBoost, LightGBM).
  - Deploy as a web app for real-time drug prediction.


