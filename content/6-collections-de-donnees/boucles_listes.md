+++
date = '2026-03-18T16:20:14-04:00'
title = 'Boucles_listes'
weight = 2
+++


## Parcourir les données : Deux méthodes, deux styles

Pour traiter chaque élément d'une liste, il existe deux philosophies en Python. Imaginez que vous devez vérifier la température de 5 éprouvettes alignées sur un présentoir.

### Méthode A : L'index (Le "Où")
On utilise `range(len(liste))` pour obtenir les numéros de position. C'est précis, mais plus lourd à écrire.

### Méthode B : L'itération directe (Le "Quoi")
On demande à Python de nous donner directement l'objet. C'est la méthode "Pythonique", plus lisible et moins sujette aux erreurs de frappe.

---

### Comparaison visuelle
Prenons la liste : `metaux = ["Cuivre", "Argent", "Or", "Zinc"]`

| Index | Élément (`metaux[i]`) | Note |
| :--- | :--- | :--- |
| **0** | "Cuivre" | Début de la liste |
| **1** | "Argent" | |
| **2** | "Or" | |
| **3** | "Zinc" | Fin de la liste (`len-1`) |

---

### Exemple comparatif : Calcul de puissance

Supprimons le mystère. Voici le même résultat avec les deux approches :

```python
tensions = [110, 120, 220, 230]

# --- APPROCHE 1 : PAR INDEX (Classique) ---
for i in range(len(tensions)): # len est la longueur de la liste
    print(f"Prise n°{i} : {tensions[i]} Volts")

# --- APPROCHE 2 : DIRECTE (Moderne) ---
for v in tensions:
    print(f"Mesure détectée : {v} Volts")
```

## Exemple 1. Conversion de masse de livres en kilogrammes
On convertit une collection de poids en livres en créant une deuxième liste à partir d'une première.

```python
masses_livres = [150.5, 400.0, 1250.2, 75.8]
masses_kg = [] # on part avec une liste vide et on la popule

for m in masses_livres:
    conversion = m / 1000
    masses_kg.append(conversion)

print(f"Masses converties : {masses_kg}")
```

## Exemple 2. 
On mélange les if et les for: on compte les éléments dans une collection qui respectent une condition, puis on affiche ce compte.

```python
releves_ph = [7.2, 6.8, 5.5, 7.0, 4.2, 8.1]
nb_acides = 0

for ph in releves_ph:
    if ph < 7.0:
        nb_acides += 1
        print(f"Alerte : pH de {ph} est acide.")

print(f"Total d'échantillons acides : {nb_acides}")
```