+++
date = '2026-02-11T07:08:50-05:00'
title = 'For Imbrique'
weight = 6
+++


# Les Boucles Imbriquées 🔄
### Comprendre la structure "Boucle dans une boucle"

---

## L'Analogie de l'Horloge 🕒

Pour chaque **heure** qui passe (boucle externe)...
...les **minutes** doivent faire un tour complet (boucle interne).


* **Heure 1** : 1min, 2min, ..., 59min.
* **Heure 2** : 1min, 2min, ..., 59min.




---

## Syntaxe en Python 🐍

Le bloc de la boucle interne est **indenté** à l'intérieur de la boucle externe.

```python {line-numbers="1|2|3|1-3"}
for i in range(3):        # Boucle EXTERNE
    for j in range(2):    # Boucle INTERNE
        print(f"i:{i}, j:{j}")
```
## Cas concret: traitement d'images
En IA et en multimédia, une image est une grille de pixels.

```python {line-numbers="1|2|3|1-3"}
for y in range(hauteur):    # Pour chaque ligne
    for x in range(largeur): # Pour chaque pixel de la ligne
        appliquer_filtre(x, y)
```

## Défi: afficher la table de multiplications des 12 premiers nombres
