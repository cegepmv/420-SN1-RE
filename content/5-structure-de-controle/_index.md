+++
title = "Structure De Controle"
type = "chapter"
draft = false
weight = 13
+++

Jusqu'à présent, vos programmes Python étaient **linéaires** : l'ordinateur exécutait la ligne 1, puis la 2, puis la 3, du haut vers le bas, sans jamais se poser de questions.

En sciences, la réalité est rarement linéaire. Les **structures de contrôle** permettent de modifier ce trajet.

## 1.1 Qu'est-ce qu'une structure de contrôle ?

Imaginez que vous programmez un robot qui doit analyser des échantillons d'eau. 
Il y a deux façons principales de briser la ligne droite :

### A. La Condition (L'Aiguillage)
C'est le **"SI ... ALORS"**. Le programme arrive à une intersection et doit prendre une décision basée sur une mesure.
* *Exemple :* **SI** la température est > 100°C, **ALORS** affiche "Vapeur", **SINON** affiche "Liquide/Solide".



### B. La Boucle (La Répétition)
C'est le **"TANT QUE"** ou le **"POUR CHAQUE"**. Le programme répète une action plusieurs fois pour nous éviter de copier-coller le code.
* *Exemple :* **POUR CHAQUE** cellule dans cette boîte de Pétri, calcule sa surface.



## 1.2 Pourquoi est-ce essentiel pour un scientifique ?

Sans ces structures, l'informatique ne serait qu'une calculatrice de luxe. Grâce à elles, on peut :
1. **Filtrer des données :** Ignorer les mesures aberrantes (ex: un capteur qui donne -999).
2. **Automatiser l'analyse :** Traiter 10 000 points de données en une milliseconde.
3. **Simuler des systèmes :** Faire évoluer une population de bactéries heure par heure jusqu'à ce qu'elle atteigne une certaine taille.

> **En résumé :** > * Les **conditions** servent à décider.
> * Les **boucles** servent à répéter.