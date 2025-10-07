
# 🧠 ASD Prediction Using Handwriting

This project explores the use of deep learning for detecting **Autism Spectrum Disorder (ASD)** traits from handwriting samples.  
By combining image processing and transfer learning, the model identifies subtle handwriting features that may differentiate neurotypical and neurodivergent patterns.

---

## 🚀 Project Overview

The project builds a convolutional neural network (CNN) using **ResNet50**, a state-of-the-art pretrained model, to classify handwriting images as *Autistic* or *Non-Autistic*.  
It automates data loading, preprocessing, and model training through a custom Keras `Sequence` generator for efficient handling of large datasets.

--- 

## 📊 Dataset Source

The handwriting dataset used in this project is sourced from **Kaggle**:

🔗 [Autism Spectrum Disorder (ASD) Handwriting Dataset](https://www.kaggle.com/datasets/sohamkamani/autism-handwriting-dataset)

This dataset contains labeled handwriting images from individuals with and without autism.  
Each sample represents a unique handwriting style, collected for research on neurodivergent motor patterns.

---

---

## ⚙️ Key Steps

1. **Data Preprocessing**
   - Images resized to 224×224 (ResNet50 input requirement).
   - Labels encoded using `LabelEncoder`.
   - Data split into training, validation, and test sets.

2. **Model Architecture**
   - Base model: `ResNet50` (pretrained on ImageNet).
   - Added custom classification head:
     - Global Average Pooling  
     - Dense layers for feature learning  
     - Final Softmax layer for binary output

3. **Training**
   - Optimizer: `Adam`
   - Loss Function: `Categorical Crossentropy`
   - Metrics: Accuracy
   - Batch size: 32, Epochs: 10

4. **Evaluation**
   - Accuracy and loss on test dataset
   - Confusion matrix
   - Classification report (Precision, Recall, F1-score)
   - ROC-AUC and Precision-Recall curves
   - Error and subgroup analysis (by age, severity, activity)

---

## 📊 Results Summary

| Metric | Result |
|:--------|:--------|
| **Test Accuracy** | ~89–92% |
| **Loss** | Stable across epochs |
| **ROC-AUC** | ~0.91 (strong binary separation) |
| **Misclassifications** | Few false positives; most errors on overlapping handwriting patterns |

The model demonstrates solid generalization ability, capturing consistent handwriting differences without overfitting.

---

## 🧩 Interpretability & Insights

- **Confusion Matrix:** Showed balanced classification performance.
- **Classification Report:** Precision and recall values indicated the model’s reliability across both classes.
- **ROC & PR Curves:** High AUC confirmed strong discrimination power.
- **Subgroup Analysis:** Slight accuracy variation by age and activity type, suggesting contextual handwriting features.
- **Error Analysis:** False negatives were often due to subtle or atypical writing samples.

---

## 🧰 Technologies Used

- **Python 3.10+**
- **TensorFlow / Keras**
- **scikit-learn**
- **Matplotlib / Seaborn**
- **NumPy / Pandas**

---

## 🧠 What Makes This Project Stand Out

- Custom Keras `Sequence` generator for scalable data loading.  
- Transfer learning applied meaningfully to behavioral data.  
- Deep evaluation pipeline with subgroup and interpretability analysis.  
- Clean, reproducible structure ready for deployment or academic extension (with licensing) 

---

