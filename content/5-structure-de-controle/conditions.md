+++
date = '2026-02-11T07:05:16-05:00'
title = 'Conditions'
weight = 2
+++

+++
title = "Conditions et Booléens"
weight = 1
+++

Avant de pouvoir dire à l'ordinateur de "choisir", il faut lui apprendre à "comparer". 

## 1. Le type Booléen (`bool`)

En programmation, une condition est une expression qui ne peut avoir que deux états : **Vrai (`True`)** ou **Faux (`False`)**. C'est ce qu'on appelle un booléen, en l'honneur du mathématicien George Boole.

## 2. Les opérateurs de comparaison

Pour poser une question à Python, on utilise des opérateurs de comparaison. Le résultat de ces opérations est toujours un booléen.

| Opérateur | Signification | Exemple | Résultat |
| :--- | :--- | :--- | :--- |
| `==` | Est égal à | `5 == 5` | `True` |
| `!=` | Est différent de | `5 != 3` | `True` |
| `>` | Strictement plus grand | `10 > 10` | `False` |
| `<` | Strictement plus petit | `2 < 8` | `True` |
| `>=` | Plus grand ou égal | `10 >= 10` | `True` |
| `<=` | Plus petit ou égal | `5 <= 2` | `False` |

> **⚠️ Attention au piège :** > * `=` sert à **assigner** une valeur (ex: `x = 10`).
> * `==` sert à **comparer** deux valeurs (ex: `x == 10`).
> * C'est l'erreur de syntaxe la plus fréquente chez les débutants !

## 3. Les opérateurs logiques

En sciences, on doit souvent vérifier plusieurs conditions à la fois (par exemple, vérifier si une température est comprise dans un intervalle).

* **`and` (ET) :** Vrai seulement si **toutes** les conditions sont vraies.
    * *Exemple :* `(temp > 0) and (temp < 100)` est vrai si l'eau est liquide.
* **`or` (OU) :** Vrai si **au moins une** des conditions est vraie.
    * *Exemple :* `(ph < 1) or (ph > 13)` est vrai si la solution est très corrosive.
* **`not` (NON) :** Inverse le résultat (le vrai devient faux et vice-versa).

## 4. Testez-le dans la console !

Essayez de deviner le résultat de cette expression avant de la tester :
```python
x = 10
y = 5
print(x > 8 and y < 2)