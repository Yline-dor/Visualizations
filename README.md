## Visualisations

### Aperçu

Lorsqu'on travaille sur un jeu de données, il est important de vérifier la distribution des données. Évidemment, pour la plupart des humains, il est difficile de visualiser les données en plus de trois dimensions.

La "viz" est importante pour comprendre les données et pour montrer les résultats. Nous allons découvrir trois bibliothèques pour visualiser les données en Python. Ce sont parmi les bibliothèques de visualisation les plus utilisées en Python :

- Module de visualisation de Pandas
- Matplotlib
- Plotly

### Jeu de rôle

Vous êtes un spécialiste de la visualisation de données dans une entreprise technologique de premier plan. Votre équipe a pour mission de créer un tableau de bord interactif pour présenter les principales informations issues de différents jeux de données de l'entreprise. Votre manager a insisté sur l'importance d'utiliser une variété de techniques de visualisation afin de communiquer efficacement des données complexes à la fois aux parties prenantes techniques et non techniques.

### Objectifs d'apprentissage

L'objectif est de comprendre les bases de ces bibliothèques. Vous aurez le temps durant le projet pour maîtriser l'une (ou les trois) d'entre elles.
VVous vous demandez peut-être pourquoi l'utilisation d'une seule bibliothèque ne suffit pas. La raison est simple : cela dépend de l'utilisation. Par exemple, si vous voulez vérifier rapidement les données, vous pouvez utiliser le module Pandas viz ou Matplotlib. Si vous voulez tracer un graphique personnalisé et plus élaboré, je vous suggère d'utiliser Matplotlib ou Plotly. Et, si vous voulez créer un graphique très joli et interactif, je vous suggère d'utiliser Plotly.

### Exercices du jour

- **Exercice 0 :** Environnement et bibliothèques
- **Exercice 1 :** Graphique Pandas 1
- **Exercice 2 :** Graphique Pandas 2
- **Exercice 3 :** Matplotlib 1
- **Exercice 4 :** Matplotlib 2
- **Exercice 5 :** Sous-graphiques Matplotlib
- **Exercice 6 :** Plotly 1
- **Exercice 7 :** Graphiques en boîte Plotly

### Environnement virtuel

- Python 3.x - NumPy - Pandas - Matplotlib - Plotly - Jupyter ou JupyterLab
  Nous suggérons d'utiliser la version la plus récente des packages.

### Exercice 0 : Environnement et bibliothèques

L'objectif de cet exercice est de configurer l'environnement de travail Python avec les bibliothèques requises.

**Remarque :** Pour chaque quête, votre premier exercice sera de configurer l'environnement virtuel avec les bibliothèques requises. Nous recommandons d'utiliser : - Les **dernières versions stables** de Python.

- L'environnement virtuel avec lequel vous êtes le plus à l'aise. `virtualenv` et `conda` sont les plus utilisés en Data Science.
- L'une des versions les plus récentes des bibliothèques requises.

1. Créez un environnement virtuel nommé `ex00`, avec une version de Python >= `3.9`, avec les bibliothèques suivantes : `pandas`, `numpy`, `jupyter`, `matplotlib` et `plotly`. --- ---

### Exercice 1 : Graphique Pandas 1 L'objectif de cet exercice est d'apprendre à créer des graphiques en utilisant Pandas. `.plot()` de Pandas est un wrapper pour `matplotlib.pyplot.plot()`. Voici les données que nous allons utiliser : `python df = pd.DataFrame({ 'name':['christopher','marion','maria','mia','clement','randy','remi'], 'age':[70,30,22,19,45,33,20], 'gender':['M','F','F','F','M','M','M'], 'state':['california','dc','california','dc','california','new york','porto'], 'num_children' [2,0,0,3,8,1,4], 'num_animaux':[5,1,0,5,2,2,3] }) `

1. Reproduisez ce graphique. Ce graphique s'appelle un diagramme en barres. ![texte alternatif][logo] [logo]: ./w1day03_ex1_plot1.png "Diagramme en barres ex1" Le graphique doit contenir : - le titre - nom sur l'axe des x - légende --- ---

### Exercice 2 : Graphique Pandas 2 L'objectif de cet exercice est d'apprendre à créer des graphiques en utilisant Pandas.

La méthode `.plot()` de Pandas est une enveloppe pour `matplotlib.pyplot.plot()`. `python df = pd.DataFrame({ 'name':['christopher','marion','maria','mia','clement','randy','remi'], 'age':[70,30,22,19,45,33,20], 'genre':['M','F','F','F','M','M','M'], 'etat':['california','dc','california','dc','california','new york','porto'], 'num_enfants':[4,2,1,0,3,1,0], 'num_animaux':[5,1,0,2,2,2,3] }) ` 1. Reproduisez ce graphique. Ce graphique s'appelle un nuage de points. Observez-vous une relation entre l'âge et le nombre d'enfants ? ![texte alternatif][logo_ex2] [logo_ex2]: ./w1day03_ex2_plot1.png "Nuage de points ex2" Le graphique doit contenir : - le titre - nom sur l'axe des x - nom sur axe des y --- ---

### Exercice 3 : Matplotlib 1 L'objectif de ce graphique est d'apprendre à utiliser Matplotlib pour tracer des données.

