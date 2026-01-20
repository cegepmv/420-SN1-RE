+++
date = '2025-08-28T21:15:14-04:00'
title = 'VSCode'
weight = 13
+++


## Installation

[Lien d'instalation](https://code.visualstudio.com/Download)


### Installation des extensions

1. Ouvrez la barre latérale de gauche dans VSCode.
2. Cliquez sur l'icône des extensions ![alt text](/420-SN1-RE/images/extensions.png) ou utilisez le raccourci clavier `Ctrl + Shift + X`.
3. Recherchez **Python** et installez l’extension.

---

## Fonctionnalités essentielles

Visual Studio Code n'est pas qu'un simple éditeur de texte ; c'est un environnement de développement complet (IDE) qui s'adapte à tes besoins grâce à ses différents outils.

### Configuration

Il est très pratique d'activer la sauvegarde automatique afin de ne plus jamais perdre du travail. Allez dans Fichier et cliquez sur sauvegarde automatique.

### 🔌 Les Extensions

C'est la force principale de VSCode. De base, le logiciel est léger, mais tu peux ajouter des fonctionnalités pour n'importe quel langage (Python, C++, Java, etc.).

* **À quoi ça sert ?** Ajouter la coloration syntaxique, l'auto-complétion intelligente (IntelliSense), ou des thèmes visuels.
* **Astuce :** Ne surcharge pas ton éditeur ! Installe uniquement ce dont tu as réellement besoin pour tes projets actuels.

### 📂 Gestion des Projets

Dans VSCode, on ne travaille pas sur un "fichier" isolé, mais sur un **Dossier**.

* Utilise `Fichier > Ouvrir le dossier...` pour charger tout ton répertoire de travail.
* Cela permet d'avoir la vue sur tous tes fichiers dans la barre latérale de gauche (Explorateur) et de faciliter la navigation entre eux.

### 💻 Le Terminal Intégré

Plus besoin de jongler entre VSCode et l'invite de commande de Windows ou le Terminal Mac.

* **Ouverture :** `Ctrl + \` `(ou`Terminal > Nouveau Terminal`).
* Il s'ouvre directement dans le dossier de ton projet, ce qui te permet de lancer tes scripts ou d'installer des bibliothèques sans changer de fenêtre.

### <img src="/420-SN1-RE/images/playBtn.png" style="vertical-align:middle;display:inline-block" /> Le "Play Button" (Run)

Situé en haut à droite, ce bouton permet de lancer ton code rapidement.

* Si tu as installé l'extension **Python**, cliquer sur le triangle lancera automatiquement ton script dans le terminal situé en bas.
* C'est la méthode la plus simple pour tester ton programme en un clic.

### 🐞 Le Debugger (Débogueur)

C'est l'outil le plus puissant pour corriger des erreurs complexes. Au lieu de mettre des `print()` partout, le debugger te permet de :

1. **Points d'arrêt (Breakpoints) :** Clique à gauche du numéro de ligne pour mettre un point rouge. Le code s'arrêtera pile à cet endroit.
2. **Inspection :** Tu peux voir la valeur de toutes tes variables à un instant précis.
3. **Pas à pas :** Avancer dans ton code ligne par ligne pour comprendre exactement où ça bloque.

*Nous verrons le débugger en détail plus tard*

---

# Racourci clavier utilie

### 🖱️ **Raccourcis de base**

| Action         | Windows/Linux | Mac             |
| -------------- | ------------- | --------------- |
| Copier         | **Ctrl + C**  | **Cmd (⌘) + C** |
| Coller         | **Ctrl + V**  | **Cmd (⌘) + V** |
| Annuler (Undo) | **Ctrl + Z**  | **Cmd (⌘) + Z** |

---

### 🔍 **Édition avancée**

| Action                                | Windows/Linux           | Mac                              |
| ------------------------------------- | ----------------------- | -------------------------------- |
| Sélectionner prochaine occurrence     | **Ctrl + D**            | **Cmd (⌘) + D**                  |
| Ajouter plusieurs curseurs (haut/bas) | **Ctrl + Alt + ↑ / ↓**  | **Option (⌥) + Cmd (⌘) + ↑ / ↓** |
| Copier ligne vers le haut ou le bas   | **Shift + Alt + ↑ / ↓** | **Shift + Option (⌥) + ↑ / ↓**   |
| Commenter rapidement des lignes       | **ctrl + é**            |                                  |

*Je n'ai pas testé la version Mac, les touches exactes peuvent changer en fonction du clavier que vous utilisez*

***Il est possible que ces raccourcis soient différents selon la configuration du clavier que vous utiliser, mais je vous assure que ces fonctions existent! Il vous suffi de les trouver.**

1. Surligner un String dont on oublié les `"`, faites le `"`et il s'ajoutera des deux côtés.

---
