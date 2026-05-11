

# CyberJack IDS — Advanced IoT Cyberattack Detection System

An end-to-end Machine Learning pipeline for detecting cyberattacks in IoT network traffic using scalable data engineering, robust validation, explainable AI techniques, and deployment-ready architecture.

---

# Overview

CyberJack IDS is a research-oriented Intrusion Detection System (IDS) designed for IoT cybersecurity environments.
The project focuses on:

* High-performance attack detection
* Scalable large-dataset processing
* Research-grade validation
* Model robustness analysis
* Deployment readiness
* Explainability and reproducibility

The system was developed using the BOT-IoT dataset and combines advanced preprocessing pipelines with machine learning and optional deep learning components.

---

# Key Features

## End-to-End ML Pipeline

* Raw CSV ingestion
* Automated preprocessing
* Feature engineering
* Training & evaluation
* Model validation
* Artifact exporting
* Deployment interface

---

## Large-Scale Data Processing

* Memory-efficient CSV loading
* Parquet optimization
* Chunked processing
* Scalable architecture for large IoT datasets

---

## Advanced Validation Framework

Includes:

* Train / Validation / Test evaluation
* Stratified Cross-Validation
* Overfitting & underfitting detection
* Calibration analysis
* Noise robustness testing
* Feature importance stability
* Permutation testing
* Concept drift analysis

---

## Explainability & Interpretability

* Feature importance analysis
* Calibration curves
* Statistical validation reports
* Drift detection metrics

---

## Deployment Ready

* Saved model artifacts
* Serialized preprocessing pipeline
* Metadata export
* Interactive Gradio interface

Built using:

* XGBoost
* PyTorch
* Gradio

---

# Project Architecture

```text
Raw CSV Files
      ↓
Data Discovery & Validation
      ↓
CSV → Parquet Conversion
      ↓
EDA & Statistical Analysis
      ↓
Feature Engineering
      ↓
Train / Validation / Test Split
      ↓
Scaling & Leakage Prevention
      ↓
Model Training (XGBoost)
      ↓
Validation & Robustness Testing
      ↓
Artifact Exporting
      ↓
Deployment Interface (Gradio)
```

---

# Technologies Used

## Core Stack

* Python 3.x
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* PyTorch
* Joblib
* Matplotlib
* Seaborn
* Gradio

---

# Dataset

Dataset used:

* BOT-IoT

The dataset contains IoT network traffic with both normal and malicious activity.

Attack categories may include:

* DDoS
* DoS
* Reconnaissance
* Keylogging
* Data Exfiltration
* Botnet behavior

---

# Model Validation Results

## Final Evaluation Metrics

| Dataset    | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ---------- | -------- | --------- | ------ | -------- | ------- |
| Train      | 1.0000   | 1.0000    | 1.0000 | 1.0000   | 1.0000  |
| Validation | 0.9989   | 0.9991    | 0.9987 | 0.9989   | 0.9999  |
| Test       | 0.9992   | 0.9992    | 0.9992 | 0.9992   | 0.9999  |

---

## Cross-Validation

```text
Mean CV Accuracy: 0.9990
CV Std: ±0.0005
```

---

## Noise Robustness

The model was evaluated against noisy inputs to test resilience against perturbations.

| Noise Std | Accuracy |
| --------- | -------- |
| 0.00      | 0.9992   |
| 0.01      | 0.9905   |
| 0.05      | 0.9864   |
| 0.10      | 0.9765   |
| 0.20      | 0.9405   |

---

## Calibration

```text
Brier Score: 0.0006
```

The model demonstrates excellent probability calibration and prediction confidence consistency.

---

# Important Research Note

Although the model achieves extremely high accuracy, feature dominance analysis revealed that a small subset of features contributes heavily to predictions.

This project therefore includes:

* Feature importance stability analysis
* Leakage prevention mechanisms
* Concept drift detection
* Robustness testing

Future work focuses on:

* Cross-dataset generalization
* SHAP explainability
* Adversarial robustness
* Temporal modeling
* Ensemble IDS architectures

---

# Folder Structure

```text
CyberJack-IDS/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── parquet/
│
├── models/
│   ├── xgboost_model.pkl
│   ├── scaler.pkl
│   └── metadata.json
│
├── reports/
│   ├── model_validation_report.json
│   ├── learning_curves.png
│   ├── calibration_curve.png
│   └── noise_robustness.png
│
├── notebooks/
│   └── cyberjack_model.ipynb
│
├── app/
│   └── gradio_app.py
│
├── requirements.txt
└── README.md
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/cyberjack-ids.git
cd cyberjack-ids
```

---

## Create Environment

```bash
python -m venv venv
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Run Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/cyberjack_model.ipynb
```

---

## Run Gradio Interface

```bash
python app/gradio_app.py
```

---

# Example Outputs

The project automatically generates:

* Validation reports
* Learning curves
* Calibration curves
* Noise robustness plots
* Feature importance analysis
* Saved trained models
* JSON experiment summaries

---

# Research Contributions

This project explores:

* IoT cybersecurity using ML
* Robust IDS validation methodologies
* Drift-aware cyber models
* Scalable network traffic processing
* Real-world deployment considerations

---

# Future Improvements

## Planned Features

* SHAP explainability
* Real-time packet streaming
* Transformer/LSTM architectures
* Ensemble IDS systems
* Federated learning
* Online learning adaptation
* Adversarial attack defense
* Docker deployment
* REST API integration

---

# Disclaimer

This project is intended for:

* Academic research
* Educational purposes
* Cybersecurity experimentation

It should not be considered a production-certified security system without additional testing and hardening.

---

# Author

Developed by Jakup Ymeraj

Focused on:

* Machine Learning
* Data Engineering
* IoT Security
* AI-based Cyber Defense

---

# License

MIT License

Feel free to use, modify, and contribute.
