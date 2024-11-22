---
name: Indépendance probabiliste
type: Matière
---
#STT-2920

On dit que les [[Événement|événement]] A et B sont indépendants si le fait de savoir qu’un des deux [[Événement|événement]] s’est produit n’influence pas la probabilité de l’autre.

### Définition mathématique
---
En utilisant la [[Probabilité conditionnel|probabilité conditionnel]], il est possible de d'écrire l'indépendance comme suit:
$$\mathbb{P}[A|B] = \mathbb{P}[A] \Longleftrightarrow \mathbb{P}[B|A] = \mathbb{P}[B]$$

>[!Info]
>Une seul des deux équation se doit d'être vrai pour validé l'indépendance

Une meilleur définition mathématique est la suivante:
$$\mathbb{P}[A \cap B] = \mathbb{P}[A]\mathbb{P}[B]$$
$$\mathbb{P}[B_{j_{1}} \cap B_{j_{2}}\cap B_{j_{3}} \cap \dots \cap B_{j_{k}}] = \mathbb{P}[B_{j_{1}}]\mathbb{P}[B_{j_{2}}]\mathbb{P}[B_{j_{3}}]\dots\mathbb{P}[B_{j_{k}}]$$

##### [[Cas discret]]
En [[Cas discret|cas discret]] cette definition s'applique:
$$p(x, y) = p_{X}(x)p_{Y}(y)$$

##### [[Cas continue]]
En [[Cas continue|cas continue]] cette definition s'applique:
$$f(x, y) = f_{X}(x)f_{Y}(y)$$

##### [[Fonction de répartition]]
L'indépendance peut aussi être appliqué a la [[Fonction de répartition|fonction de répartition]]:
$$F(x, y) = F_{X}(x)F_{Y}(y)$$

##### [[Espérance]]
L'indépendance peut aussi être appliqué a l'[[Espérance]]:
$$\mathbb{E}[x, y] = \mathbb{E}[x]\mathbb{E}[y]$$

### Préservation de l'indépendance
---
Un [[Événement|événement]] composé d'[[Événement|événement]] indépendant resteras indépendant