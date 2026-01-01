# ♻️ Waste Image Classification with CNN & XGBoost

## 📌 Project Overview
This project focuses on a **multi-class waste image classification** problem aimed at automatically identifying different types of waste from images. The objective is to support efficient and scalable waste management and recycling systems by reducing manual sorting errors. The classification task covers five categories: **glass, plastic, paper, metal, and biological/domestic waste**.

The project investigates both **deep learning** and **hybrid modeling** strategies by combining Convolutional Neural Networks (CNNs) with classical machine learning methods.

---

## 🧠 Problem Definition
- **Input:** Waste images  
- **Output:** Waste class label (Glass, Plastic, Paper, Metal, Biological)  
- **Learning Type:** Supervised learning  
- **Task:** Multi-class classification  

Each image belongs to exactly one class.

---

## 📂 Dataset
- ~**2,600 labeled images**
- Balanced class distribution
- Organized in **class-based directories**
- Compiled from publicly available waste classification datasets

---

## 🔄 Data Preprocessing & Augmentation
To improve robustness and generalization:
- Image resizing to a fixed input size
- Pixel normalization (per-channel mean & standard deviation)
- **Training-only augmentation**:
  - Random horizontal flip
  - Random rotation

**Data split:**
- Training: 70%
- Validation: 15%
- Test: 15%

---

## 🧩 Model Architectures

### 1️⃣ CNN-Based Classification
A custom **CNN** was trained end-to-end:
- Automatic learning of spatial features (edges, textures, shapes)
- **Adam optimizer** with **Cross-Entropy Loss**
- Hyperparameters (learning rate, batch size, epochs) tuned

---

### 2️⃣ Transfer Learning (ResNet-18)
To improve performance on limited data:
- **Pre-trained ResNet-18** used
- Convolutional layers frozen as a **feature extractor**
- Task-specific layers fine-tuned
- Reduced training time and overfitting

---

### 3️⃣ CNN Feature Extraction + XGBoost (Hybrid Model)
- CNN convolutional layers used **only for feature extraction**
- Feature maps flattened into high-dimensional vectors
- **XGBoost** used as the final classifier

**Why XGBoost?**
- Strong tree-based decision boundaries
- Built-in regularization (L1/L2)
- Efficient and scalable
- Robust on small-to-medium datasets

This hybrid approach combines **CNN representation power** with **gradient boosting decision strength**.

---

## ⚙️ Hyperparameter Optimization
- **Random Search** employed
- Tuned parameters:
  - Learning rate
  - Batch size
  - Number of epochs
- Best configuration selected based on validation performance

---

## 🔬 Key Concepts Covered
- Image-based multi-class classification  
- CNN architecture design  
- Transfer learning (ResNet-18)  
- Feature extraction vs end-to-end learning  
- Hybrid CNN + XGBoost modeling  
- Data preprocessing and augmentation  
- Hyperparameter optimization  

---

## 🚀 Applications
- Automated waste sorting
- Smart recycling systems
- Environmental sustainability solutions
- Computer vision classification pipelines



*Introduction to Machine Learning – Final Project (December 2025)*
