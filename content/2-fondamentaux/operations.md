+++
date = '2026-01-20T09:53:45-05:00'
title = 'Opérations'
weight = 21
+++
## Les Opérations Arithmétiques

Python est une calculatrice scientifique extrêmement puissante. Pour manipuler vos données de laboratoire, vous devez maîtriser les opérateurs de base et l'ordre dans lequel Python les traite.

---

## 1. Les Opérateurs de base

La plupart des opérateurs sont identiques à ceux que vous utilisez en mathématiques.

| Opération | Symbole | Exemple | Résultat |
| :--- | :--- | :--- | :--- |
| Addition | `+` | `10 + 5` | `15` |
| Soustraction | `-` | `10 - 5` | `5` |
| Multiplication | `*` | `10 * 5` | `50` |
| Exposant | `**` | `10 ** 2` | `100` |


> **Attention** : En Python, l'exposant est `**`. Le symbole `^` existe mais il sert à la logique binaire (XOR). Pour calculer {{< math >}}$E = mc^2${{< /math >}}, on écrira `E = m * c**2`.

---

## 2. Les trois types de Divisions

C'est ici que les erreurs de calcul arrivent souvent. Python distingue la division réelle de la division entière.

### A. La division flottante (`/`)
Elle donne toujours un résultat précis (un `float`), même si les nombres tombent "juste".
```python
print(10 / 2)  # Affiche 5.0
print(7 / 2)   # Affiche 3.5
```

### B. La division entière (`//`)
Elle calcule combien de fois un nombre entre dans un autre et **ignore** le reste (troncature vers le bas).
```python
print(7 // 2)  # Affiche 3
```

### C. Le Modulo (`%`)
Il donne le **reste** de la division entière. Très utile en informatique pour vérifier la parité d'un nombre ou gérer des cycles.
```python
print(7 % 2)   # Affiche 1 (car 7 = 3 * 2 + 1)
```



---

## 3. Priorité des opérations (PEMDAS)

Python respecte fidèlement les règles d'algèbre que vous voyez en calcul différentiel. L'ordre de priorité est :

1.  **P**arenthèses `()`
2.  **E**xposants `**`
3.  **M**ultiplication et **D**ivision `*`, `/`, `//`, `%`
4.  **A**ddition et **S**oustraction `+`, `-`

**Exemple :**
$$x = 2 + 3 \times 4^2$$
En Python : `2 + 3 * 4**2` donnera **50** (car $3 \times 16 = 48$, puis $+ 2$).

> **Conseil de prof** : En cas de doute, utilisez des parenthèses. C'est plus lisible pour vous et pour la personne qui relira votre rapport de labo.

---

## 4. Opérateurs d'assignation composée

Pour simplifier l'écriture des mises à jour de variables (comme en cinématique), on peut utiliser des raccourcis :

```python
vitesse = 10
vitesse += 2  # Équivalent à : vitesse = vitesse + 2
vitesse *= 3  # Équivalent à : vitesse = vitesse * 3
```

---

### Exercice : Énergie Cinétique
La formule de l'énergie cinétique est $E_c = \frac{1}{2}mv^2$.
Traduisez cette formule en Python pour une masse $m = 10$ kg et une vitesse $v = 5$ m/s.

```python
m = 10
v = 5
# Votre code ici :
Ec = 0.5 * m * v**2
print(f"L'énergie cinétique est de {Ec} Joules")
```