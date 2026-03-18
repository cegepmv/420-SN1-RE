+++
date = '2026-03-18T16:20:02-04:00'
title = 'Structures_avances'
weight = 12
+++

### 1. Les Ensembles (`set`) : La théorie des ensembles en code
Un **set** est une collection non ordonnée d'éléments **uniques**. Si vous essayez d'ajouter deux fois la même chose, le `set` l'ignore.


* **Pourquoi l'utiliser ?** Pour éliminer les doublons instantanément.

```python
mesures = [10, 20, 10, 30, 20, 50]
uniques = set(mesures) 
# Résultat : {10, 20, 30, 50} (Magie : plus de doublons !)

# Opérations mathématiques éclair
groupe_A = {"Analyse", "Algebre", "Stats"}
groupe_B = {"Stats", "Programmation", "Reseaux"}

# Qui fait les deux ? (Intersection)
communs = groupe_A & groupe_B  # {'Stats'}
```

### 2. `enumerate`: index et valeur.

On a vu que for x in liste est propre, mais on perd l'index. for i in range(len(liste)) est moche, mais on a l'index.
enumerate() vous donne les deux sur un plateau d'argent.

```python
etudiants = ["Alice", "Bob", "Charlie"]

for i, nom in enumerate(etudiants, start=1):
    print(f"Rang {i} : {nom}")
```

### 3. `zip` : Fusionner des colonnes de données

Imaginez que vous avez une liste de noms et une liste de notes. Vous voulez les traiter ensemble. Au lieu de jongler avec les index, on "zippe" les listes comme une fermeture éclair.

```python
noms = ["Mathieu", "Sophie", "Yan"]
notes = [92, 88, 95]

for nom, note in zip(noms, notes):
    print(f"{nom} a obtenu {note}%")
```

### 4. `dict`(`zip`())
On peut facilement créer des dictionnaires à partir de listes en utilisant cette procédure, c'est parfois très utile:

```python
ids = ["E-01", "E-02", "E-03"]
concentrations = [0.45, 0.12, 0.78]

# BOOM : Une seule ligne
lab_data = dict(zip(ids, concentrations))

print(lab_data["E-02"])  # Affiche : 0.12
```