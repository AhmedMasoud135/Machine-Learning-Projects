# Laptop Price Prediction

Predict the price of a laptop in Euros using machine learning, based on its specifications.

---

## 📌 Project Overview

This project aims to build a **high-performance machine learning model** that can accurately predict laptop prices based on various features such as CPU, GPU, RAM, storage, screen resolution, and brand. The challenge was not only building the model but also handling **messy and complex real-world data**.

The final model achieves an **R² score of 0.88**, explaining 88% of the variation in laptop prices — a strong predictive performance.

---

## 🛠️ Technologies & Tools Used

* **Programming Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
* **Development Environment:** Jupyter Notebook
* **Version Control:** GitHub

---

## 🔍 Data Exploration & Preprocessing

The dataset contained raw laptop specifications in various formats. Key preprocessing steps included:

1. **Categorical Feature Handling**

   * Simplified `Company` and `OpSys` features by grouping less frequent categories into “Other”.

2. **Feature Extraction**

   * **Screen Resolution:** Parsed into `Touchscreen`, `IPS`, `X_resolution`, and `Y_resolution`.
   * **CPU & GPU:** Extracted brand, type (integrated/dedicated), GPU family, and model number.
   * **Memory:** Converted complex strings like `"128GB SSD + 1TB HDD"` into separate numerical columns: `SSD`, `HDD`, `Flash_Storage`, and `Hybrid`.

3. **Data Type Conversion**

   * Converted textual units to numeric, e.g., `Ram` from "16GB" → 16, `Weight` from "2.3kg" → 2.3.

4. **Correlation Analysis**

   * Performed heatmap analysis to identify multicollinearity and dropped highly correlated features like `Inches`.

---

## ⚙️ Model Building

* **Algorithm:** XGBoost Regressor (`XGBRegressor`)
* **Train/Test Split:** 80% training, 20% testing
* **Hyperparameters:** Default XGBoost settings 

---

## 📊 Model Evaluation

* **Metric:** R² score
* **Result:** **0.88** — the model explains 88% of laptop price variation.

This indicates a strong predictive capability suitable for real-world pricing insights.

---

## 💡 Key Insights

* Feature engineering is critical for converting unstructured data into valuable predictive features.
* Simple approaches, such as splitting combined memory specs and standardizing units, can dramatically improve model performance.
* Every complex dataset has hidden patterns; extracting these patterns is often the key to a successful ML project.
