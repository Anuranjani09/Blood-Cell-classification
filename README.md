
# 🧬 Decoding Cellular Complexity: Blood Cell Image Classification with Deep Learning

## 🔍 Overview
This project introduces an advanced deep learning framework for classifying blood cells from peripheral smear images. Using a curated and expert-annotated dataset, we explore and compare multiple state-of-the-art architectures to enhance diagnostic accuracy and efficiency.

---

## 🚀 Key Features

### 📊 Dataset
- 17,092 high-resolution images from the Hospital Clinic of Barcelona
- Annotated by clinical pathologists to ensure label quality
- Balanced representation of 8 blood cell classes

### 🧠 Deep Learning Models
- Includes CNN, U-Net, ResNet50, DenseNet-201, VGG-16, MobileNet-V2, InceptionV3, Xception
- A hybrid model combining **InceptionV3 and Xception** achieved state-of-the-art performance

### ⚙️ Performance Enhancements
- SMOTE used for class imbalance handling
- Data augmentation and image resizing for training efficiency
- Supervised Contrastive Learning for robust representation learning

### 🧪 Robust Evaluation Pipeline
- Stratified train-test split (70-30) with 20% validation
- Performance tracked using accuracy, precision, recall, F1-score, and confusion matrix
- Comparison with and without dataset shuffling to assess generalization

---

## 🔧 Methodology

1. **📁 Data Preprocessing**
   - Resized all images to 224×224 pixels (later to 128×128 when using SMOTE)
   - Converted to NumPy arrays, stratified sampling for balanced splits

2. **📌 Model Selection & Training**
   - Implemented and tuned multiple architectures (transfer learning + custom layers)
   - Used optimizers like Adam, SGD, and RMSProp based on model behavior
   - Trained using 10–30 epochs and batch sizes of 32, depending on complexity

3. **📉 Evaluation**
   - 5-fold cross-validation on CNN to reduce variance
   - Supervised contrastive learning to improve class separability
   - Evaluated using standard classification metrics + confusion matrices

---

## 📊 Results

Top performing models based on test accuracy:
- **Hybrid Model (InceptionV3 + Xception)** – **98.51%**
- **Xception** – **97.89%**
- **Supervised Contrastive Learning** – **96.35%**

---

## ✅ Conclusion

This project presents a **scalable, high-accuracy system for automated blood cell classification**, significantly improving the speed and reliability of blood smear analysis. The hybrid deep learning model outperformed individual architectures, demonstrating the value of ensemble techniques and supervised contrastive learning in medical imaging.

---

## 🔭 Future Work

- **Explore new deep learning and hybrid architectures** to further enhance classification performance.
- **Broaden the study using varied and multi-source datasets** to improve model generalization.
- **Embed the system into real-time diagnostic platforms** to support clinical decision-making and deployment.
