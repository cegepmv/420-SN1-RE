+++
date = '2026-01-20T10:17:02-05:00'
title = 'Binaire'
weight = 22
+++

## Comprendre le Binaire : Compter avec des interrupteurs

En mathématiques ou en mécanique, vous manipulez des nombres dans le système **décimal** (base 10). Cependant, au niveau matériel, un ordinateur ne comprend que deux états physiques : le courant passe (**1**) ou le courant ne passe pas (**0**). C'est ce qu'on appelle un **bit** (*binary digit*).

---

## 1. Rappel : La notation positionnelle (Base 10)

Pour comprendre le binaire, il faut réaliser que notre façon de noter les nombres est une **somme de puissances**. 

Quand vous écrivez le nombre **425**, vous faites l'opération suivante :
{{< math >}}
$$425 = (4 \times 10^2) + (2 \times 10^1) + (5 \times 10^0)$$
$$425 = 400 + 20 + 5$$
{{< /math >}}
Chaque position vers la gauche multiplie la valeur par la base (10).

---

## 2. Le Système Binaire (Base 2)

En informatique, la base n'est plus 10, mais **2**. Les seuls chiffres disponibles sont $\{0, 1\}$.

### Conversion : Du binaire vers le décimal
Prenons le nombre binaire **1011**. Pour trouver sa valeur, on utilise les puissances de 2 :

| Position | Puissance | Valeur | Bit | Calcul |
| :--- | :--- | :--- | :--- | :--- |
| 3 | $2^3$ | 8 | **1** | $1 \times 8 = 8$ |
| 2 | $2^2$ | 4 | **0** | $0 \times 4 = 0$ |
| 1 | $2^1$ | 2 | **1** | $1 \times 2 = 2$ |
| 0 | $2^0$ | 1 | **1** | $1 \times 1 = 1$ |
| **Total** | | | | **11** |

**Résultat :** $1011_2 = 11_{10}$

> **Analogie avec la mécanique :** Imaginez une balance avec des poids de $1, 2, 4, 8, 16...$ kg. Le nombre binaire indique simplement quels poids sont posés sur le plateau pour atteindre l'équilibre.

---

## 3. Pourquoi est-ce important pour un scientifique ?

Contrairement aux mathématiques pures où les nombres peuvent être infiniment grands, la mémoire d'un ordinateur est **physiquement limitée**.

1. **L'Octet (Byte) :** C'est un regroupement de **8 bits**. 
   * Le plus grand nombre stockable sur un octet est $11111111_2$, soit $255_{10}$.
2. **Le Dépassement (Overflow) :** Si vous tentez d'ajouter 1 à un espace mémoire déjà plein, le système "déborde". 

---

## 4. Manipulation avec Python

L'interpréteur Python permet de jongler facilement entre les bases. Testez ces commandes dans votre terminal :

```python
# Dire à Python qu'on écrit en binaire (préfixe 0b)
print(0b1011)        # Affiche 11

# Convertir un nombre décimal en binaire
print(bin(11))       # Affiche '0b1011'

# Un octet complet à 1
print(0b11111111)    # Affiche 255