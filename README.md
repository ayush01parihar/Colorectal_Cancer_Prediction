# 🧬 Colorectal Cancer Prediction

This project implements a machine learning system to predict the likelihood of colorectal cancer survival based on clinical, demographic, and lifestyle data. It uses a structured MLOps workflow with experiment tracking, model versioning, and a Flask-based user interface, making it suitable for scalable deployment and healthcare research.

---

## 🎯 Objective

To predict 5-year survival outcomes in colorectal cancer patients using clinical and lifestyle features, and deploy the solution with MLOps best practices.

---

## 🩺 Use Case

Early prediction of cancer survival can support oncologists in:
- Personalized treatment planning  
- Healthcare cost estimation  
- Patient risk stratification  

The app allows non-technical users to input patient details and receive survival predictions instantly.

---

## 📊 Dataset Overview

- **Source**: Synthetic healthcare data (`data.csv`)  
- **Features**: 27 attributes including age, tumor size, treatment type, lifestyle factors, and healthcare costs  
- **Target**: `Survival_Prediction` (Yes/No for 5-year survival)

---

## ⚙️ Workflow

### 1. Data Processing
- Loaded and cleaned data using `pandas`
- Encoded categorical variables using `LabelEncoder`
- Applied `StandardScaler` for normalization
- Used `SelectKBest` for feature selection

### 2. Model Training
- Model: `GradientBoostingClassifier`  
- Evaluation: Accuracy, Precision, Recall, F1 Score, ROC AUC  
- Saved artifacts using `joblib`

### 3. Web Application
- Developed with **Flask**
- HTML-based UI form for predictions
- Inputs scaled and passed to model in real-time

### 4. Experiment Tracking
- Tracked with **MLflow**
- Configured for remote tracking via DAGsHub
- Logs include metrics, models, parameters

---

## 📈 Performance

- **Accuracy**: ~90% on test data  
- Robust performance across clinical and lifestyle feature combinations  

---

## 🧰 Tech Stack

- **ML & Data**: Python, Scikit-learn, Pandas, Numpy, Joblib  
- **Web App**: Flask, HTML/CSS  
- **MLOps Tools**: MLflow, DAGsHub  
- **Version Control**: Git, GitHub  

---

## 🔮 Future Improvements

- CI/CD with Jenkins & Docker  
- Cloud deployment using GCP/AWS  
- Model explainability (SHAP/LIME)  
- Enhanced validation with real-world datasets  

---

## 🧪 Example Inputs (UI Form)

| Feature             | Example Value |
|---------------------|----------------|
| Tumor Size (mm)     | 69             |
| Treatment Type       | Combination (encoded) |
| Diabetes             | No (0)         |
| Mortality Rate       | 5              |
| Healthcare Costs ($) | 54,413         |

---

