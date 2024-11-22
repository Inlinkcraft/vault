---
name: Vector
type: wiki
---
#wiki/cpp 

Représentation informatique d'un [[Vecteur|vecteur]] en C++. Chaque élément d'un vecteur à une position.

> [!Success] Avantage
> - Accès d'une position $x$ en $O(1)$

> [!Warning] À prendre en note
> - Contiguë en mémoire
> - Suppression de l'élément à la position $x$ en $O(n)$
> - Insertion de l'élément à la position $x$ en $O(n)$

>[!Fail] Désavantage
> - Modification dynamique de la taille est couteux

### Implémentation
---
##### constructor

```cpp
#include <vector>
using std;

vector();     \\ Vecteur vide
vector(n);    \\ Vecteur à n élément
vector(n, a); \\ Vecteur à n copy de a
```

##### Fonctions

`resize(n)`: Permet de redimensionné le vecteur