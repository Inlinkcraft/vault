---
name: List
type: wiki
---
#wiki/cpp 

Représentation informatique d'une liste en C++.

> [!Success] Avantage
> - Suppression à la position courante se fait en $O(1)$
> - Inséré à la position courante se fait en $O(1)$
> - Accédé à la position suivante se fait en $O(1)$
> - Accédé à la position précédente se fait en $O(1)$

> [!Warning] À prendre en note
> - Accédé à une position $x$ se fait en $O(n)$

>[!Fail] Désavantage
> - Aucun concept de position d'élément

### Implémentation
---
##### constructor

```cpp
#include <list>
using std;

list();     \\ Liste vide
```

##### Fonctions