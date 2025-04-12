# 🚀 Predictive Maintenance with MLOps | End-to-End Production-ready Pipeline


## 📌 Overview

This project is a **real-world simulation** of a complete MLOps workflow for Predictive Maintenance using the **Microsoft Azure Predictive Maintenance dataset**. The goal is to identify potential **machine failures** in advance — enabling proactive repairs, reducing downtime, and minimizing costs.

It goes beyond model training — you'll see how this project transitions into **production** with:
- 🚀 Modular architecture
- ⚙️ FastAPI deployment
- 📁 Organized data & code
- 🔁 Retraining-ready structure
- ✅ Designed for CI/CD and monitoring integration

---

## 🎯 Problem Statement

In manufacturing, machines fail unexpectedly, disrupting production and incurring high costs. This project builds a system that:

- ✅ Detects early signs of failure using sensor data
- ✅ Predicts the **type of failure** (5 error types)
- ✅ Provides a ready-to-deploy pipeline with real-time inference capability

---

## 🛠️ Tech Stack

| Category            | Tools/Tech                                      |
|---------------------|--------------------------------------------------|
| Data Manipulation   | pandas, numpy                                    |
| Visualization       | matplotlib, seaborn                              |
| Model Development   | XGBoost, scikit-learn                            |
| Serialization       | joblib                                           |
| Deployment          | FastAPI, Uvicorn, ngrok                          |
| Environment         | Google Colab                                     |
| MLOps Readiness     | Modular folders, retraining & monitoring hooks  |

---

## 📂 Project Structure


<img width="608" alt="Screenshot 2025-04-12 at 7 42 17 PM" src="https://github.com/user-attachments/assets/ea033c09-36df-432f-8ce1-93348755fd34" />


---

## 📊 Dataset Description

**Source:** Microsoft Azure Predictive Maintenance  
**Main Features:**
- `datetime`: Timestamp
- `machineID`: Machine identifier
- `errorID`: One of five failure types (error1 to error5)

**Target:** `errorID` (multi-class classification)

---

## 🧪 EDA Highlights

- Checked for missing values and datatypes
- Visualized class imbalance in `errorID`
- Analyzed trends over time
- Explored feature correlations (filtered out non-numeric issues)

---

## 🤖 Model Building

- **Model Used:** XGBoost Classifier
- **Task:** Multi-class classification of machine failure types
- **Features Used:**
  - Air & process temperatures
  - Torque & rotational speed
  - Tool wear
  - Time-based features (hour, day of week, month)
  - One-hot encoded machine IDs
- **Metrics Evaluated:** Accuracy, Confusion Matrix, Classification Report

---

## 🚀 FastAPI Deployment (Colab + ngrok)

Model deployed using **FastAPI** and served publicly via **ngrok**.

### 🔧 Example Payload

```json
{
  "air_temperature": 295.0,
  "process_temperature": 308.0,
  "rotational_speed": 1450,
  "torque": 45.0,
  "tool_wear": 150,
  "hour": 7,
  "dayofweek": 2,
  "month": 1,
  "machineID_2": 0
}
```


## 🧠 What I Learned

🧱 How to structure scalable ML projects

🌐 Deploying ML models in the cloud (via ngrok)

🧪 Building robust, testable data pipelines

🤝 Merging Data Science with Software Engineering practices

🧰 Laying foundations for CI/CD and model retraining

## 🔥 Future Work

 Add CI/CD with GitHub Actions

 Add Streamlit front-end interface

 Integrate Prometheus + Grafana for monitoring

 Build Docker containers and deploy to GCP/Azure

 Schedule automatic retraining

