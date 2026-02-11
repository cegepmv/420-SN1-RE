+++
date = '2026-02-11T07:08:17-05:00'
title = 'Boucles For'
weight = 4
+++

## 6. La boucle `for` : Automatiser la répétition

La boucle `for` est utilisée lorsque vous savez exactement combien de fois une opération doit être répétée. C'est l'outil parfait pour traiter des séries de données ou simuler des étapes temporelles fixes.

### L'outil `range()` : Le générateur de pas
Pour dire à Python combien de fois boucler, on utilise souvent la fonction `range()`. Elle crée une séquence de nombres qui sert de guide à la boucle.

* `range(5)` : Génère 5 étapes (de 0 à 4).
* `range(1, 11)` : Génère 10 étapes (de 1 à 10).


### Exemple 1 : Calcul de croissance

Voici comment on écrit le script pour calculer l'évolution d'une population sur 10 jours. Remarquez bien les deux-points et le décalage (indentation) du `print` et du calcul.

```python
population = 100
taux_croissance = 1.05  # +5% par jour

for jour in range(10):
    population = population * taux_croissance
    print(f"Jour {jour} : {population:.2f} individus")
```

- for jour in range(10): : Signifie "Répète l'action 10 fois". La variable jour prendra les valeurs de 0 à 9.

- L'indentation : Les deux lignes sous le for sont décalées. C'est ce qui indique à Python qu'elles font partie de la boucle.

- Mise à jour : À chaque tour, la variable population change de valeur et cette nouvelle valeur est utilisée au tour suivant.

-  La variable jour est créée automatiquement par la boucle. Vous n'avez pas besoin de la définir avant. Elle sert de "compteur" interne.

### Exemple 2: Calcul de somme

Admettons qu'on observe la série géométrique suivante: 

{{< math >}}
$$ S_{100} = \sum_{k=0}^{100} \left( \frac{1}{2} \right)^k = 1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots $$
{{< /math >}}

Il est possible de la transformer en un programme python: 

```python
somme = 0
raison = 0.5
terme = 1  # C'est (1/2)^0
n_etapes = 100

for k in range(n_etapes):
    somme += terme
    terme *= raison  # On prépare le prochain terme : (1/2)^(k+1)
print(f"Somme = {somme}")
```

### Analogie : La croissance bactérienne
Imaginez une population de bactéries qui double à chaque heure. Si vous voulez connaître l'évolution de la population sur une période de 24 heures, vous n'allez pas écrire 24 fois le calcul. Vous utilisez une boucle `for` qui va répéter l'opération pour chaque heure comprise dans le `range(24)`.



### Pourquoi utiliser `for` plutôt que de copier le code ?
1. **Évite les erreurs :** Moins de lignes de code signifie moins de risques d'erreurs de frappe.
2. **Flexibilité :** Si vous décidez de simuler 100 heures au lieu de 24, il suffit de changer un chiffre dans le `range()`.
3. **Traitement de masse :** C'est ainsi que l'on traite des fichiers contenant des milliers de mesures expérimentales.

### Le fonctionnement interne
À chaque passage dans la boucle (chaque "itération"), une variable (souvent appelée `i`, `t` ou `n`) prend la valeur suivante de la séquence fournie par le `range()`. 

> **Important :** Comme pour les conditions, tout le code qui doit être répété **doit être indenté**. Dès que vous revenez vers la gauche, vous sortez de la boucle.

---

**Défi de réflexion :**
Si vous utilisez `range(0, 10)`, est-ce que le chiffre 10 est inclus dans le calcul ? Pourquoi est-ce que les informaticiens commencent souvent à compter à 0 plutôt qu'à 1 ?