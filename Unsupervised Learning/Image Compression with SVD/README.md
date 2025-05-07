# Image Compression with SVD

**Singular Value Decomposition (SVD)** is a technique used to decompose a matrix (like an image) into three components (U, S, Vᵗ). In image processing, SVD allows you to approximate an image using only the most important singular values, which drastically reduces storage while preserving visual quality.

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

The goal is to **compress a grayscale image** by reconstructing it with fewer singular values (lower-rank approximations). The fewer the rank values used, the more compressed (but less detailed) the image becomes.

The code will:
- Display the original image
- Show reconstructions using different ranks (e.g., 1, 5, 10, 20, …)
- Help you visually understand the tradeoff between compression and image quality