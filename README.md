# 🖼️ Image Classification with Custom CNN & Transfer Learning (CIFAR‑10)

## 🎯 Business Problem

Retail, e‑commerce, and logistics companies rely heavily on accurate product image classification.
Manual sorting is slow, error‑prone, and difficult to scale as catalogs grow.

How can we automate image classification with a reliable, efficient, and scalable deep learning pipeline?

## 💡 Proposed Solution

This project develops a full **end‑to‑end Computer Vision pipeline** using CIFAR‑10 to benchmark two approaches:

- A **custom Convolutional Neural Network (CNN)** optimized through systematic ablation 
- **Transfer Learning with VGG19**, fine‑tuned on the dataset  

### Key steps:

- Data preprocessing and augmentation  
- Architecture search through ablation (depth, filters, activation, regularization)   
- Final training with **Dropout, Weight Decay, EarlyStopping, ReduceLROnPlateau, Mixed Precision**  
- Transfer Learning benchmark with **VGG19** (frozen + fine‑tuned)  
- Model evaluation using accuracy curves, confusion matrix, and misclassified samples

### Final Results

- **Custom CNN (optimized): ~87% accuracy**  
- **VGG19 fine‑tuned: ~75% accuracy**  

## 🛠️ Technologies

Python • TensorFlow/Keras • CNN • Transfer Learning • VGG19 • Mixed Precision • Data Augmentation • Pandas • Matplotlib • Seaborn

## 🚀 Business Impact

- **Reduced operational workloa**d through automated image classification  
- **Lower error rates** compared to manual sorting  
- **Scalable pipeline** adaptable to new product categories or larger datasets  
- Strong foundation for deployment (API, batch scoring, or real‑time inference)

## 📊 Model Results

### Custom CNN — Training Curves

<img width="547" height="435" alt="curves " src="https://github.com/user-attachments/assets/09766bc6-37f9-495f-bdf2-2d38f0af23c3" />
<img width="547" height="435" alt="curves_acc" src="https://github.com/user-attachments/assets/2ebc429d-81c8-46b1-b9b3-c733ff826499" />

### VGG19 — Fine‑Tuning Curves

<img width="547" height="435" alt="loss_vgg" src="https://github.com/user-attachments/assets/25634226-f12e-48b0-bde2-363220678a50" />
<img width="547" height="435" alt="acc_vgg" src="https://github.com/user-attachments/assets/d1aee6ca-b75c-4467-8514-31801959320b" />

### Confusion Matrix

<img width="736" height="699" alt="cm" src="https://github.com/user-attachments/assets/51356f06-2e38-4f2c-a003-0eea32d31777" />

### Misclassified Samples

<img width="794" height="311" alt="miss" src="https://github.com/user-attachments/assets/5fade5e0-d783-4218-b561-87402c426a0a" />

## 🧠 Key Learnings

- Ablation studies are essential to identify the optimal architecture  
- Transfer Learning is powerful but not always superior to a well‑designed custom model  
- Regularization (Dropout, Weight Decay) and callbacks significantly improve generalization  
- Mixed precision accelerates training without sacrificing accuracy
