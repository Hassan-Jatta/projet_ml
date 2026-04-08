# Projet Optimisation Combinatoire : MCKP par Algorithme Génétique et Machine Learning

## Description du projet
Ce projet a été réalisé dans le cadre de l'UE d'Optimisation Combinatoire (M1 MIAGE MIXTE à l'Université Paris Nanterre). Il a pour objectif de concevoir et d'évaluer une approche hybride combinant une métaheuristique classique et un algorithme de Machine Learning pour résoudre le **Multiple Choice Knapsack Problem (MCKP)**, ou Problème du sac à dos à choix multiple.

L'approche se déroule en deux étapes principales :
1. **Métaheuristique de base** : Implémentation d'un Algorithme Génétique (AG) classique avec sélection par tournoi, évaluation de la fitness (avec gestion des pénalités liées à la capacité), croisement (implémentations à 1 et 2 points) et mutation.
2. **Amélioration par le Machine Learning** : Intégration d'un algorithme de classification (**Random Forest**) pour guider la construction des solutions et optimiser la recherche. Le modèle de ML s'entraîne sur les premières générations pour apprendre à distinguer les "bons" individus des "mauvais" en se basant sur la médiane des fitness. Une fois entraîné, le modèle de classification agit comme un filtre : il prédit la qualité des enfants générés avant de les intégrer à la nouvelle population, accélérant ainsi la convergence vers des solutions optimales tout en gardant une part d'exploration.

Le projet inclut également des expérimentations permettant de comparer l'algorithme génétique classique et l'algorithme génétique hybride (qualité de la fitness, rapidité de convergence et courbes d'évolution).

## Instructions d'exécution

### Prérequis
Pour exécuter ce projet, vous devez disposer de Python 3 et des bibliothèques standard pour la Data Science.
Nous recommandons l'utilisation de `pip` pour installer les dépendances :

```bash
pip install numpy matplotlib scikit-learn jupyter

```
### Lancement du projet
**1. Cloner le dépôt sur votre machine locale**
```bash
git clone [https://github.com/hassan-jatta/projet_ml.git](https://github.com/hassan-jatta/projet_ml.git)
cd projet_ml
```
**2. Lancer Jupyter :**

```bash
jupyter notebook
```
**3. Exécuter le code :**

* Ouvrez le fichier `MCKP_AG_ML.ipynb` depuis l'interface web de Jupyter.
* Le notebook est interactif et séquentiel. Exécutez les cellules de haut en bas.
* Il commence par les fonctions de génération d'instances, définit ensuite l'algorithme génétique standard, puis introduit la version hybride avec Random Forest, et enfin affiche les graphiques de comparaison des résultats (`matplotlib`).
(Note : Vous pouvez également ouvrir et exécuter ce notebook directement sur Google Colab).

### Structure du dépôt

```bash
projet_ml/
│
├── MCKP_AG_ML.ipynb    # Code source complet du projet (génération, AG classique, AG avec Machine Learning, et analyse visuelle des résultats)
└── README.md        
```
