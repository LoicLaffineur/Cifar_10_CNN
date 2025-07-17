# 🧠 Classification d'images – Projet CIFAR-10

## 🎯 Objectif
Construire un modèle de classification d’images performant sur le jeu de données CIFAR-10 (10 classes) en utilisant un **réseau de neurones convolutif (CNN)** et des techniques de **Transfer Learning**.

---

## 📚 Données
- **Source** : [CIFAR-10 – TensorFlow Dataset](https://www.tensorflow.org/datasets/catalog/cifar10?hl=fr)
- **Taille** : 60 000 images couleur 32x32 (50 000 entraînement / 10 000 test)
- **Classes** : avion, automobile, oiseau, chat, cerf, chien, grenouille, cheval, bateau, camion

---

## ⚙️ Méthodologie

### 🔧 Prétraitement :
- Normalisation des pixels
- Encodage one-hot des labels
- Augmentation de données (rotation, zoom, flip)

### 🏗️ Modèles testés :
1. **CNN from scratch** (TensorFlow / Keras) :
   - 3 blocs convolutifs avec MaxPooling, BatchNormalization et Dropout
   - Activation ReLU + Softmax
   - Optimiseur : Adam
2. **Transfer Learning** :
   - Modèle pré-entraîné **ResNet152** (ImageNet)
   - Fine-tuning sur les dernières couches
   - Ajout de couche Dense + Dropout

---

## 📊 Résultats

| Modèle                | Accuracy (Test) 
|----------------------|----------------
| CNN personnalisé      | ~86 %          
| Transfer Learning (ResNet152) | ~54%      

- Matrice de confusion incluse
- Interprétation des erreurs fréquentes (ex. chat vs chien)

  ## 🧠 Pistes d’amélioration
- Ajouter des visualisations sur les plus grosses erreurs de predictions
- Ajouter des l'interprétation sur les résultats
- Revoir le transfer learning parce que les résultats sont vraiment pas a la hauteur
