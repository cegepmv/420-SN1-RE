+++
date = '2026-01-20T10:52:01-05:00'
title = 'Erreurs'
+++



## Les Flottants : L'incertitude numérique

En mécanique ou en physique, vous savez qu'une mesure n'est jamais infiniment précise. En informatique, c'est la même chose pour les nombres à virgule, appelés **flottants** (`float`). 

L'ordinateur utilise la norme **IEEE 754** pour stocker ces nombres dans un espace fini (64 bits). Cette limitation physique entraîne des comportements qui peuvent fausser vos calculs scientifiques si vous n'y prenez pas garde.

---

## 1. Le choc du 0.1 + 0.2

Testez ceci directement dans votre terminal Python :

```python
>>> 0.1 + 0.2
0.30000000000000004
```

### Pourquoi ce résultat ?
{{< math >}}
Certains nombres simples en base 10 (comme $0.1$) ont une expansion **infinie** en base 2, un peu comme $1/3$ donne $0.3333...$ en base 10. 
{{< /math >}}


Comme l'ordinateur ne peut pas stocker une infinité de chiffres, il doit **tronquer** ou **arrondir**. C'est cette minuscule différence qui s'accumule et devient visible.

---

## 2. Grands vs Petits nombres

Le format "flottant" fonctionne comme la notation scientifique : $1.23 \times 10^{15}$. L'ordinateur sépare le nombre en deux parties : la **mantisse** (les chiffres significatifs) et l'**exposant**.

### La perte de précision
Si vous ajoutez un nombre minuscule à un nombre immense, le petit nombre peut être "effacé" car il est trop petit par rapport à la précision (la résolution) du grand nombre.

```python
# Exemple de saturation de précision
grand_nombre = 10**16
print(grand_nombre == grand_nombre + 1) 
# Affiche : True
```

C'est une limite matérielle : l'ordinateur n'a plus assez de bits pour "voir" la différence. C'est ce qu'on appelle l'**erreur d'arrondi**.

---

## 3. Bonne pratique : La comparaison

À cause de ces erreurs, **il ne faut jamais utiliser `==` pour comparer deux flottants.**

* **ERREUR :** `if x == 0.3:`
* **SOLUTION :** On vérifie si la différence entre les deux valeurs est inférieure à une tolérance acceptable ($\epsilon$).

```python
x = 0.1 + 0.2
tolerance = 1e-10

if abs(x - 0.3) < tolerance:
    print("Les nombres sont considérés égaux pour le calcul.")
```
## 4. Un cas réel catastrophique : Le missile Patriot (1991)

Pourquoi est-ce que ces micro-erreurs d'arrondi sont graves ? En 1991, pendant la guerre du Golfe, un système de défense Patriot a échoué à intercepter un missile, causant la mort de 28 soldats.

### L'erreur technique
Le système calculait le temps en multipliant un compteur interne par **0.1**. 
* Comme nous l'avons vu, **0.1** a une erreur d'arrondi en binaire.
* Après 100 heures de fonctionnement, cette minuscule erreur s'est accumulée par addition répétée.



**Résultat :** Le décalage temporel était de **0.34 seconde**. 
À la vitesse d'un missile Scud (1600 m/s), cela représente une erreur de position de plus de **500 mètres**. Le missile Patriot a cherché la cible là où elle n'était plus.

> **Leçon pour l'ingénieur :** Une erreur de $10^{-7}$ peut sembler négligeable au début d'un calcul différentiel, mais sur un système qui tourne pendant des jours, elle peut devenir fatale.


---

## Ce qu'il faut retenir
1.  **Approximation** : Un `float` n'est pas une valeur exacte, c'est une estimation très précise (environ 15 à 17 chiffres significatifs).
2.  **Limites** : Il existe un plafond (environ $1.8 \times 10^{308}$) et un plancher très proche de zéro ($5.0 \times 10^{-324}$).
3.  **Ordre des calculs** : En statistiques ou en simulation, l'ordre des opérations peut influencer le résultat final à cause de la propagation des erreurs d'arrondi.