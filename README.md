# ML_Model_Flask_Deployment

# Prédiction d'Octroi de Crédit Bancaire

Projet de Machine Learning visant à prédire si un client de banque va souscrire à un crédit ou non, à partir de ses caractéristiques. Le projet couvre l'ensemble du pipeline : nettoyage des données, exploration, sélection de features, modélisation et déploiement web.

## Description du projet

Ce projet a été réalisé en deux parties :

1. **Analyse et modélisation (Google Colab)** — préparation des données et entraînement de plusieurs modèles de classification
2. **Déploiement (VS Code / Flask)** — mise en place d'une application web permettant de tester le modèle en conditions réelles

## Jeu de données

- Source : [Kaggle]([https://www.kaggle.com/](https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset)) — dataset bancaire
- Objectif : prédire si un client va prendre un crédit (variable cible binaire : Oui/Non)

## Étapes du projet

### 1. Récupération des données
Téléchargement du dataset bancaire depuis Kaggle.

### 2. Nettoyage des données (Data Cleaning)
- Traitement des valeurs manquantes
- Correction des types de données
- Suppression des doublons et valeurs aberrantes

### 3. Analyse exploratoire des données (EDA)
- Visualisation des distributions
- Analyse des corrélations entre variables
- Étude de la relation entre les features et la variable cible

### 4. Sélection de features (Feature Selection)
Identification des variables les plus pertinentes pour la prédiction, afin d'améliorer la performance et réduire la complexité des modèles.

### 5. Modélisation
Trois modèles de classification ont été entraînés et comparés :

| Modèle | Description |
|---|---|
| **Logistic Regression** | Modèle de base, interprétable, bon point de référence |
| **K-Nearest Neighbors (KNN)** | Modèle basé sur la proximité entre observations |
| **Decision Tree** | Modèle basé sur des règles de décision, facilement interprétable |

Les modèles ont été évalués et comparés pour retenir le plus performant.

### 6. Déploiement
Le modèle final a été déployé sous forme d'application web avec **Flask**, permettant à un utilisateur de saisir les informations d'un client et d'obtenir une prédiction (crédit accordé ou non).

## Technologies utilisées

- **Python**
- **Pandas / NumPy** — manipulation des données
- **Matplotlib / Seaborn** — visualisation
- **Scikit-learn** — modélisation (Logistic Regression, KNN, Decision Tree)
- **Flask** — déploiement web
- **Google Colab** — environnement d'entraînement
- **VS Code** — environnement de déploiement

## Installation et utilisation

### Prérequis
```bash
pip install -r requirements.txt
```

### Lancer l'application
```bash
python app.py
```

L'application sera accessible sur `http://127.0.0.1:5000/`

## Structure du projet

```
├── notebook/
│   └── credit_prediction.ipynb    # Analyse et modélisation (Colab)
├── model/
│   └── model.pkl                   # Modèle entraîné sauvegardé
├── app.py                          # Application Flask
├── templates/
│   └── index.html                  # Interface utilisateur
├── requirements.txt
└── README.md
```

## Résultats

Après comparaison des trois modèles, la régression logistique a donné les meilleurs résultats et a été retenue pour le déploiement avec accuracy: 	0.8536

## Auteur

Hiba — Étudiante Ingénieure, ENET'Com Sfax
