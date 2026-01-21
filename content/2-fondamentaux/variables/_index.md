+++
date = '2026-01-20T10:03:03-05:00'
title = 'Variables'
weight = 23
+++
## Les Variables : Gérer la mémoire

Pour un ordinateur, une **variable** est une zone nommée dans la mémoire vive (RAM) où l'on stocke une information pour la réutiliser plus tard.

---

## 1. L'Analogie de la Boîte

Imaginez la mémoire de l'ordinateur comme un immense entrepôt rempli de casiers. Pour utiliser un casier, vous avez besoin de deux choses :
1. **Une étiquette** (le nom de la variable) pour le retrouver.
2. **Un contenu** (la valeur) rangé à l'intérieur.



### Syntaxe de l'assignation
En Python, on utilise l'opérateur `=` pour lier un nom à une valeur. 

```python
vitesse = 100
```
*Ici, on ne dit pas que "vitesse est égal à 100" au sens mathématique, mais plutôt : "Mets la valeur 100 dans l'étiquette vitesse".*

---

## 2. Réutilisation et Mise à jour

Contrairement à une constante en physique, une variable peut changer au cours de l'exécution du programme.

```python
position = 10
print(position) # Affiche 10

position = position + 5
print(position) # Affiche 15
```

**Note pour le calcul différentiel :** L'instruction `position = position + 5` est une hérésie en mathématiques ($x = x + 5$ est impossible), mais en informatique, c'est une **mise à jour** : on prend l'ancienne valeur, on ajoute 5, et on écrase l'ancien contenu du casier.

---

## 3. Le cycle de vie d'une variable

### Création
Une variable naît dès qu'on lui assigne une valeur pour la première fois.

### Suppression (`del`)
On peut libérer manuellement un espace mémoire si on n'en a plus besoin, bien que Python gère cela automatiquement (via le *Garbage Collector*).
```python
x = 500
del x
# print(x) <-- Provoquerait une erreur car 'x' n'existe plus
```

### Le "Swap" (Échange)
Comment échanger le contenu de deux boîtes ? 
En physique, si vous avez deux béchers, il vous en faut un troisième pour ne pas mélanger les liquides. En Python, il existe une syntaxe élégante :

```python
a = 1
b = 2

# La méthode "magique" de Python
a, b = b, a

print(a) # Affiche 2
print(b) # Affiche 1
```



---

## 4. Bonnes pratiques de nommage (Style)

Puisque vous travaillez en équipe de labo, vos noms de variables doivent être explicites :
* **OUI :** `vitesse_initiale`, `temp_celsius`, `force_f`
* **NON :** `a`, `var1`, `truc`

> **Règle d'or :** Le code est lu beaucoup plus souvent qu'il n'est écrit. Nommez vos variables pour l'humain qui passera derrière vous !