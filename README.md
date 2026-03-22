# MLP sur Fashion-MNIST

## 📌 Présentation du projet

Ce projet a été réalisé dans le cadre d'un mini-projet de Deep Learning. Il consiste à implémenter, analyser et optimiser un Perceptron Multicouche (MLP) pour la classification d'images Fashion-MNIST.

## 🎯 Objectifs

- Implémenter un MLP **from scratch** pour comprendre les mécanismes internes
- Implémenter une version **concise** avec les API haut niveau de PyTorch
- Étudier l'influence des hyperparamètres (`num_hiddens`, `lr`) sur les performances
- Identifier les phénomènes de sous-apprentissage et de sur-apprentissage
- Assurer la reproductibilité des résultats (seed fixe)

## 📊 Principaux résultats

| Modèle | Meilleure précision test | Configuration |
|--------|-------------------------|---------------|
| From scratch | **85.73%** | h=256, lr=0.1 |
| Concise | **86.34%** | h=256, lr=0.1 |
| Optimal | **87.00%** | h=1024, lr=0.1 |

## 📁 Structure du repository
MLP-FashionMNIST-Project/
├── MLP-DeepLearning-version_final.ipynb # Notebook principal
├── figures/ # Graphiques générés
│ ├── scratch_training_curves.png
│ ├── concise_training_curves.png
│ ├── hidden_impact.png
│ ├── lr_impact.png
│ ├── train_test_curves.png
│ └── gap_evolution.png
└── README.md # Ce fichier


## 🚀 Exécution

### Avec Google Colab (recommandé)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Rayane-Loukhmi/MLP-FashionMNIST-Project/blob/main/MLP-DeepLearning-version_final.ipynb)

1. Cliquer sur le badge ci-dessus
2. Exécuter toutes les cellules (Runtime → Run all)

### En local

```bash
git clone https://github.com/Rayane-Loukhmi/MLP-FashionMNIST-Project.git
cd MLP-FashionMNIST-Project
pip install torch torchvision matplotlib numpy
jupyter notebook MLP-DeepLearning-version_final.ipynb
```

🔧 Dépendances
torch>=2.0.0
torchvision>=0.15.0
matplotlib>=3.5.0
numpy>=1.21.0

🔄 Reproductibilité
Tous les résultats sont reproductibles grâce à une seed fixe :

```python
SEED = 42
torch.manual_seed(SEED)
np.random.seed(SEED)
random.seed(SEED)
```

📈 Graphiques générés

Graphique	                    Description
scratch_training_curves.png	  Évolution loss/accuracy du modèle from scratch
concise_training_curves.png	  Évolution loss/accuracy du modèle concise
hidden_impact.png	            Précision en fonction du nombre de neurones cachés
lr_impact.png	                Précision en fonction du taux d'apprentissage
train_test_curves.png	        Évolution train/test pour h=16, 128, 1024
gap_evolution.png	            Évolution du gap train-test

👨‍💻 Auteur
Rayane LOUKHMI
EMSI - École Marocaine des Sciences de l'Ingénieur
Projet réalisé dans le cadre du cours de Deep Learning

📅 Date
Mars 2026
