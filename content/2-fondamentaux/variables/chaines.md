+++
date = '2026-01-20T10:03:20-05:00'
title = 'Chaines'
weight = 23
+++

## Les Chaînes de Caractères (Strings)

Une chaîne de caractères, notée `str` en Python, est une suite de symboles (lettres, chiffres, espaces, ponctuation) entourée de guillemets.

---

## 1. Définition et Syntaxe

Vous pouvez utiliser des guillemets simples `'` ou doubles `"` :

```python
laboratoire = "Physique 1"
unite = 'mètres par seconde'
```

### L'immuabilité (Concept important)
En Python, les chaînes sont **immuables**. Cela signifie qu'une fois créée, vous ne pouvez pas modifier une lettre à l'intérieur de la "boîte". Si vous transformez la chaîne, Python en crée simplement une nouvelle ailleurs en mémoire.



---

## 2. La Concaténation (L'addition de texte)

On utilise le symbole `+` pour coller deux chaînes ensemble. Attention : Python ne devine pas les espaces, il faut les ajouter manuellement !

```python
nom = "Galilée"
action = "étudie la chute des corps."

phrase = nom + " " + action
print(phrase) # Affiche: Galilée étudie la chute des corps.
```

> **Piège classique :** Vous ne pouvez pas concaténer un `str` et un `int` directement.
> `print("Score: " + 10)` -> **Erreur !**
> Il faut convertir : `print("Score: " + str(10))`

---

## 3. Les f-strings (La méthode moderne)

Depuis Python 3.6, on utilise les **f-strings** (formatted strings). C'est la méthode la plus propre et la plus rapide pour intégrer des variables dans du texte.

On place un `f` juste avant les guillemets et on insère les variables entre accolades `{}`.

```python
temp = 22.5
unite = "Celsius"

# Simple et lisible
message = f"La température du capteur est de {temp} {unite}."
print(message)
```

### Pourquoi c'est génial pour les sciences ?
Les f-strings permettent de formater les nombres (arrondir l'affichage) directement à l'intérieur de la chaîne sans modifier la valeur réelle de la variable.

```python
pi_long = 3.1415926535
# Afficher seulement 2 décimales
print(f"La valeur de pi arrondie est : {pi_long:.2f}") 
# Affiche: 3.14
```

---

## 4. Caractères spéciaux

Certains caractères ont une fonction de mise en forme :
* `\n` : Saut de ligne (Nouvelle ligne).
* `\t` : Tabulation (Pratique pour aligner des colonnes de données).

```python
print("Résultats:\nNom\tValeur\ng\t9.81")
```



---

### Exercice de labo
Essayez de générer une phrase qui affiche le résultat d'un calcul de vitesse {{< math >}}($v = d/t$){{< /math >}} en utilisant une f-string, arrondie à une seule décimale.

```python
distance = 100
temps = 9.58
vitesse = distance / temps

# À vous de jouer avec la f-string !
```

