+++
date = '2026-03-18T16:11:41-04:00'
title = 'Dictionnaires'
weight = 3
+++

## 8. Les Dictionnaires : Organiser par étiquettes

Si la **liste** est une file d'attente (on accède par la position), le **dictionnaire** est un classeur (on accède par une étiquette). Au lieu d'un numéro d'index (0, 1, 2...), on utilise une **clé** pour retrouver une **valeur**.

C'est la structure de base derrière presque tout le Web (JSON).

### Création et accès : Le duo Clé-Valeur
On utilise des accolades `{}` et le symbole `:` pour lier une clé à sa valeur.

```python
# Un dictionnaire représentant un serveur
serveur = {
    "nom": "SRV-LAB-01",
    "ip": "192.168.1.10",
    "etat": "actif",
    "utilisateurs": 12
}

# Accéder à une info précise via sa clé
print(f"Le serveur {serveur['nom']} est actuellement {serveur['etat']}.")
```

### Exemple 1 : Mise à jour et ajout
Contrairement aux listes où l'on utilise .append(), avec un dictionnaire, il suffit d'assigner une valeur à une nouvelle clé.

```python
config = {"theme": "sombre", "langue": "fr"}

# Modifier une valeur existante
config["theme"] = "clair"

# Ajouter une nouvelle paire clé-valeur
config["auto_save"] = True

print(config)
```

### Exemple 2: boucle de dictionnaire (matière optionnelle)

C'est ici que les dictionnaires deviennent un puissant outil d'automatisation. On peut récupérer les clés, les valeurs, ou les deux en même temps avec .items().

```python
inventaire = {
    "pommes": 50,
    "bananes": 30,
    "oranges": 12
}

print("État des stocks :")
for fruit, quantite in inventaire.items():
    if quantite < 20:
        print(f"⚠️ Réapprovisionner : {fruit} ({quantite} restants)")
    else:
        print(f"Stock OK : {fruit}")
```