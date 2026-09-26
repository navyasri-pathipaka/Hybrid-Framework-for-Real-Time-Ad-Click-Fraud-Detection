# Adaptive Hybrid Framework for Real-Time Ad Click Fraud Detection

## 📌 Project Overview

The **Adaptive Hybrid Framework for Real-Time Ad Click Fraud Detection** is a machine learning and deep learning-based web application designed to identify fraudulent and legitimate advertisement clicks.

The system analyzes click-related information, user behavior, device details, session activity, and temporal patterns. It combines a **Random Forest machine learning model** with an **LSTM deep learning model** to improve fraud detection.

The hybrid approach helps detect both structured fraud patterns and sequential behavioral patterns that may be missed by a single model.

---

## 🎯 Objectives

- Detect fraudulent ad clicks in real time.
- Analyze user and click behavior.
- Identify suspicious click patterns.
- Combine Machine Learning and Deep Learning predictions.
- Reduce false positives and false negatives.
- Provide fraud probability and risk information.
- Store prediction results for future analysis.
- Support adaptation to changing fraud patterns.

---

## 🧠 Proposed Approach

The framework follows these main stages:

1. Data Collection
2. Data Preprocessing
3. Feature Engineering
4. Random Forest Prediction
5. LSTM Sequential Analysis
6. Hybrid Decision
7. Fraud Classification
8. Result Storage
9. Incremental Learning

### Hybrid Detection

The system uses:

- **Random Forest** → analyzes structured and statistical features.
- **LSTM** → analyzes sequential and temporal user behavior.
- **Hybrid Decision Module** → combines the outputs of both models.

The final output classifies the click as:

- ✅ Legitimate Click
- 🚨 Fraudulent Click

## Commands to Execute
- python -m venv venv
- venv\Scripts\activate
- pip install django pandas numpy scikit-learn tensorflow keras joblib matplotlib seaborn openpyxl
- python manage.py makemigrations
- python manage.py migrate
- python manage.py runserver


## 🏗️ System Architecture

```text
                ┌──────────────────┐
                │   Click Data     │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ Data Preprocessing│
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ Feature Engineering│
                └────────┬─────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
     ┌────────────────┐    ┌────────────────┐
     │ Random Forest  │    │      LSTM      │
     │  ML Model      │    │ Deep Learning  │
     └────────┬───────┘    └───────┬────────┘
              │                    │
              └─────────┬──────────┘
                        ▼
              ┌─────────────────────┐
              │ Hybrid Decision     │
              │      Engine         │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ Fraud / Legitimate  │
              │      Result         │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ SQLite Database     │
              └─────────────────────┘
