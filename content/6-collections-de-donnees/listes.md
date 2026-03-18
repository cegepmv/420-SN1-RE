+++
date = '2026-03-18T16:11:48-04:00'
title = 'Listes'
weight = 1
+++

## Les Listes : Organiser des séquences de données

Jusqu'à présent, nous avons utilisé des variables simples pour stocker une seule valeur (ex: `population = 100`). Mais comment gérer 1000 mesures de température ou une liste de noms d'étudiants ? 

C'est là qu'interviennent les **listes**. Une liste est un conteneur qui peut contenir plusieurs éléments, ordonnés, que l'on peut modifier à volonté.

### Création et accès : Le système d'index
En Python, on crée une liste avec des crochets `[]`. Chaque élément est séparé par une virgule.

```python
# Une liste de mesures de pH
mesures = [7.0, 6.5, 8.2, 7.4, 5.9]

# Accéder au premier élément (L'informatique commence à 0 !)
premier = mesures[0]  # 7.0

# Accéder au dernier élément (L'astuce du -1)
dernier = mesures[-1]  # 5.9
```

### Manipulation de listes

```python
notes = [85, 92, 78]

# Ajouter une note à la fin
notes.append(95) 

# Modifier la deuxième note (index 1)
notes[1] = 94

# Longueur de la liste (combien d'éléments ?)
nb_notes = len(notes)

print(f"La moyenne des {nb_notes} notes est : {sum(notes)/nb_notes:.2f}")
```

Voir la documentation: https://www.geeksforgeeks.org/python/python-lists/ 