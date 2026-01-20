+++
date = '2026-01-20T10:19:57-05:00'
title = 'Constantes'
weight = 21
+++


## Constantes

Dans un programme scientifique, certaines valeurs ne devraient jamais changer.

---

## 1. Les Constantes - standard

En Python, il n'existe pas de "vraies" constantes protégées par le langage (contrairement au C++ ou au Java, d'autres langages de programmation). Par convention, les programmeurs utilisent des **MAJUSCULES** pour indiquer qu'une valeur ne doit pas être modifiée.

### Pourquoi les utiliser ?
Pour éviter les "nombres magiques" dans le code. Il est plus clair d'écrire `GRAVITÉ` que d'utiliser `9.81` à dix endroits différents.

```python
# Convention de nommage des constantes
PI = 3.14159
ACCELERATION_G = 9.81
VITESSE_LUMIERE = 299792458
```

> **Règle d'or :** Si vous voyez une variable en majuscules, ne lui réassignez jamais de nouvelle valeur. C'est un contrat moral entre programmeurs.

---

## 2. Le module `math`

Pour accéder à ces constantes, on doit d'abord "importer" le module mathématique. C'est comme sortir une calculatrice scientifique de son sac.

```python
import math

print(math.pi)   # Rapport de la circonférence au diamètre (π)
print(math.e)    # Constante d'Euler (base des logarithmes naturels)
print(math.tau)  # Égal à 2π (utilisé en ingénierie et physique)
```

### Pourquoi utiliser `math.pi` plutôt que `3.14` ?
En calcul différentiel ou en mécanique, l'accumulation d'erreurs peut être fatale (rappelez-vous l'exemple du missile Patriot). `math.pi` vous donne la précision maximale permise par votre processeur (environ 15 chiffres significatifs).

---

## 3. Les constantes de l'infini et "Not a Number"

Parfois, un calcul échoue ou dépasse les limites de la machine. Python a des constantes pour représenter ces états :

* **`math.inf`** : Représente l'infini mathématique. Utile pour initialiser une valeur minimale que l'on veut dépasser.
* **`math.nan`** : Signifie *Not a Number*. C'est ce qu'on obtient si on essaie de faire un calcul indéfini (comme $0/0$ dans certains contextes ou la racine carrée d'un nombre négatif sans nombres complexes).



---

## 4. Sensibilisation : Le module `scipy` (Aperçu)

Bien que nous ne l'utiliserons pas tout de suite, sachez que pour vos cours avancés de physique ou de chimie, le module `scipy.constants` contient tout le tableau périodique et les constantes universelles :

```python
# Exemple de ce qui existe (ne pas apprendre par cœur)
# from scipy.constants import G, c, h

# G : constante gravitationnelle
# c : vitesse de la lumière
# h : constante de Planck
```

---

## 5. Les constantes de l'interpréteur

Il existe aussi des constantes "système" que vous rencontrerez souvent :

* **`True` / `False`** : Les constantes booléennes (logique).
* **`None`** : Représente l'absence de valeur. C'est l'équivalent du "vide" ou de l'ensemble vide $\emptyset$. On l'utilise pour dire qu'une variable n'a pas encore de résultat.

---

### Exercice de réflexion
Si vous calculez la trajectoire d'un projectile et que le résultat de votre équation est `math.inf`, qu'est-ce que cela signifie physiquement pour votre simulation ?

Cherchez trois explications plausibles.