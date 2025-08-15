# 🍷 Wine Quality Prediction using MLOps & AWS EC2  

## 📌 Overview  
This project implements a **fully automated MLOps pipeline** to predict wine quality based on physicochemical properties. It demonstrates end-to-end machine learning development — from **data ingestion and preprocessing** to **model training, experiment tracking, containerization, CI/CD automation, and cloud deployment** on **AWS EC2**.  

The solution replicates a **production-grade ML system**, ensuring reproducibility, scalability, and maintainability.  

---

## 🎯 Objective  
- Predict wine quality (0–10 score) based on features such as acidity, pH, alcohol content, sulphates, etc.  
- Deploy the solution in an automated and reproducible cloud environment.  

---

## 📊 Dataset  
- **Source:** [UCI Machine Learning Repository – Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)  
- **Size:** ~1,600 rows, 12 columns  
- **Target Variable:** `quality` (integer score)  
- **Features:**  
  - Fixed acidity, volatile acidity, citric acid  
  - Residual sugar, chlorides, free sulfur dioxide  
  - Total sulfur dioxide, density, pH, sulphates, alcohol  

---

## 🛠️ Tools & Technologies  
- **Languages/Libraries:** Python, scikit-learn, pandas, seaborn  
- **MLOps Tools:** MLflow, DAGsHub  
- **Containerization:** Docker  
- **CI/CD:** GitHub Actions  
- **Cloud:** AWS EC2, AWS ECR  
- **Web Framework:** Flask  

---

## ⚙️ Methodology  
1. **Data Ingestion & Validation**  
   - Automated ingestion pipeline with schema checks (column names, counts, data types).  
2. **Data Preprocessing**  
   - Standard scaling of features  
   - Saving transformation pipeline for reproducibility  
3. **Model Training & Evaluation**  
   - Models used: Linear Regression, Random Forest Regressor, XGBoost Regressor  
   - Evaluation metrics: R², MAE, RMSE  
   - Best model: **Random Forest Regressor**  
4. **Experiment Tracking**  
   - MLflow & DAGsHub for parameter, metric, and artifact tracking  
5. **Containerization**  
   - Dockerfile for environment consistency  
6. **CI/CD Pipeline**  
   - GitHub Actions workflow for automated Docker build, push to AWS ECR, and EC2 deployment  
7. **Deployment**  
   - Flask web app hosted on AWS EC2 for real-time predictions  

---

## 🚀 AWS Deployment Workflow  
1. Push code changes to GitHub  
2. GitHub Actions builds Docker image  
3. Push image to **AWS ECR**  
4. SSH into AWS EC2 instance  
5. Pull and run the latest container  

---

## 📈 Results  
- **Best Model:** Random Forest Regressor  
- **Performance:**  
  - High R² score  
  - Low RMSE indicating accurate predictions  
- **Deployment:** Fully functional Flask application hosted on AWS EC2  
- **MLOps Impact:**  
  - Reproducible experiments via MLflow  
  - Automated cloud deployment via GitHub Actions & Docker  

---

## 🖥️ Web Application  
- **Input:** Chemical attributes of wine  
- **Output:** Predicted wine quality score  
- Hosted on AWS EC2 and accessible via public IP  

---

## 📜 License  
This project is licensed under the **MIT License**.

---
