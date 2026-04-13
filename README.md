# Image Classification with Custom CNN & Transfer Learning (CIFAR-10)

## Business Problem

Retail, e-commerce, and logistics companies rely on accurate product image classification.
Manual sorting is slow, error-prone, and difficult to scale as catalogs grow.

How can we automate image classification with a reliable, efficient, and scalable deep learning pipeline?

## Proposed Solution

End-to-end Computer Vision pipeline using CIFAR-10 to benchmark two approaches:

- A **custom CNN** optimized through systematic ablation studies
- **Transfer Learning with VGG19**, fine-tuned on the dataset

**Key steps:**

- Data preprocessing and augmentation
- Architecture search via ablation (depth, filters, activation, regularization)
- Final training with Dropout, Weight Decay, EarlyStopping, ReduceLROnPlateau, Mixed Precision
- VGG19 benchmark (frozen → fine-tuned)
- Evaluation: accuracy curves, confusion matrix, misclassified samples

## Results

| Model | Accuracy | Notes |
|-------|----------|-------|
| Custom CNN (optimized) | **~87%** | Ablation-tuned architecture |
| VGG19 fine-tuned | ~75% | Transfer learning benchmark |

**Key insight:** a well-optimized custom CNN outperforms VGG19 fine-tuning on CIFAR-10 — demonstrating that transfer learning is not always the best solution, and that systematic ablation pays off.

## Technologies

Python · TensorFlow/Keras · CNN · VGG19 · Transfer Learning · Mixed Precision · Data Augmentation · Matplotlib · Seaborn

## Business Impact

- Reduced operational workload through automated image classification
- Lower error rates compared to manual sorting
- Scalable pipeline adaptable to new product categories or larger datasets
- Strong foundation for deployment (API, batch scoring, real-time inference)

## Model Results

### Custom CNN — Training Curves

<img width="547" height="435" alt="curves_loss" src="assets/cnn_loss.png" />
<img width="547" height="435" alt="curves_acc" src="assets/cnn_acc.png" />

### VGG19 — Fine-Tuning Curves

<img width="547" height="435" alt="loss_vgg" src="assets/vgg_loss.png" />
<img width="547" height="435" alt="acc_vgg" src="assets/vgg_acc.png" />

### Confusion Matrix

<img width="736" height="699" alt="cm" src="assets/cnn_confusion_matrix.png" />

### Misclassified Samples

<img width="794" height="311" alt="miss" src="assets/cnn_missclassified.png" />
