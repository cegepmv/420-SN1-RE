+++
date = '2026-01-21T09:26:35-05:00'
title = 'Commentaires'
weight = 20
+++

---

## 💡 Pourquoi commenter son code ?

En programmation, le code est lu beaucoup plus souvent qu'il n'est écrit. Les commentaires servent à :

* **Expliquer le "pourquoi"** plutôt que le "comment" (le code montre déjà le "comment").
* **Aider à la collaboration** avec d'autres développeurs.
* **Se souvenir de sa propre logique** lorsqu'on relit un projet après plusieurs mois.

---

## 1. Les types de commentaires

### A. Le commentaire sur une seule ligne (`#`)

C'est la forme la plus courante. Tout ce qui suit le symbole `#` sur la même ligne est ignoré par l'interpréteur Python.

```python
# Voici un commentaire complet sur une ligne
vitesse = 100  # Commentaire de fin de ligne (inline)

```

### B. Les commentaires multi-lignes

Techniquement, Python n'a pas de syntaxe spécifique pour les commentaires multi-lignes. On utilise deux méthodes :

* **Répéter le symbole `#**` sur chaque ligne (méthode recommandée par le guide de style PEP 8).
* **Utiliser des chaînes de caractères triples** (`"""` ou `'''`). Bien qu'elles soient techniquement des chaînes de texte, si elles ne sont pas assignées à une variable, Python les ignore.

```python
# Ceci est un commentaire
# écrit sur plusieurs
# lignes de code.

"""
Ceci est souvent utilisé comme commentaire 
bloc, même si c'est techniquement une 
chaîne de caractères non assignée.
"""

```

## 2. Les meilleures pratiques (Le standard PEP 8)

* **Soyez concis :** Un commentaire ne doit pas expliquer une évidence.
* ❌ `x = x + 1 # Ajoute 1 à x` (Inutile)
* ✅ `x = x + 1 # Correction de l'index suite au décalage du header`


* **Gardez-les à jour :** Un commentaire erroné est pire qu'une absence de commentaire.
* **La langue :** En milieu professionnel, l'anglais est souvent privilégié, mais en apprentissage, utilisez la langue avec laquelle vous êtes le plus à l'aise.
* **Espace après le `#` :** Toujours mettre un espace entre le symbole et le premier caractère (ex: `# Commentaire` et non `#Commentaire`).

---

## 3. Astuce pour déboguer : "Commenter le code"

On utilise souvent les commentaires pour désactiver temporairement une partie du code sans la supprimer afin de tester une autre solution.

```python
# print("Ancienne méthode")
print("Nouvelle méthode")

```

