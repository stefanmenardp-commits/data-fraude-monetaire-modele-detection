# Fraude monétaire - Détection de faux billet - Machine Learning

Ce projet consiste à développer un modèle de machine learning capable de prédire si un billet est authentique ou contrefait à partir de plusieurs caractéristiques physiques (dimension).

## Table des matières

- [Présentation du projet](#aperçu-projet)
- [Problématique](#problématique)
- [Objectifs](#objectifs)
- [Source de donnée](#source-de-donnée)
- [Méthodologie](#méthodologie)
- [Stack technique](#stack-technique)
- [Compétences développées](#compétences-développées)

## Présentation du projet

Ce projet a vu le jour lors d'un projet de la formation de Data Analyst d'Open Classrooms. Le sujet était donné, avec un cas de fraude monétaire à détecter. L'objectif est de comparer plusieurs modèles statistiques et algorithmiques afin de sélectionner la meilleure solution de classification pour éviter la fraude.

---

## Problématique

Comment identifier automatiquement un billet authentique ou contrefait à partir de ses caractéristiques dimensionnelles et physiques ?

---

## Objectifs

- comprendre la structure du jeu de données
- nettoyer le jeu de données
- enrichir le jeu de données avec l'imputation de certaines données à l'aide de méthodes statistiques
- entraîner plusieurs modèles de classification pour la détection de faux
- comparer leurs performances
- sélectionner le modèle le plus performant

---

## Source de données

Le jeu de données contient plusieurs caractéristiques associées à des billets :

- variables numériques en millimètre liées aux dimensions physiques (Longueur, Diagonale, Hauteur gauche, Hauteur droite, Marge supérieure, Marge inférieure)
- variable cible booléenne indiquant si le billet est authentique ou contrefait (True = Billet authentique, False = Billet contrefait)

---

## Méthodologie

### 1. Analyse des données

Pour mieux comprendre vers laquelle direction se diriger et avant de faire quoi que ce soit comme action, il était essentiel d'effectuer plusieurs étapes d'analyse :

- analyse des types de données
- analyse descriptive des variables
- vérification de la distribution des classes
- identification des valeurs absurdes
- détection des valeurs aberrantes
- Recherche des doublons
- Analyse des valeurs manquantes

### 2. Nettoyage des données

Lorsque l'analyse était terminée, les étapes de nettoyage pouvaient commencer pour uniformiser l'état du jeu de données :

- conversion des types de données
- suppression ou correction des valeurs incohérentes (valeurs absurdes)
- traitement des doublons
- traitement des valeurs manquantes
- identification des valeurs aberrantes et exclusion
- préparation des variables pour la modélisation

### 3. Imputation des valeurs manquantes


Mise en place d'une méthode d'imputation utilisant des méthodes statistiques pour l'enrichissement du jeu de données concernant les valeurs manquantes. Plusieurs méthodes statistiques peuvent être utilisées pour compléter les données manquantes :

- Régression linéaire simple
- Régression linéaire multiple
- Imputation selon des statistiques descriptives

La régression linéaire multiple était celle qui était adéquate avec ces données. Le besoin était de prédire une variable en utilisant plusieurs variables.

### 4. Modélisation

Plusieurs modèles sont comparés à la suite du nettoyage du jeu de données, pour sélectionner celui qui sera le plus performant pour la détection de fraude monétaire : 

- Régression logistique
- K-Means
- Random Forest (Bagging)
- XGBoost (Boosting)
- Combinaison des modèles Random Forest et XGBoost (Stacking)

Un déroulement commun se reproduit pour chaque entrainement des modèles, il se présente en 6 grandes parties : 

1. La préparation de données (variable cible et variable explicative)
2. Division du jeu de données en deux segments (80/20, données d'entrainements et de tests)
3. Choix de normaliser les données ou garder la donnée brute pour l'entrainement et les tests (la raison étant une différence potentielle et significative d'unité ou d'échelle entre les variables)
4. Entrainement du modèle (80 % des données allouées)
5. Evaluation de la prédiction du modèle après entrainement (sur les 20 % de données allouées pour les tests)
6. Interprétation des résultats, avec différentes métriques

### 5. Évaluation et résultat

Les performances des différents modèles sont comparées afin de sélectionner le meilleur modèle selon la capacité de prédiction, la précision des résultats, la robustesse et l'équilibre entre faux positifs et faux négatifs. Plusieurs métriques permettent d'évaluer ces différents critères, ils peuvent être différents selon les modèles, voici une liste de celles utilisées :

- Accuracy
- Precision
- Recall
- F1-score
- F-Beta-Score - Validation croisée
- Matrice de confusion
- Courbe ROC
- AUC

---

## Stack technique

| **Domaines** | **Technologies** |
|---|---|
| **Outil de développement** | `Jupyter Notebook` |
| **Langage** | `Python` |
| **Manipulation des données** | `Pandas`, `NumPy` |
| **Visualisation** | `Matplotlib`, `Seaborn` |
| **Machine learning** | `Scikit-learn` |
| **Modèles statistiques** | `Régression linéaire`, `Régression logistique`, `Random Forest`, `XGBoost`, `K-Means`, `Stacking` |
| **Évaluation** | `Accuracy`, `Precision`, `Recall`, `F1-score`, `F-Beta-Score - Validation croisée`, `Matrice de confusion`, `Courbe ROC`, `AUC` |
| **Documentation** | `Markdown` |

---

## Compétences développées

Ce projet m'a permis de développer et de mettre en œuvre mes compétences dans les domaines suivants.

- nettoyage des données
- enrichissement des données par modèle statistique
- préparation des données pour un modèle
- entraînement et comparaison de modèles
- évaluation des performances d’un modèle
- interprétation des résultats
