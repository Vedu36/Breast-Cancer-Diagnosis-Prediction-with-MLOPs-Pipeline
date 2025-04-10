# 🧠 Agentic MLOps Pipeline for Breast Cancer Classification

An autonomous MLOps pipeline engineered to classify breast cancer using Support Vector Machines (SVM). This system integrates **LangGraph** for workflow orchestration and **Groq's LLaMA-3 LLM** for intelligent decision-making—enabling drift detection, model retraining, hyperparameter tuning, and deployment with zero manual intervention.

---

## 🚀 Features

- **Agentic Workflow Orchestration** using LangGraph
- **LLM-Guided Retraining Decisions** with Groq (LLaMA-3)
- **Model Drift Monitoring** with accuracy thresholding
- **Automated Retraining & Deployment**
- **Hyperparameter Tuning** using Optuna
- **Pickle-based Model & Scaler Storage** using Joblib

---

## 🏗️ Project Architecture

```mermaid
graph TD
    A[Start: Monitor Accuracy] --> B{Accuracy < Threshold?}
    B -- No --> F[Done]
    B -- Yes --> C[Query Groq LLM]
    C -- Yes --> D[Retrain Model]
    D --> E[Deploy Model]
    E --> F[Done]
