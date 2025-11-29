# 🚀 SpaceX Falcon 9 Landing Prediction

Ce projet vise à prédire si le premier étage de la fusée Falcon 9 de SpaceX atterrira avec succès. Cette information est cruciale pour déterminer le coût d'un lancement : si le premier étage peut être récupéré, le coût du lancement est considérablement réduit.

Le projet suit une méthodologie complète de Data Science, allant de la collecte de données via API et Web Scraping jusqu'au déploiement d'un modèle de Machine Learning et d'un tableau de bord interactif.

---

## 🏗 Méthodologie & Workflow

Le projet est structuré en plusieurs étapes séquentielles, chacune correspondant à un notebook Jupyter ou un script spécifique :

### 1. Collecte de Données (Data Collection)
* **API SpaceX** : Récupération des données de lancement via l'API REST publique de SpaceX.
* **Web Scraping** : Extraction de données complémentaires depuis les pages Wikipédia des lancements Falcon 9.

### 2. Nettoyage & Préparation (Data Wrangling)
* Traitement des valeurs manquantes.
* Standardisation des formats de données.
* Encodage One-Hot (One-Hot Encoding) pour les variables catégorielles.

### 3. Analyse Exploratoire (EDA)
* **Visualisation** : Utilisation de Matplotlib et Seaborn pour identifier des modèles.
* **SQL** : Requêtes SQL pour répondre à des questions précises sur les données (taux de succès, charges utiles, etc.).

### 4. Analyse Visuelle Interactive
* **Folium** : Création de cartes interactives pour visualiser les sites de lancement et les succès/échecs d'atterrissage.
* **Dash** : Développement d'un tableau de bord web interactif pour explorer les données en temps réel.

### 5. Prédiction (Machine Learning)
* Entraînement de plusieurs modèles de classification (Régression Logistique, SVM, Arbre de Décision, KNN).
* Optimisation des hyperparamètres via GridSearchCV.
* Évaluation des performances pour sélectionner le meilleur modèle.

---

## 🛠 Technologies Utilisées

* **Langage** : Python 3
* **Bibliothèques Data** : Pandas, NumPy
* **Visualisation** : Matplotlib, Seaborn, Folium
* **Dashboarding** : Plotly Dash
* **Machine Learning** : Scikit-learn
* **Base de données** : SQL (SQLite/DB2)

---

## 📂 Structure du Projet

Voici la correspondance entre les fichiers et les étapes du projet :

| Fichier | Description |
| :--- | :--- |
| [`1.Data Collection Api .ipynb`](./1.Data%20Collection%20Api%20.ipynb) | Collecte des données via l'API SpaceX. |
| [`2.Data Collection with Web Scraping.ipynb`](./2.Data%20Collection%20with%20Web%20Scraping.ipynb) | Scraping des données historiques depuis Wikipédia. |
| [`3.Data wrangling .ipynb`](./3.Data%20wrangling%20.ipynb) | Nettoyage des données et Feature Engineering. |
| [`4.EDA with Visualization.ipynb`](./4.EDA%20with%20Visualization.ipynb) | Analyse exploratoire avec graphiques statiques. |
| [`5.EDA with SQL.ipynb`](./5.EDA%20with%20SQL.ipynb) | Analyse exploratoire via requêtes SQL. |
| [`6.Interactive Visual Analytics with Folium.ipynb`](./6.Interactive%20Visual%20Analytics%20with%20Folium.ipynb) | Cartographie interactive des sites de lancement. |
| [`7.spacex_dash_app.py`](./7.spacex_dash_app.py) | Application Dashboard (script Python exécutable). |
| [`8.Machine Learning Prediction.ipynb`](./8.Machine%20Learning%20Prediction.ipynb) | Comparaison et évaluation des modèles de prédiction. |

---

## 🚀 Installation et Utilisation

### Prérequis

Assurez-vous d'avoir Python installé avec les bibliothèques suivantes :

```bash
pip install pandas numpy matplotlib seaborn folium plotly dash scikit-learn requests beautifulsoup4
```

### Exécution des Notebooks
Vous pouvez ouvrir et exécuter les fichiers `.ipynb` dans l'ordre (de 1 à 8) en utilisant Jupyter Notebook, JupyterLab ou VS Code.

### Lancement du Dashboard
Pour lancer l'application interactive Dash (fichier n°7) :

1. Ouvrez un terminal dans le dossier du projet.
2. Exécutez la commande suivante :

```bash
python 7.spacex_dash_app.py
```

3. Ouvrez votre navigateur à l'adresse indiquée (généralement `http://127.0.0.1:8050/`).

> [!TIP]
> Le dashboard vous permet de filtrer les lancements par site et par charge utile (Payload) pour visualiser les corrélations avec le succès de l'atterrissage.

---

## 📊 Résultats Clés

> [!NOTE]
> Les résultats détaillés sont disponibles dans le notebook `8.Machine Learning Prediction.ipynb`.

Le projet compare plusieurs algorithmes pour déterminer lequel prédit le mieux l'atterrissage. Généralement, les arbres de décision (Decision Trees) ou les SVM offrent de bons résultats sur ce jeu de données après optimisation.
