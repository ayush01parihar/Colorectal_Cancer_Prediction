🧬 Colorectal Cancer Prediction
This project implements a machine learning system to predict the likelihood of colorectal cancer survival based on clinical, demographic, and lifestyle data. It uses a structured MLOps workflow with experiment tracking, model versioning, and a Flask-based user interface, making it suitable for scalable deployment and healthcare research.

🎯 Objective
To predict 5-year survival outcomes in colorectal cancer patients using clinical and lifestyle features, and deploy the solution with MLOps best practices.

🩺 Use Case
Early prediction of cancer survival can support oncologists in personalized treatment planning, healthcare cost estimation, and patient risk stratification. The app allows non-technical users to input patient details and receive survival predictions instantly.

📊 Dataset Overview
Source: Synthetic healthcare data (data.csv)

Features: Includes 27 attributes such as age, tumor size, treatment type, lifestyle factors, and healthcare costs.

Target: Survival_Prediction (Yes/No for 5-year survival)

⚙️ Workflow
1. Data Processing
Loaded and cleaned data using pandas

Encoded categorical variables with LabelEncoder

Applied SelectKBest for feature selection

Standardized data using StandardScaler

2. Model Training
Used GradientBoostingClassifier for classification

Tracked training metrics (accuracy, precision, recall, ROC AUC) using MLflow

Serialized model and scaler with joblib

3. Web Application
Built a web interface using Flask

Integrated trained model to predict survival based on form input

Served predictions dynamically via /predict endpoint

4. Experiment Tracking
MLflow setup for logging metrics and storing model versions

Integrated with DAGsHub for remote tracking (via MLFLOW_TRACKING_URI setup)

🧪 Key Features
Form-based user input for real-time survival prediction

Dynamic web dashboard with Flask templating

Model and scaler loading via joblib

Modular code architecture using custom logging and exceptions

Prepared for scalable deployment with future integration of CI/CD and cloud services

📈 Performance
Model Used: Gradient Boosting Classifier

Accuracy: ~90% (based on test data)

Metrics Tracked: Accuracy, Precision, Recall, F1 Score, ROC AUC

🧰 Tech Stack
Languages & Libraries: Python, Scikit-learn, Pandas, Numpy, Joblib

Web App: Flask, HTML/CSS (via Jinja templates)

MLOps Tools: MLflow, DAGsHub

Version Control: Git, GitHub
