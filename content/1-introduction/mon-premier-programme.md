+++
date = '2026-01-20T11:04:07-05:00'
title = 'Mon Premier Programme'
weight = 14
+++

---

## Créer votre premier script

Avant de tester les trois méthodes, créez un fichier nommé `bonjour.py` et écrivez la ligne suivante :

```python
print("Bonjour le monde!")

```

---

## 1. La méthode rapide : Le bouton Play <img src="/420-SN1-RE/images/playBtn.png" width="20" style="display:inline-block;vertical-align:middle">

C'est la méthode la plus simple pour les débutants.

* **Comment faire :** Cliquez sur l'icône de triangle en haut à droite de l'éditeur.
* **Ce qui se passe :** VSCode ouvre automatiquement le terminal, tape le chemin de Python et lance votre fichier.
* **Avantage :** Aucun risque de faire une faute de frappe dans la commande.

---

## 2. La méthode pro : Appeler le script via le Terminal

C'est ainsi que les développeurs lancent souvent leurs programmes pour passer des paramètres ou tester des environnements précis.

* **Comment faire :**
1. Ouvrez le terminal.
2. Tapez la commande suivante : `python3 bonjour.py`
3. Appuyez sur **Entrée**.


* **Avantage :** Vous apprenez à utiliser la ligne de commande, ce qui est essentiel pour la suite du cours.

---

## 3. La méthode interactive : Directement dans le Terminal (REPL)

Parfois, on ne veut pas créer de fichier, on veut juste tester une ou deux lignes de code rapidement. On appelle cela le mode **REPL** (Read-Eval-Print Loop).

* **Comment faire :**
1. Dans le terminal, tapez simplement `python3` et faites **Entrée**.
2. Vous verrez apparaître des chevrons `>>>`. Vous êtes maintenant "dans" Python.
3. Tapez `print("Test")` et faites **Entrée**. Le résultat s'affiche immédiatement.


* **Comment quitter :** Tapez `exit()`.
* **Avantage :** Parfait pour tester des calculs mathématiques ou le comportement d'une fonction sans polluer votre projet de fichiers temporaires.

---

### ⚠️ Erreur commune

Si vous tapez `python3 bonjour.py` et que vous recevez un message d'erreur disant que le fichier n'existe pas, vérifiez que vous avez bien **ouvert le dossier** de votre projet dans VSCode. Le terminal doit être situé au même endroit que votre fichier. 

