# Fraud Detection Approaches – Summary

This repository summarizes **two different approaches** to tackle the imbalanced fraud detection problem.

---

## Approach 1: Anomaly Detection

* **Model Used:** Isolation Forest
* **Key Points:**
  * Treated fraud cases as **anomalies**.
  * Trained only on the **normal class**.
* **Performance:**
  * **Recall (Fraud):** 0.85 ✅
  * **Training Time:** ~5 seconds ⏱
* **Remarks:**
  * Fast training and good recall, making it suitable for **real-time anomaly detection** scenarios.

---

## Approach 2: Classification with Oversampling

* **Models Tested:** Logistic Regression, XGBoost, Random Forest, KNN, etc.
* **Key Techniques:**
  * Used **SMOTE** to increase the minority class (fraud) in training.
  * Evaluated models using **cross-validation focusing on recall for fraud**.
* **Best Models:**

| Model               | Recall (Fraud) | Training Time | Notes                                                                    |
| ------------------- | -------------- | ------------- | ------------------------------------------------------------------------ |
| Logistic Regression | 0.85           | ~30 seconds   | SMOTE applied; high recall; slower due to oversampling                   |
| XGBoost             | 0.79           | ~2.5 seconds  | No SMOTE needed; handles imbalance via `scale_pos_weight`; fast training |

* **Remarks:**
  * Logistic Regression achieved the **highest recall** but took longer to train due to SMOTE.
  * XGBoost was **faster**, still with good recall, suitable when **training speed is important**.

---

## ✅ Conclusion

* **Anomaly detection (Isolation Forest)** is **fast** and gives **good recall** without oversampling.
* **Classification with SMOTE** allows more **control over minority class detection**, but may increase training time.
* Choice depends on **trade-off between speed and flexibility**:
  * **Real-time monitoring:** Isolation Forest
  * **Thorough offline analysis with higher recall tuning:** Logistic Regression with SMOTE
