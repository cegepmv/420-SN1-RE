+++
date = '2026-01-20T12:01:45-05:00'
title = 'Intéraction Utilisateur'
weight = 24
+++

## Interagir avec l'utilisateur

Un programme doit souvent poser des questions et communiquer des réponses/résultats. Pour cela, nous utilisons deux fonctions de base dans le terminal.

---

## 1. La fonction `print()` : Afficher des données

La fonction `print()` envoie des informations vers la **sortie standard** (votre terminal).

### Plusieurs arguments
Vous pouvez passer plusieurs éléments à `print()`, séparés par des virgules. Python ajoutera automatiquement un espace entre eux.

```python
nom = "Mars"
gravite = 3.71
print("La gravité sur", nom, "est de", gravite, "m/s².")
```

### Paramètres utiles
* `sep` : Modifier le séparateur entre les éléments (par défaut un espace).
* `end` : Modifier ce qui s'affiche à la fin (par défaut un saut de ligne `\n`).

```python
print("Chargement", end="...")
print("Terminé") 
# Affiche: Chargement...Terminé (sur la même ligne)
```

---

## 2. La fonction `input()` : Récupérer des données

La fonction `input()` met le programme en pause et attend que l'utilisateur tape quelque chose au clavier et appuie sur **Entrée**.

```python
nom_usager = input("Quel est votre nom ? ")
print(f"Bonjour {nom_usager} !")
```



---

## 3. Le piège de l'input (Crucial pour les calculs)

C'est l'erreur numéro 1 des débutants en programmation scientifique : **`input()` retourne TOUJOURS du texte (`str`)**, même si vous tapez un nombre.

### Le problème :
```python
rayon = input("Entrez le rayon du cercle : ")
# surface = 3.14 * (rayon ** 2)  <-- ERREUR !
# On ne peut pas faire de maths sur du texte.
```

### La solution : La conversion immédiate
Pour faire des calculs, vous devez "envelopper" votre input dans une fonction de conversion (`int` ou `float`).

```python
# Conversion en nombre à virgule (float)
rayon = float(input("Entrez le rayon en cm : "))
surface = 3.14159 * (rayon ** 2)

print(f"La surface est de {surface:.2f} cm².")
```



---

## 4. Résumé du flux de travail

1. **Entrée** : `input()` récupère la saisie (texte).
2. **Traitement** : Conversion du texte en nombre + calcul mathématique.
3. **Sortie** : `print()` affiche le résultat final formaté.

---

### Exercice : Mini-convertisseur de labo
Créez un court script qui :
1. Demande une température en **Celsius** à l'utilisateur.
2. La convertit en **Kelvin** (ajoute 273.15).
3. Affiche le résultat avec une phrase claire.

```python
# Votre code ici
```