# PrédiVol – Prédire et expliquer les retards de vols

Projet du cours d'intelligence artificielle – Collège La Cité – Groupe 7
Mohamed Ridha Benmansour et Mariem Gnichi

## Objectif

Prédire, **avant le départ**, le retard d'un vol à l'arrivée (en minutes) et identifier les principaux facteurs de retard.
Client fictif : Air Numidia (Alger et Tunis), qui ouvre des lignes vers le Canada.

- Type de tâche : régression (cible `Arr_Delay`, en minutes)
- Données : vols intérieurs américains 2023 (Bureau of Transportation Statistics, via Kaggle) et météo quotidienne par aéroport

## Contenu du dépôt

| Fichier | Rôle |
| --- | --- |
| `PrediVol.ipynb` | Tout le projet : données (partie 1), modélisation (partie 2), suivi MLflow (section 23) |
| `requirements.txt` | Bibliothèques Python nécessaires |
| `.gitignore` | Exclut les données, l'environnement virtuel et les fichiers produits |

## Résultats actuels (jeu de validation)

| Modèle | MAE (min) | RMSE (min) | Gros retards captés |
| --- | --- | --- | --- |
| **Forêt aléatoire (modèle de base)** | **24,36** | **53,50** | **32,5 %** |
| Gradient boosting | 24,47 | 53,61 | 32,4 % |
| Ridge | 24,91 | 54,11 | 29,1 % |
| XGBoost | 25,10 | 54,05 | 32,3 % |
| Naïf – moyenne de la route | 25,70 | 55,27 | 15,8 % |

## Exécution

1. Ouvrir `PrediVol.ipynb` dans Google Colab (*Fichier › Ouvrir un notebook › GitHub* › `gnichimariem1-cell/predivol`).
2. `pip install -r requirements.txt` (Colab a déjà la plupart des bibliothèques).
3. *Exécution › Tout exécuter*. Les données sont téléchargées automatiquement depuis Kaggle.

## Suivi des expériences (MLflow)

Les 6 modèles (4 modèles et 2 modèles naïfs) sont enregistrés avec MLflow sur DagsHub (section 23 du notebook) : paramètres, métriques (MAE, RMSE, R², capture des gros retards, prédictions à ±15 min) et fichiers produits.

À l'exécution de la section 23, le notebook demande le **jeton DagsHub** (*DagsHub › Settings › Tokens*) dans une case cachée : le jeton n'est jamais écrit dans le code.

Interface MLflow : https://dagshub.com/gnichimariem1-cell/predivol.mlflow