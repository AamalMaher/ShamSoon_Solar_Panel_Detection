# 🔆 ShamSoon — Solar Panel Fault Detection (AI Module)

Hi! This is the AI module I developed as part of my graduation project **ShamSoon**.  
The goal of this module is to automatically detect **faults in solar panels** using deep learning.  
The model is integrated into a specific screen inside the mobile app, allowing users to upload or capture images of their solar panels and get instant feedback on their condition.

---

## 🚀 Project Summary

Solar panels are exposed to various environmental and physical factors that may reduce their efficiency over time. Regular inspection is essential but often impractical.

So, I built and trained a deep learning model that can **automatically classify the type of fault** in a solar panel image into one of six categories. This module runs behind the scenes in the ShamSoon mobile app and provides **real-time diagnostics** to the user.

---

## 🧠 Model Details

- **Architecture**: MobileNetV2 (fine-tuned)
- **Framework**: PyTorch
- **Input Size**: 224x224
- **Training Accuracy**: **98%**
- **Loss Function**: CrossEntropyLoss
- **Optimizer**: Adam

---

## 📦 Dataset

- **Source**: Kaggle  
- **Classes** (6 total):
  - `Clean`
  - `Dusty`
  - `Bird Drop`
  - `Electrical Damage`
  - `Physical Damage`
  - `Snowy`

The dataset was preprocessed with resizing, normalization, and data augmentation to improve generalization.

---

## 📱 How It Works in the App

This AI model is connected to the mobile app through a backend API. From the user's point of view:

1. The user opens the **"Panel Diagnosis"** screen.
2. Uploads or captures a solar panel image.
3. The image is sent to the API where the model runs inference.
4. The result (e.g., "Dusty", "Physical Damage") is shown immediately with maintenance suggestions.

---

## 🧪 Results

| Class             | Precision | Recall | F1-score |
|------------------|-----------|--------|----------|
| Clean            | 0.98      | 0.99   | 0.98     |
| Dusty            | 0.97      | 0.97   | 0.97     |
| Bird Drop        | 0.99      | 0.97   | 0.98     |
| Electrical Damage| 0.97      | 0.98   | 0.97     |
| Physical Damage  | 0.98      | 0.97   | 0.98     |
| Snowy            | 0.98      | 0.99   | 0.98     |

**Overall Accuracy**: **98%**

---



