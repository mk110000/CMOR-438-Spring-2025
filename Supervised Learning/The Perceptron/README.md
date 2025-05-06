# The Perceptron

The Perceptron is one of the first algorithms used in machine learning and is inspired by how the human brain works. It is mainly used for binary classification, which means it helps decide between two possible outcomes—for example, whether someone has diabetes or not.

The perceptron takes in several inputs (like age, BMI, blood sugar levels), multiplies each by a weight (which the model learns during training), adds them up, and then passes the total through an activation function. This function decides if the result should be a 0 or 1.

Although simple, the perceptron is useful for understanding how machine learning models make decisions. However, it only works well when the data can be separated clearly into two groups (called **linearly separable**). If that’s not the case, more advanced models are needed.

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

The goal is to train a **Perceptron** model on real-world health data and see how well it can predict diabetes. It also shows how to balance the data using **SMOTE** and how to evaluate the model's accuracy.

---

## Instructions to Reproduce Results

1. Run all cells in order.
2. Upload the provided CSV file when prompted.
3. The code will clean the data, train the model, and show the results, including:
   - Model accuracy  
   - A classification report  
   - A confusion matrix  
   - The most important features used by the model