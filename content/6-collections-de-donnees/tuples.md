+++
date = '2026-03-18T16:19:32-04:00'
title = 'Tuples'
weight = 7
+++

## 10. Les structures immuables : Sécuriser ses données

Contrairement aux listes que l'on peut modifier à l'infini (`.append`, `.pop`, etc.), Python propose des structures "en lecture seule". Une fois créées, on ne peut plus changer leur contenu.

### 1. Le Tuple : Une liste figée
On crée un tuple avec des parenthèses `()`. C'est l'outil idéal pour stocker des constantes ou des coordonnées qui ne doivent pas bouger.

```python
# Coordonnées GPS d'un laboratoire
position = (45.5017, -73.5673)

# On peut lire les données comme une liste
lat = position[0]

# MAIS on ne peut pas les modifier !
# position[0] = 46.0  <-- Provoquera une ERREUR (TypeError)
```

## 11. Le piège de la virgule (Français vs Python)

C'est l'erreur numéro 1 pour les étudiants francophones. En mathématiques au Québec, on écrit souvent `3,14`. En Python, si vous écrivez une virgule au lieu d'un point, vous ne créez pas un nombre... vous créez un **Tuple**.

### La différence fatale

Regardez bien ce qui se passe dans la console Python :

```python
# Ce que vous voulez (un nombre décimal / float)
pi_correct = 3.14
print(type(pi_correct))  # Résultat : <class 'float'>

# Ce que vous écrivez par habitude (un tuple !)
pi_erreur = 3,14
print(type(pi_erreur))   # Résultat : <class 'tuple'>
```