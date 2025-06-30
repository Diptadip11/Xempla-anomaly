# Xempla-anomaly

# ⚡ Energy Anomaly Detector – Smart Building Monitoring

> Built for the Xempla ML Internship | Decision Intelligence R&D (2025)

---

## 📌 Overview

This project implements an anomaly detection system for smart building energy usage, inspired by Xempla’s mission of building intelligent, autonomous decision systems. Using real-world power consumption data, we detect and explain unusual energy behaviors such as equipment faults, inefficiencies, or unplanned usage.

---

## 📊 Dataset

- **Source**: UCI Individual Household Electric Power Consumption Dataset  
  https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption
- **Sampling**: 1-minute resolution
- **Time range used**: Jan 1–15, 2007
- **Features Used**:
  - `Global_active_power`
  - `Voltage`
  - `hour` of the day
  - `day_of_week`
  - `total_sub_metering` (sum of submeter 1, 2, 3)

---

## 🧠 Approach

### 🔍 Model: Isolation Forest
- Unsupervised anomaly detection
- Learns normal consumption patterns and isolates rare behavior
- Scales well to large, high-dimensional tabular data

### 🧠 Explainability: SHAP
- Trained a surrogate Random Forest model on Isolation Forest’s labels
- Applied SHAP to understand which features contribute most to anomaly detection
- Example insight: High power usage during off-hours with low submetering → likely anomaly

---

## 📈 Results

- ~3% of the data was flagged as anomalous (configurable)
- Visual time series highlights unusual spikes
- SHAP summary plot provides interpretability:

![SHAP Summary Plot](shap_summary.png)

---

## ✅ Why This Project Matters

This system simulates a real-world decision support tool for operations and maintenance (O&M) teams:

- **Early detection** of inefficiencies or faults
- **Explains** what triggered anomalies
- Aligns with Xempla's focus on **energy efficiency**, **autonomous decision loops**, and **real-time feedback systems**

---

## 🛠️ Tech Stack

- Python 3.11
- pandas, scikit-learn
- SHAP, matplotlib
- (Optional) Streamlit for dashboard

---

## 🚀 Future Scope

- Integrate a **Streamlit UI** for real-time anomaly monitoring
- Add **feedback loop** for retraining the model based on operator inputs
- Expand to multiple buildings/zones
- Use **autoencoder or time-series models** for temporal anomaly detection

---

## 👤 Author

Diptadip Choudhury  
[GitHub](https://github.com/diptadip) | [Instagram](https://instagram.com/diptadip__)  

---

## 📬 Submission

- Loom video link: [INSERT HERE]
- GitHub repo: [INSERT REPO LINK]
- Submitted to: **Xempla ML Intern – Decision Intelligence R&D**  
  `workofourlife@xempla.io`

---
