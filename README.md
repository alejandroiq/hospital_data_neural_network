# 🏥 Predicting Hospital Patient Length of Stay with Neural Networks

## 📌 Objective

This project aims to develop a neural network-based regression model to **predict the number of days a patient is expected to stay in the hospital**, based on features like admission type, vital signs, comorbidity scores, and procedures. Accurate predictions can improve bed management, resource allocation, and discharge planning.

---

## 🧠 Approach Overview

1. **Exploratory Data Analysis (EDA)**

   * Statistical summaries and distribution plots
   * Correlation heatmaps and missing value checks

2. **Preprocessing Pipeline**

   * Used `ColumnTransformer` for:

     * Standardizing numerical features
     * One-hot encoding categorical variables
   * Split into training, validation, and test sets

3. **Model Building**

   * Implemented fully connected neural networks using **Keras**
   * Tested 3 optimizers: `SGD`, `RMSprop`, and `Adam`
   * Used `MSE` for loss and `MAE` as the evaluation metric

4. **Training & Tuning**

   * Trained for 50 epochs with early stopping on validation loss
   * Tracked and visualized training and validation performance

5. **Model Evaluation**

   * Selected best model based on **lowest validation loss**
   * Evaluated on the test set: MSE, MAE, RMSE
   * Visualized predicted vs actual values and residuals
   * Performed subgroup error analysis (e.g., age group)

---

## 🔍 Insights for Stakeholders - Recommendations

* The model can predict LOS with an **average error of \~X.XX days**.
* Performance is **consistent across age groups**, showing no demographic bias.
* Most difficult cases tend to be those with **higher procedure counts or longer actual stays**.
* **Only X.X% of predictions are within 2 days** of the actual LOS — suggesting room for improvement with richer clinical features or temporal data.

---

## 🛠️ Tech Stack

* **Language:** Python 3.9
* **Libraries:** TensorFlow/Keras, Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
* To replicate the evaluation, be aware the running time is above 20 minutes per model

## 👤 Author

**Alejandro Silva**
Data Scientist | Energy & Healthcare Analytics
