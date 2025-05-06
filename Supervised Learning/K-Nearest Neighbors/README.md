# K-Nearest Neighbors

**K-Nearest Neighbors (KNN)** is a simple algorithm that predicts outcomes based on the closest data points. It checks which training samples are “nearest” to a new sample and chooses the most common label among them. It's kind of like asking your neighbors for advice and going with the majority.

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

The goal is to predict whether someone has diabetes using their health data. The code:

- Cleans the data  
- Balances it using **SMOTE**  
- Scales the features (important for KNN)  
- Trains the KNN model  
- Evaluates prediction accuracy  

It also displays a **confusion matrix** to compare actual vs predicted outcomes.

---

## Instructions to Reproduce Results

1. Open the code in **Google Colab**.
2. Upload a CSV file with a `"diabetes"` column and other health-related features.
3. Run each code block step-by-step.  
   This will:
   - Train the KNN model  
   - Make predictions  
   - Show evaluation results