+++
title = "Fonctions"
type = "chapter"
draft = true
weight = 3
+++

---

## 2. Les Docstrings (Chaînes de documentation)

C'est une fonctionnalité spécifique à Python pour documenter les fonctions, les classes et les modules. Contrairement aux commentaires classiques, les docstrings sont stockées dans l'attribut `__doc__` et peuvent être extraites par des outils de documentation.

```python
def calculer_aire(rayon):
    """
    Calcule l'aire d'un cercle à partir de son rayon.
    
    Args:
        rayon (float): Le rayon du cercle.
    Returns:
        float: L'aire calculée.
    """
    return 3.14159 * (rayon ** 2)

```

---
## 2. La Portée (Scope)

La **portée** définit où une variable est "visible" et utilisable dans votre code.

### Variables Locales
Une variable créée à l'intérieur d'un bloc spécifique (comme une fonction) est locale. Elle n'existe que là. C'est comme un brouillon de calcul que vous jetez après usage.

### Variables Globales
Une variable définie tout en haut de votre script, en dehors de tout bloc, est **globale**. Elle peut être lue de n'importe où dans le fichier.

[Image showing the difference between global scope (the whole house) and local scope (one specific room)]

---

## 3. Le mot-clé `global`

Si vous avez besoin de **modifier** une variable globale à l'intérieur d'une fonction, Python vous oblige à déclarer explicitement que vous savez ce que vous faites avec le mot-clé `global`.

```python
compteur = 0  # Variable globale

def incrementer():
    global compteur
    compteur = compteur + 1

incrementer()
print(compteur) # Affiche 1
```

---

## 4. Danger des variables globales

En tant que futurs scientifiques ou ingénieurs, vous devez être prudents avec les variables globales :

1. **Effets de bord :** Si plusieurs parties de votre programme modifient la même variable globale, il devient très difficile de trouver l'origine d'un bogue.
2. **Mémoire :** Les variables globales restent en mémoire pendant toute la durée de l'exécution, contrairement aux locales qui sont libérées rapidement.

> **Conseil de prof :** Utilisez les **constantes globales** (en MAJUSCULES) sans modération pour vos paramètres physiques, mais évitez au maximum les **variables globales modifiables**.