# Voting

**Voting** is an ensemble method that combines multiple models (like decision trees, random forests, and logistic regression) and predicts the class that gets the majority vote from those models.

---

## Dataset

The data used for this algorithm is from a health dataset focused on diabetes prediction. It contains information on individuals from various US states, with data ranging from 2015 to 2020.

In this dataset, the goal is to predict the presence of diabetes, represented by the `"diabetes"` column (`0 = no diabetes`, `1 = diabetes`). The dataset includes different variables that may influence diabetes risk, such as:

- **Demographics**: `"age"`, `"gender"`, `"location"`, and race indicators (e.g., `"race:AfricanAmerican"`, `"race:Asian"`, etc)
- **Health conditions**: `"hypertension"`, `"heart_disease"`
- **Lifestyle**: `"smoking_history"`
- **Medical indicators**: `"bmi"` (Body Mass Index), `"hbA1c_level"` (a key measure of blood sugar over time), and `"blood_glucose_level"`
- **Other**: `"clinical_notes"` (brief qualitative observations from a healthcare perspective)

By observing the data, we can see that diabetes risk is likely dependent on a combination of age, BMI, HbA1c level, glucose levels, and pre-existing health conditions. Race and lifestyle behaviors such as smoking history may also contribute to the prediction.

---

## Goal

The goal is to improve prediction accuracy by **combining three different classifiers** to predict whether a patient has diabetes. By using a **voting system**, the code leverages the strengths of multiple models to produce a more robust overall prediction.

---

## Instructions to Reproduce Results

1. Open the code in **Google Colab**.
2. Upload your **CSV file** (must include a `"diabetes"` column).
3. Run each cell in order.  
   The script will:
   - Clean the data  
   - Balance it using **SMOTE**  
   - Build individual classifiers  
   - Combine them using **voting**  
   - Evaluate how well the combined model predicts diabetes