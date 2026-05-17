+++
title = "Numpy Arrays"
type = "chapter"
weight = 7
draft = false
+++

En Python standard, les listes peuvent contenir n'importe quel type d'objet (des textes, des entiers, des listes, etc.). Cette flexibilité a un coût : chaque élément demande de la gestion en mémoire, ce qui rend les calculs sur de gros volumes de données extrêmement lents.


## Numpy array
NumPy (Numerical Python) résout ce problème en introduisant un nouvel objet : le ndarray (tableau multidimensionnel). Les tableaux NumPy possèdent deux caractéristiques fondamentales :

- L'homogénéité : Tous les éléments du tableau doivent obligatoirement posséder le même type de données (par exemple, uniquement des chiffres à virgule ou uniquement des entiers).

- Le stockage contigu : Les données sont stockées côte à côte en mémoire physique.

Cette structure permet d'éliminer le besoin d'écrire des boucles for en Python pour appliquer des calculs. On utilise plutôt la vectorisation : une opération mathématique appliquée sur un tableau NumPy s'exécute instantanément sur l'ensemble de ses éléments en arrière-plan, à une vitesse comparable à des langages de bas niveau comme le C et Fortran.

## Utilisation de numpy 

Pour utiliser la bibliothèque NumPy, il faut d'abord importer la librairie:

```python
import numpy as np
```

### Opérations avec numpy
Plus besoin de boucles for pour faire les opérations sur les éléments d'un tableau, elles se font directement:

```python
x = np.arange(5)
y = 2 ** x + 2 * x
# valeur de x : array([0, 1, 2, 3, 4])
# valeur de y : array([ 1,  4,  8, 14, 24])

```


## Créer un array Numpy

### Méthode 1: partir d'une liste ordinaire
```python
mon_tableau = np.array([1, 2, 3])

# array([1, 2, 3])
```

### Méthode 2: Utiliser np.arange
```python
mon_tableau = np.arange(0, 30, 2)

# équivalent à mais plus rapide que
ma_liste = [i for i in range(0,30,2)]
mon_tableau = np.array(ma_liste)

# équivalent mais supérieur à 
ma_liste = []
for i in range(0, 30, 2):
    ma_liste.append(i)
mon_tableau = np.array(ma_liste)
```

### Méthode 3: Utiliser np.linspace
```python
# place 11 données entre 0 et 10 inclusivement
mon_tableau = np.linspace(0, 10, 11)
# array([ 0.,  1.,  2.,  3.,  4.,  5.,  6.,  7.,  8.,  9., 10.])
```

### Méthode 4: générer des données aléatoires
Les méthodes de nombres aléatoires (np.random) utilisent un générateur de nombre aléatoires, basé sur l'horloge de l'ordinateur, pour créer un array numpy en se basant sur les instructions du programmeur.


#### Générer des entiers aléatoires
La méthode np.random.randint(start, stop, size) permet de créer {size} nombres entiers aléatoires entre {start} et {stop - 1}

```python
mon_tableau = np.random.randint(0, 10, 5)
# array([6, 6, 2, 3, 4])
```

#### Générer un nombre entre 0 et 1
La méthode np.random.random(size) permet de créer {size} nombres entiers aléatoires entre 0 et 1.

```python
# il est toujours possible de l'utiliser de n'importe quelle autre façon en faisant des opérations sur le numpy array.
mon_tableau = 2 * np.random.random(5) - 1
# array([ 0.41933666, -0.52965639,  0.13870528,  0.30943438,  0.12915535])
```


#### Générer des données normales (gaussienne, distribution en cloche)
La méthode np.random.normal(loc, scale, size) permet de créer {size} nombres normalement distribués autour de la moyenne {loc}, avec écart-type {scale}.


C'est la méthode par excellence pour ajouter du bruit dans les données, parce qu'une grande déviation est possible mais moins probable.



```python
mon_tableau = np.random.normal(100, 15, 4)
# il est aussi correct de le faire en utilisant les noms. Alors, l'ordre n'importe plus:
mon_tableau_b = np.random.normal(size = 4, scale = 15, loc = 100)
# array([ 87.6797127 , 104.3712966 ,  99.05110894, 100.20084564])
```


## Manipulations avancées

### Valeurs logiques

Numpy permet aussi de créer des tableaux Vrai/Faux selon une condition:

```python
temperatures = np.array([15, 22, 12, 28, 8])

# Est-ce que la température est supérieure à 20 degrés ?
meteo_chaude = temperatures > 20

print(meteo_chaude)
# Résultat : array([False,  True, False,  True, False])
```

### Statistiques
Les méthodes de Numpy nous donnent rapidement accès à des statistiques:

```python
donnees = np.array([10, 20, 30, 40])

print(donnees.max())   # Trouve la valeur maximale (40)
print(donnees.min())   # Trouve la valeur minimale (10)
print(donnees.mean())  # Calcule la moyenne de l'ensemble (25.0) (np.mean(donnees) fonctionne aussi)
```

### Slicing
Si on souhaite seulement prendre une partie d'un tableau, c'est facile avec numpy:

```python
notes = np.array([60, 75, 82, 90, 45])

# Prendre les trois premiers éléments (de l'index 0 à 3 exclu)
premiers = notes[0:3] 
# Résultat : array([60, 75, 82])

# Prendre tout à partir de l'index 2 jusqu'à la fin
fin_tableau = notes[2:] 
# Résultat : array([82, 90, 45])
# [:2] fait le contraire de [2:]
```