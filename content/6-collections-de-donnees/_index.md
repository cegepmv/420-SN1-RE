+++
title = "Collections De Donnees"
type = "chapter"
draft = false
weight = 14
+++
## Pourquoi ne pas simplement utiliser des variables ?

Jusqu'à présent, nous avons manipulé des données isolées : un âge, une température, un nom. En programmation réelle, on traite rarement les données une par une. On manipule des **groupes** de données.

Imaginez que vous gérez un capteur qui prend une mesure par seconde. Au bout d'une heure, vous avez 3600 variables. Créer `mesure1`, `mesure2`, ... `mesure3600` est impossible.

### Les trois piliers des collections en Python

Dans ce chapitre, nous allons explorer comment Python structure l'information pour nous faciliter la vie :

1.  **Les Listes :** Pour stocker des suites d'éléments ordonnés (comme une file d'attente ou une série chronologique).
2.  **Les Dictionnaires :** Pour créer des relations "Clé ↔️ Valeur" (comme un annuaire ou un fichier de configuration).
3.  **L'Itération efficace :** Comment passer au travers de ces structures sans écrire 50 lignes de code.



### L'objectif pédagogique
L'idée n'est pas de devenir une encyclopédie vivante de la documentation Python, mais de comprendre **quelle structure choisir** selon le problème à résoudre. 

* *Besoin d'un historique de prix ?* **Liste.**
* *Besoin de stocker le profil d'un utilisateur ?* **Dictionnaire.**
* *Besoin de transformer 1000 données d'un coup ?* **Compréhension de liste.**