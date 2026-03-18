+++
date = '2026-03-18T16:11:58-04:00'
title = 'Comprehension_liste'
weight = 7
+++

## 12. Les Compréhensions de listes : Puissance et Statistiques (matière avancée)

La compréhension de liste est la manière "experte" de créer des listes en Python. Elle permet de transformer une séquence en une seule ligne, en suivant une logique qui ressemble beaucoup à la notation mathématique des ensembles :

{{< math >}}
$$S = \{ f(x) \mid x \in \text{Données} \}$$
{{< /math >}}

En mots simples, on transforme chaque donnée dans la collection avec la même règle et on en fait une nouvelle collection.

### L'exemple concret : Le Bootstrapping
En statistiques, le **Bootstrap** consiste à créer plusieurs sous-échantillons à partir d'un échantillon original pour estimer la variabilité d'une mesure (comme la moyenne).

#### 1. Préparation des données
Imaginons que nous avons 10 mesures de tension artérielle.

```python
import random

# Nos données originales (n=10)
mesures = [120, 118, 122, 140, 135, 128, 115, 121, 132, 126]
```

#### 2. Génération des sous-échantillons
On crée des sous-échantillons en pigeant avec remise dans les mesures.

```python
# On veut 1000 échantillons de taille 10 (avec remise)
n_boot = 1000

# LA MAGIE : On crée une liste de listes
subsamples = [random.choices(mesures, k=len(mesures)) for _ in range(n_boot)]
```

#### 3. Calcul des moyennes
On peut voir tous les 1000 sous-échantillons comme une belle approximation de la distribution des échantillons et en tirer des statistiques.

```python
# Encore une compréhension de liste !
moyennes_boot = [sum(s) / len(s) for s in subsamples]

# On peut maintenant estimer l'erreur type ou l'intervalle de confiance
print(f"Moyenne globale : {sum(moyennes_boot)/n_boot:.2f}")
print(f"Moyenne min/max observée : {min(moyennes_boot)} / {max(moyennes_boot)}")
```

### 4. L'Intervalle de Confiance (IC) à 95%

Maintenant que nous avons 1000 moyennes simulées dans notre liste `moyennes_boot`, comment savoir si notre estimation est fiable ? 

On va utiliser la méthode des **percentiles** : on trie nos 1000 moyennes et on regarde où se situent les 2.5% les plus bas et les 2.5% les plus hauts. Ce qui reste au milieu est notre intervalle de confiance à 95%.



```python
# 1. Trier la liste des moyennes
moyennes_boot.sort()

# 2. Trouver les indices pour 2.5% et 97.5%
# (Pour 1000 moyennes, ce sont les positions 25 et 975)
ic_bas = moyennes_boot[24]
ic_haut = moyennes_boot[974]

print(f"La moyenne réelle de la population se situe probablement entre :")
print(f"[{ic_bas:.2f} , {ic_haut:.2f}] avec une confiance de 95%.")
```