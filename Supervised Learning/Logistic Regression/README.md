# Logistic Regression

**Logistic Regression** is a supervised machine learning algorithm used for classification. It predicts the probability that something belongs to a particular class—like whether someone has diabetes (`1`) or not (`0`)—based on input features.

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

The goal is to train a **Logistic Regression model** that can accurately predict diabetes using patient data. The model is trained on a **balanced dataset** (using **SMOTE** to handle class imbalance), and its performance is evaluated using:

- **Accuracy**
- **Classification report**
- **Confusion matrix**
- A **plot showing the top features** that influence predictions

---

## Instructions to Reproduce Results

1. Open the code in **Google Colab**.
2. Upload your dataset (a **CSV file** with a `"diabetes"` column and patient features).
3. Run each code cell step by step.  
   The script will:
   - Clean your data  
   - Balance the dataset using **SMOTE**  
   - Train the **Logistic Regression model**  
   - Evaluate performance  
   - Highlight the most important predictive features