# Decision Trees

A **Decision Tree** is a supervised machine learning algorithm used for classification. It splits the data into branches based on feature values, helping it learn simple decision rules to classify whether a patient has diabetes or not.

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

The goal is to build a **Decision Tree model** to predict diabetes using patient data. The code balances the dataset using **SMOTE**, trains the tree, evaluates its performance with metrics like **accuracy** and a **confusion matrix**, and visualizes both the **full tree** and the **top features** that influenced the decision-making process.