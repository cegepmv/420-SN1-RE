+++
title = "Règles & conventions"
type = "chapter"
weight = 4
+++
---

## 1. L'Indentation et la Mise en Page

C'est la base visuelle du langage.
    
* **Espaces, pas de tabulations :** Utilise toujours **4 espaces** par niveau d'indentation (Un tab normal).
* **Longueur de ligne :** Limite tes lignes à un maximum de **79 caractères**. Cela permet d'ouvrir deux fichiers côte à côte sans scroller horizontalement.
* **Lignes vides :** * Sépare les fonctions et les classes de haut niveau par **deux lignes vides**.
* Sépare les méthodes à l'intérieur d'une classe par **une seule ligne vide**.



## 2. Les Espaces Blancs (Le "Bruit" Visuel)

Évite de surcharger ton code d'espaces inutiles :

* **Autour des opérateurs :** Mets un espace avant et après les opérateurs de comparaison (`==`, `!=`, `<`, `>`) et les affectations (`=`).
* *Correct :* `x = 5`
* *Incorrect :* `x=5`


* **Arguments de fonction :** Ne mets **pas** d'espaces autour du signe `=` quand tu définis une valeur par défaut dans une fonction.
* *Correct :* `def ma_fonction(name="Jean"):`


* **Parenthèses et crochets :** Pas d'espaces juste après une parenthèse ouvrante ou avant une fermante.
* *Correct :* `ma_liste[1]` (pas `ma_liste[ 1 ]`).



## 3. Conventions de Nommage (Le "Naming")

C'est ici que l'on reconnaît un développeur Python aguerri :

| Type | Style | Exemple |
| --- | --- | --- |
| **Variables / Fonctions** | `snake_case` (minuscules et underscores) | `ma_variable`, `calculer_total()` |
| **Classes** | `PascalCase` (majuscule à chaque mot) | `UtilisateurProfil`, `MaClasse` |
| **Constantes** | `UPPER_CASE` (tout en majuscules) | `PI_VALEUR`, `MAX_TENTATIVES` |
| **Privé (interne)** | Un underscore au début | `_variable_interne` |

## 4. Les Imports

Ils doivent toujours être placés en haut du fichier, juste après les commentaires de docstring.

* **Un par ligne :** * *Correct :* `python import os import sys `
* *Incorrect :* `import os, sys`


* **Ordre spécifique :**
1. Bibliothèques standards (ex: `os`, `json`).
2. Bibliothèques tierces (ex: `pandas`, `requests`).
3. Imports locaux (tes propres modules).



---

### Pourquoi s'embêter ?

Suivre la PEP 8 rend ton code immédiatement plus professionnel. Si tu travailles en équipe ou sur un projet open-source, c'est le ticket d'entrée indispensable.