Comme vous le savez, Matplotlib est la bibliothèque sous-jacente utilisée par Pandas. Elle offre plus d'options pour créer des visualisations personnalisées. Cependant, la plupart des graphiques que nous créerons avec Matplotlib peuvent être reproduits avec la méthode `.plot()` de Pandas.

1.  Reproduisez ce graphique. Nous supposons que les points de données ont des coordonnées entières. ![alt text][logo_ex3] [logo_ex3]: ./w1day03_ex3_plot1.png "Graphique de dispersion ex3" Le graphique doit contenir : - le titre - le nom de l'axe des x et de l'axe des y - les axes x et y sont limités à [1,8] - **style** : - ligne rouge point-trait d'une largeur de 3 - cercles bleus d'une taille de 12 --- ---

### Exercice 4 : Matplotlib 2 L'objectif de ce graphique est d'apprendre à utiliser Matplotlib pour tracer différentes lignes dans le même graphique sur des axes différents en utilisant `twinx`.

Ceci est très utile pour comparer des variables ayant des plages différentes. Voici les données : `python left_data = [5, 7, 11, 13, 17] right_data = [0.1, 0.2, 0.4, 0.8, -1.6] x_aaxis = [0.0, 1.0, 2.0, 3.0, 4.0] ` 1. Reproduisez ce graphique ![alt text][logo_ex4] [logo_ex4]: ./w1day03_ex4_plot1.png "Graphique à axes jumeaux ex4" Le graphique doit contenir : - le titre - le nom des axes y gauche et droit - **style** : - données de gauche en noir - données de droite en rouge --- ---

### Exercice 5 : Sous-graphiques Matplotlib L'objectif de cet exercice est d'apprendre à utiliser Matplotlib pour créer des sous-graphiques.

1.  Reproduisez ce graphique en utilisant une **boucle for** : ![alt text][logo_ex5] [logo_ex5]: ./w1day03*ex5_plot1.png "Sous-graphiques ex5" Le graphique doit contenir : - 6 sous-graphiques : 2 lignes, 3 colonnes - Garder de l'espace entre les graphiques : `hspace=0.5` et `wspace=0.5` - Chaque graphique contient : - Texte (2,3,i) centré en 0.5, 0.5. \_Astuce* : Vérifiez le paramètre `ha` de `text` - un titre : Titre i --- ---

### Exercice 6 : Plotly 1 Plotly a beaucoup évolué ces dernières années. Il est important de **toujours consulter la documentation**.

Plotly est fourni avec une interface de haut niveau : Plotly Express. Elle permet de construire facilement certains graphiques complexes. La leçon ne s'arrêtera pas ici détaillez les exemples complexes. Plotly Express est assez intéressant lorsqu'on utilise des DataFrames Pandas car il existe certaines fonctions intégrées qui tirent parti des DataFrames Pandas. Le graphique généré par Plotly est interactif et peut également être dynamique. L'objectif de l'exercice est de tracer le prix d'une entreprise. Son prix est généré ci-dessous. `python returns = np.random.randn(50) price = 100 + np.cumsum(returns) dates = pd.date_range(start='2020-09-01', periods=50, freq='B') df = pd.DataFrame(zip(dates, price), columns=['Date','Company_A']) `

1.  En utilisant **Plotly Express**, reproduisez le graphique de l'image. Comme les données sont générées aléatoirement, je ne m'attends pas à ce que vous reproduisiez exactement la même courbe. ![alt text][logo_ex6] [logo_ex6]: ./w1day03_ex6_plot1.png "Série temporelle ex6" Le graphique doit contenir : - un titre - un nom pour l'axe des x - un nom pour l'axe des y
2.  Même question mais cette fois en utilisant `plotly.graph_objects`. Vous devrez peut-être utiliser `init_notebook_mode` de `plotly.offline`. - [Ressource](https://plotly.com/python/time-series/) --- ---

#### Exercice 7 : Graphiques en boîte avec Plotly L'objectif de cet exercice est d'apprendre à utiliser Plotly pour tracer des graphiques en boîte.

C'est une méthode pour représenter graphiquement des groupes de données numériques à travers leurs quartiles et leurs valeurs min et max. Elle permet de comparer rapidement certaines variables.

Générez 3 tableaux aléatoires à partir d'une distribution normale. Conservez-en un tel quel et pour les deux autres tableaux, ajoutez respectivement 1 et 2 à la distribution normale.

```python
y0 = np.random.randn(50)
y1 = np.random.randn(50) + 1  # décaler la moyenne
y2 = np.random.randn(50) + 2
```

1. Dans la même figure, tracez les 3 distributions sous forme de graphiques en boîte comme montré sur l'image. Dans cet exercice, le style n'est pas important.

![alt text][logo_ex7]
[logo_ex7]: ./w1day03_ex7_plot1.png "Graphique en boîte ex7"

Le graphique doit contenir :

- Le titre
- La légende

### Ressources

- [Ressource 1](https://matplotlib.org/3.3.3/tutorials/index.html)
- [Ressource 2](https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596)
- [Ressource 3](https://github.com/rougier/matplotlib-tutorial)
- [Ressource 4](https://jakevdp.github.io/PythonDataScienceHandbook/05.13-kernel-density-estimation.html)
- [Ressource 5](https://plotly.com/python/box-plots/)
