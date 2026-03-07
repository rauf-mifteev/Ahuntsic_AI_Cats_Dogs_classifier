# Classification Chats vs Chiens — Travail Pratique sur CNN (Réseaux de neurones convolutifs)

## Aperçu du projet

Ce projet est réalisé dans le cadre du cours de l'Intelligence Artificielle 1 (420‐313‐AH) au Collège Ahuntsic. J'y construis et entraîne des **réseaux de neurones convolutif (CNN)** dans un **Jupyter Notebook** en utilisant **TensorFlow / Keras** pour classifier des photos de chats et de chiens.

En partant d'un modèle de base atteignant 78 % de précision, j'ai réalisé **8 expériences successives** en modifiant différents aspects du modèle :

| # | Modification | Précision test |
|---|---|---|
| Base | Modèle de départ (Conv×3, 2 000 images) | 78,00 % |
| Exp 1 | Plus de données : 4 000 images par classe | 84,00 % |
| Exp 2 | Architecture plus profonde : 4ᵉ couche Conv2D (256 filtres) | 87,25 % |
| Exp 3 | Taux d'apprentissage réduit : 0.001 → 0.0005 | 85,17 % |
| Exp 4 | Dropout réduit : 0.5 → 0.3 | 85,92 % |
| Exp 5 | Augmentation de luminosité ajoutée | 50,00 % |
| Exp 6 | Architecture type VGG (sans normalisation) | 50,00 % |
| Exp 7 | Architecture VGG + Batch Normalization | 91,67 % |
| **Exp 8** | **Transfer Learning — MobileNetV2** | **95,50 %** |

Le meilleur résultat obtenu est **95,50 % de précision** sur le jeu de test, grâce au Transfer Learning.

## Prérequis

Le code est en **Python** dans un **Jupyter Notebook** et utilise :

* [TensorFlow / Keras](https://www.tensorflow.org/)
* [NumPy](https://numpy.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)
* [scikit-learn](https://scikit-learn.org/)
* [Pillow](https://python-pillow.org/)

## Lancer le notebook

### Sur Google Colab

Placez le fichier zip du dataset dans votre Google Drive :

```
MyDrive/AI_class/kagglecatsanddogs_5340.zip
```

Puis ouvrez `cats_vs_dogs_TP.ipynb` dans Colab, activez le GPU via **Exécution → Modifier le type d'exécution → GPU T4**, et exécutez toutes les cellules.


