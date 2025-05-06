# K-Means Clustering

**K-Means Clustering** is an unsupervised learning algorithm that groups similar data points into clusters based on their features. For instance, you might be clustering a diabetes dataset into 2 groups, aiming to see if they align with diabetes vs. no diabetes.

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

The goal is to apply **K-Means** to find natural groupings in the dataset and visualize them. You then compare the clustering results to the actual diabetes labels to see how well the clusters reflect true outcomes. **PCA** (Principal Component Analysis) is used here to reduce the feature space to 2D for easier plotting and interpretation.

---

## Instructions to Reproduce Results

1. Open the code in **Google Colab**.
2. Upload a **CSV file** that includes a diabetes column and remove any unnecessary columns like `year` or `clinical_notes`.
3. The script standardizes the features, applies **K-Means clustering** (with 2 clusters), and projects the data into 2D using **PCA**.
4. It produces two plots:
   - One colored by **true diabetes labels**
   - Another colored by **K-Means cluster assignments**