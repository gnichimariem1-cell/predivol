## Exécution

1. Ouvrir `PrediVol.ipynb` dans Google Colab (*Fichier › Ouvrir un notebook › GitHub* › `gnichimariem1-cell/predivol`).
2. `pip install -r requirements.txt` (Colab a déjà la plupart des bibliothèques).
3. *Exécution › Tout exécuter*. Les données sont téléchargées automatiquement depuis Kaggle.

## Suivi des expériences (MLflow)

Les 6 modèles (4 modèles et 2 modèles naïfs) sont enregistrés avec MLflow sur DagsHub (section 23 du notebook) : paramètres, métriques (MAE, RMSE, R², capture des gros retards, prédictions à ±15 min) et fichiers produits.

À l'exécution de la section 23, le notebook demande le **jeton DagsHub** (*DagsHub › Settings › Tokens*) dans une case cachée : le jeton n'est jamais écrit dans le code.

Interface MLflow : https://dagshub.com/gnichimariem1-cell/predivol.mlflow

## Exécution

1. Ouvrir `PrediVol_notebook_complet.ipynb` dans Google Colab.
2. `pip install -r requirements.txt` (Colab a déjà la plupart des bibliothèques).
3. *Exécution › Tout exécuter*. Les données sont téléchargées automatiquement depuis Kaggle.

## Suivi des expériences (MLflow)

Les expériences sont enregistrées avec MLflow sur DagsHub (section 23 du notebook).
Interface MLflow : `https://dagshub.com/<utilisateur>/predivol.mlflow`
