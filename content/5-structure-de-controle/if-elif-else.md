+++
date = '2026-02-11T07:05:28-05:00'
title = 'If Elif Else'
weight = 3
+++


La structure conditionnelle est le "système nerveux" de votre programme. C'est elle qui permet de passer d'une calculatrice linéaire à un logiciel capable d'analyser des données et de prendre des décisions.

## 1. La syntaxe fondamentale : `:` et Indentation

En Python, la hiérarchie du code ne dépend pas d'accolades, mais de la mise en page. C'est ce qu'on appelle la **syntaxe par indentation**.

* **Les deux-points (`:`)** : Ils annoncent à Python qu'un bloc de code spécifique commence.
* **L'indentation** : Le décalage vers la droite (généralement 4 espaces) indique quelles lignes appartiennent à la condition.

### Le "Si" simple (`if`)
C'est la prise de décision de base. Si la condition est vraie, le code est exécuté. Si elle est fausse, le programme saute simplement par-dessus.

```python
temperature = 25
if temperature > 20:
    print("La réaction chimique s'accélère.")
```
## 2. Le choix binaire (if-else)

Le **else** (Sinon) est le complément logique du **if**. Il permet de gérer deux issues mutuellement exclusives. C'est l'équivalent d'un aiguillage sur une voie ferrée : le programme emprunte soit la voie A, soit la voie B.



```python
concentration = 0.85
seuil = 0.80

if concentration <= seuil:
    print("Échantillon conforme.")
else:
    print("Alerte : Concentration trop élevée !")
```

**Note technique :** * Le **else** ne porte jamais de condition.
* Il sert de "bac de récupération" pour tout ce qui n'a pas été capturé par le `if`. 
* Il doit être parfaitement aligné verticalement avec son `if` pour que Python comprenne qu'ils forment un duo.

## 3. Les choix multiples (if-elif-else)

Pour gérer des systèmes à plusieurs états (ex: les phases de la matière, les catégories de pH ou des paliers de bourses d'études), on utilise **elif** (contraction de *else if*). 

```python
ph = 7.0

if ph < 7:
    print("La solution est acide.")
elif ph > 7:
    print("La solution est basique.")
else:
    print("La solution est neutre.")
```

L'ordinateur évalue les conditions de haut en bas. **Dès qu'une condition est vraie**, il exécute son bloc et **ignore totalement** le reste de la structure, même si d'autres conditions plus bas auraient pu être vraies aussi. L'ordre des conditions est donc primordial pour la logique scientifique.



## 4. L'imbrication

L'imbrication consiste à placer une structure `if` à l'intérieur d'un autre bloc `if`. Cela permet de créer des filtres successifs. Par exemple, on peut vérifier si un instrument de mesure est calibré avant de vérifier si la donnée qu'il transmet est dans les normes.

```python
tension = 220
appareil_allume = True

if appareil_allume:
    if tension > 230:
        print("Surtension détectée !")
    else:
        print("Fonctionnement normal.")
else:
    print("L'appareil est hors tension.")
```

> **Conseil de débogage :** Si votre programme affiche une **IndentationError**, vérifiez l'alignement de vos `if`, `elif` et `else`. Un seul espace de décalage et Python ne sait plus quelle condition appartient à quel bloc. C'est la cause numéro 1 de frustration chez les nouveaux programmeurs !

---
## 5. La "Vérité" des nombres (Truthy vs Falsy)

En Python, il n'y a pas que les comparaisons (comme `x > 10`) qui peuvent servir de condition. Les nombres eux-mêmes ont une valeur logique intrinsèque.

* **Le chiffre 0** est considéré comme **Faux** (`False`).
* **Tous les autres nombres** (positifs ou négatifs, comme `5`, `-1` ou `3.14`) sont considérés comme **Vrais** (`True`).



### Pourquoi est-ce utile ?
Cela permet parfois d'écrire du code plus court pour vérifier si une quantité existe. Par exemple, si vous comptez le nombre d'impuretés dans un échantillon, une condition peut simplement vérifier si ce nombre est différent de zéro sans avoir à l'écrire explicitement.

> **Analogie :** C'est comme un interrupteur. `0`, c'est le courant coupé (Faux). N'importe quel autre voltage, c'est le courant qui passe (Vrai).


**Défi :** Selon vous, que se passe-t-il dans une analyse de pH si on utilise uniquement une série de `if` au lieu de `if-elif-else` ? Est-ce que l'ordinateur pourrait afficher deux résultats contradictoires ?