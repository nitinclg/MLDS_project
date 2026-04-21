# MLDS_project
This project predicts loan default risk using deep learning autoencoder models. It compares AE+NN, VAE, and Hybrid AE on financial data after preprocessing and scaling. Hybrid AE gives best overall performance, while imbalance handling improves recall for detecting high-risk borrowers.


## 📊 Overview

The project compares different deep learning models:

- Autoencoder + Neural Network (AE + NN)
- Variational Autoencoder + Neural Network (VAE + NN)
- Hybrid Autoencoder (Reconstruction + Classification)
- Imbalance-aware model with threshold optimization

---

## 🎯 Objective

- Learn meaningful feature representations using autoencoders
- Predict loan default probability
- Compare multiple deep learning approaches
- Handle class imbalance effectively

---

## 🗂 Dataset

- Source: Home Credit Default Risk dataset
- Type: Structured tabular data
- Rows used: 30,000
- Features include:
  - Income
  - Loan details
  - Employment information
  - Demographic attributes

---

## ⚙️ Data Preprocessing

- Removed columns with high missing values (>40%)
- Filled missing values using median
- Encoded categorical variables using Label Encoding
- Scaled features using StandardScaler
- Split data into training and testing sets

---

## 🧠 Models Implemented

### 1. Autoencoder + Neural Network (AE + NN)
- Learns compressed feature representation
- Uses encoder output for classification

---

### 2. Variational Autoencoder (VAE + NN)
- Learns probabilistic latent representation
- Uses KL divergence for regularization

---

### 3. Hybrid Autoencoder ⭐
- Combines reconstruction and classification
- Jointly optimizes both objectives
- Achieves best overall performance

---

### 4. Imbalance-Aware Model
- Uses class weighting
- Applies threshold optimization
- Improves recall and F1-score

---

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

---

## 📊 Results

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|------|--------|--------|--------|------|------|
| AE + NN | Moderate | Low | Low | Low | Low |
| VAE + NN | High Accuracy | Low Recall | Low | Moderate | Moderate |
| Hybrid AE | ⭐ Best Overall | Moderate | Moderate | Good | Highest |
| Imbalance Model | Lower Accuracy | Moderate | Highest | Best Recall | Moderate |

---

## 📉 Visualization

- ROC-AUC comparison bar chart
- Performance comparison table

---

## 🏗 System Architecture

Input Data → Preprocessing → Autoencoder → Latent Features → Classifier → Prediction → Evaluation
