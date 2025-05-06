# Linear Regression

**Linear Regression** is a basic machine learning algorithm that finds a straight-line relationship between the input variables (like age or blood pressure) and a numeric outcome. It’s often used to predict values based on patterns in the data.

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

The code is trying to predict the chances of someone having diabetes based on their medical data. It prepares the data, balances it using **SMOTE** to avoid bias, builds a **Linear Regression** model, and then checks how well the model predicts using evaluation metrics and graphs.

---

## Instructions to Reproduce Results

1. Open the code in **Google Colab**.
2. Upload your own CSV file with similar medical features and a `"diabetes"` column.
3. Run the cells in order — this will:
   - Clean the data  
   - Train the model  
   - Show predictions through plots and metrics