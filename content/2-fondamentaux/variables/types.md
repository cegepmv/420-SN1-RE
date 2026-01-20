+++
date = '2026-01-20T10:17:46-05:00'
title = 'Types'
weight = 22
+++

## 1. Les types numériques

C'est ce que vous utiliserez le plus pour vos calculs de physique et de statistiques.

| Type Python | Nom | Description | Exemple |
| :--- | :--- | :--- | :--- |
| `int` | Entier | Nombres sans virgule (positifs ou négatifs). | `10`, `-5`, `0` |
| `float` | Flottant | Nombres à virgule (précision scientifique). | `3.14`, `-0.001`, `2.0` |
| `str` | Chaîne | Texte (lettres, chiffres, symboles). | `"Vitesse"`, `'A'` |
| `bool` | Booléen | Valeurs logiques (Vrai ou Faux). | `True`, `False` |

> **Attention :** Pour Python, `2` est un `int`, mais `2.0` est un `float`. Même si la valeur mathématique est la même, leur représentation en mémoire est totalement différente !



---

## 2. Le type Logique (Booléen)

Le type `bool` ne peut avoir que deux valeurs : `True` (Vrai) ou `False` (Faux). 
C'est le résultat d'une comparaison ou d'un test logique.

```python
est_en_mouvement = True
valeur_valide = False
```

---

## 3. Déterminer le type : `type()`

Si vous avez un doute sur la nature d'une variable, Python possède une fonction intégrée pour vous répondre :

```python
x = 9.81
print(type(x))  # Affiche <class 'float'>
```

---

## 4. La Conversion (Casting)

Parfois, vous recevez une donnée sous un format et vous devez la transformer pour faire un calcul. C'est ce qu'on appelle le **casting**.

### Pourquoi convertir ?
Imaginez que vous lisiez une mesure d'un capteur : elle arrive souvent sous forme de texte. Vous ne pouvez pas faire de calculs dessus sans la convertir.

```python
mesure_texte = "25.4"
# mesure_nombre = mesure_texte + 10  <-- ERREUR !

# On convertit le texte en nombre réel
mesure_nombre = float(mesure_texte)
resultat = mesure_nombre + 10  # Affiche 35.4
```

### Fonctions de conversion principales :
* `int()` : Transforme en entier (attention, cela coupe la partie décimale sans arrondir).
* `float()` : Transforme en nombre à virgule.
* `str()` : Transforme n'importe quoi en texte (pour l'affichage).



---

## 5. Le typage dynamique

En Python, contrairement à d'autres langages de programmation, vous n'avez pas besoin de déclarer le type à l'avance. Python est "intelligent" et devine le type selon la valeur que vous lui donnez.

```python
donnee = 10      # C'est un int
donnee = 10.5    # La même variable devient un float sans erreur
```

> **Conseil :** Cette flexibilité est pratique, mais soyez prudents ! Changer le type d'une variable en plein milieu d'un calcul complexe peut mener à des erreurs difficiles à trouver.

---

### Exercice rapide
Que se passe-t-il si vous faites `int(9.99)` ? 
1. Testez-le dans le terminal.
2. Est-ce que Python arrondit à 10 ou reste à 9 ?