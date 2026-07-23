# Medical Disease Prediction using Deep Learning

## Overview

This repository contains an end-to-end deep learning project for predicting multiple medical conditions using TensorFlow and Keras. The objective of this project is to implement modern neural network architectures and deep learning workflows while building a scalable disease prediction system.

The project is being developed incrementally as a series:

- **Part 1:** Heart Disease Prediction *(Completed)*
- **Part 2:** Kidney Disease Prediction *(In Progress)*
- **Part 3:** Stroke Prediction *(Planned)*
- **Final Phase:** Full-Stack Medical Disease Prediction Application

Rather than focusing solely on model accuracy, this project emphasizes building production-oriented machine learning pipelines and understanding the engineering principles behind each component.

---

## Repository Structure

```
Medical_Disease_Prediction/
│
├── Dataset/
│   ├── framingham_heart_study.csv
│   ├── healthcare-dataset-stroke-data.csv
│   └── kidney_disease.csv
│
├── Images/
│   └── Hear_Diesease/
│       ├── preprocessing_pipeline.png
│       ├── Build_model.png
│       ├── Build_model_2.png
│       ├── Build_model_3.png
│       ├── Build_model_4.png
│       ├── Hyperband.png
│       ├── Hyberband_search.png
│       ├── Early_Stopping.png
│       ├── best_hp.png
│       ├── loss_acc.png
│       ├── NN_1.png
│       ├── NN_2.png
│       └── df.info().png
│
└── Notebook/
    ├── Medical_Disease_prediction_NN.ipynb
    ├── Medical_Disease_prediction_NN (1).ipynb
    ├── Medical_Disease_prediction_NN (2).ipynb
    └── Medical_Disease_prediction_NN (3).ipynb
```

---

# Project Roadmap

| Module | Status |
|---------|--------|
| Heart Disease Prediction | Completed |
| Kidney Disease Prediction | In Progress |
| Stroke Prediction | Planned |
| Full Stack Deployment | Planned |

---

# Part 1 – Heart Disease Prediction

## Dataset

- **Dataset:** Framingham Heart Study
- **Task:** Binary Classification
- **Framework:** TensorFlow / Keras

---

## Deep Learning Pipeline

The current implementation includes:

- Data cleaning
- Missing value imputation
- Feature scaling
- Train / Validation / Test split
- Scikit-learn preprocessing pipelines
- TensorFlow Normalization layers
- Wide & Deep Neural Network
- Custom model using `tf.keras.Model`
- Hyperparameter tuning using Hyperband
- Early Stopping
- Performance evaluation

---

## Data Preprocessing

The preprocessing pipeline is implemented using Scikit-learn.

### Components

- `SimpleImputer`
- `StandardScaler`
- `ColumnTransformer`
- `Pipeline`

Dataset split:

- Training: **80%**
- Validation: **10%**
- Test: **10%**

---

## Model Architecture

The neural network is implemented by subclassing `tf.keras.Model`.

Architecture includes:

- Input Normalization
- Wide Input Branch
- Deep Dense Network
- Feature Concatenation
- Sigmoid Output Layer

Hidden layers are automatically configured during hyperparameter tuning.

---

## Hyperparameter Tuning

Hyperparameter optimization is performed using **Keras Tuner (Hyperband)**.

### Search Space

| Hyperparameter | Range |
|---------------|------|
| Hidden Layers | 1 – 8 |
| Units | 16 – 256 |
| Activation | ReLU / Tanh |
| Optimizer | Adam / SGD |
| Learning Rate | 1e-4 – 1e-2 |

### Search Configuration

| Parameter | Value |
|-----------|------|
| Algorithm | Hyperband |
| Maximum Epochs | 20 |
| Total Trials | 30 |

### Best Hyperparameters

| Hyperparameter | Value |
|----------------|------|
| Hidden Layers | 8 |
| Units | 144 |
| Activation | tanh |
| Optimizer | Adam |
| Learning Rate | 0.001206 |

---

## Model Performance

### Validation

| Metric | Value |
|--------|------|
| Validation AUC | **0.7333** |

### Test Set

| Metric | Value |
|--------|------|
| Accuracy | **84.67%** |
| AUC | **0.7204** |
| Binary Cross Entropy Loss | **0.3881** |

---

# Technologies Used

- Python
- TensorFlow
- Keras
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Keras Tuner

---

# Future Work

The repository will continue to evolve as additional deep learning concepts are implemented.

Upcoming improvements include:

- Kidney Disease Prediction
- Stroke Prediction
- Feature Engineering
- Learning Rate Scheduling
- Regularization Techniques
- Batch Normalization
- Dropout
- Model Explainability
- Cross Validation
- Model Comparison
- Full-Stack Web Application
- Docker Deployment

---

# Learning Objectives

This project is intended to gain practical experience with:

- Neural Network Architecture Design
- Deep Learning Engineering
- Data Preprocessing Pipelines
- Hyperparameter Optimization
- Model Evaluation
- Experiment Tracking
- End-to-End Machine Learning Workflows

---

# License

This project is intended for educational and research purposes.