+++
date = '2026-02-11T07:08:33-05:00'
title = 'Boucles While'
weight = 5
+++

## 7. La boucle `while` : Répéter jusqu'à un objectif

Contrairement à la boucle `for` qui parcourt une séquence prédéterminée, la boucle **`while`** (Tant que) répète un bloc de code aussi longtemps qu'une condition logique reste **vraie**. 

C'est l'outil idéal pour les processus itératifs où l'on ne sait pas d'avance combien d'étapes seront nécessaires pour atteindre un résultat (ex: atteindre un équilibre chimique ou une précision numérique).



### Exemple : La demi-vie radioactive
Imaginons que vous étudiez un isotope. Vous voulez savoir combien de cycles de demi-vie sont nécessaires pour que la radioactivité tombe sous un seuil de sécurité (5% de la dose initiale).

```python
quantite = 100.0  # mg
seuil_securite = 5.0
cycles = 0

while quantite > seuil_securite:
    quantite = quantite / 2
    cycles += 1
    print(f"Après {cycles} cycle(s), il reste {quantite:.2f} mg.")

print(f"Sécurité atteinte après {cycles} cycles.")
```

### Le danger : La boucle infinie
C'est l'erreur classique : si votre condition ne devient jamais fausse, le programme boucle éternellement.

Note technique : Pour éviter cela, assurez-vous qu'à l'intérieur de votre while, il y a une instruction qui modifie la variable testée (comme quantite = quantite / 2 ci-dessus).

Voici un exemple à ne pas faire: 

```python 
while 1 > 0: 
    print('a')
```

Ce programme continuera éternellement à imprimer le caractère 'a'.


### L'algorithme d'Héron (Exemple avancé)
L'extraction d'une racine carrée par la méthode d'Héron est un classique en calcul numérique. On cherche la racine de $x$ en affinant une estimation de manière itérative :

{{< math >}}
$$x_{n+1} = \frac{x_n + \frac{S}{x_n}}{2}$$
{{< /math >}}

On définit la condition d'arrêt comme la suivante: 

{{< math >}}
$$\epsilon = |x_n^2 - S| > \text{tolérance}$$
{{< /math >}}

Complétez le programme suivant pour évaluer l'algorithme de Héron à une précision fixe. 

```python
nombre = 2          # Le nombre dont on cherche la racine
racine = 1.0        # La racine estimée avec Héron
tolerance = 0.00001 # La tolérance 

condition = False   # uniquement pour que le programme ne plante pas avant votre code 
while condition :
    pass
    # traitement

print(f"La racine approximative est {estimation}")
```

**Défi!** Essayez d'afficher également le nombre d'itérations avant d'arriver à une solution assez proche.