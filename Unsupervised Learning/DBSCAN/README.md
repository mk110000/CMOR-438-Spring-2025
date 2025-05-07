# DBSCAN

**DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** is an unsupervised algorithm that groups data points based on how closely packed they are. It finds clusters of points that are near each other and labels outliers as noise. You don’t need to tell it how many clusters to look for—it figures that out on its own.

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

The goal is to explore patterns in the data using **DBSCAN**, which helps find natural groupings (clusters) in the health data. Even though we know who has diabetes, this method tries to group patients based only on patterns in their features—**without using the diabetes labels during training**. The results are visualized in a **scatter plot** and compared with actual labels for evaluation.