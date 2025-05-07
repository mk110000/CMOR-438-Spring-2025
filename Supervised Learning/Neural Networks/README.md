# Neural Networks

**Neural Networks** are a machine learning method inspired by how the human brain works. They’re made up of layers of connected “neurons” that help the model learn complex patterns in data. Neural networks are especially useful when relationships between inputs and outcomes aren’t obvious or linear.

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

This code builds a **Neural Network** to predict whether someone has diabetes based on their health data. It cleans the data, balances it using **SMOTE**, trains the model using multiple layers, and then checks how accurate the predictions are. It also shows which features were most important to the model.