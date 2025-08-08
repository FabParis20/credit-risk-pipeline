# credit-risk-pipeline
Mise en œuvre d'un outil de “scoring crédit” pour calculer la probabilité qu’un client rembourse son crédit, puis classification de la demande en crédit accordé ou refusé
## 🎯 Objectif du projet

Ce projet vise à entraîner un modèle de scoring de crédit à partir des données de Home Credit et à mettre en œuvre une démarche MLOps complète incluant :

- Le tracking des expériences avec MLflow
- L’entraînement de plusieurs modèles (RandomForest, XGBoost, LightGBM, etc.)
- La gestion du déséquilibre des classes
- L’optimisation métier via une fonction de coût personnalisée (FN > FP)
- La sélection du meilleur modèle et son enregistrement dans le Model Registry

---

## 🧰 Outils et technologies

- **Python 3.13.3**
- **Poetry** pour la gestion d’environnement
- **pandas**, **scikit-learn**, **xgboost**, **lightgbm**
- **MLflow** pour le tracking, le Model Registry, et la visualisation des runs
- **Jupyter Notebooks** pour l’EDA et la modélisation
- **Git** & **GitHub** pour le versionnement

---

## 📁 Organisation du projet

```bash
.
├── data/                    # Données brutes (non versionnées)
├── notebooks/              # Analyses exploratoires, modélisation
├── src/                    # Code Python modulaire (prétraitement, features, modèles...)
├── models/                 # Modèles entraînés (joblib, pickle)
├── mlruns/                 # Tracking MLflow
├── docs/                   # Documentation, diagrammes, screenshots
├── README.md               # Ce fichier
├── pyproject.toml          # Dépendances gérées avec Poetry
└── .gitignore              # Fichiers à exclure du versionnement

```

## 🗂️ Sources de données
Les fichiers proviennent du dataset Home Credit proposé sur Kaggle.
Les principaux fichiers utilisés sont :

- application_train.csv / application_test.csv
- bureau.csv, bureau_balance.csv
- previous_application.csv, installments_payments.csv
- POS_CASH_balance.csv, credit_card_balance.csv
- HomeCredit_columns_description.csv