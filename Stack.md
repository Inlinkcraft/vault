---
name: Queue
type: wiki
---
#wiki/cpp 

Application du principe de "First in, Last out" sur une [[List]].

> [!Success] Avantage
> - Suppression au début se fait en $O(1)$
> - Inséré au début se fait en $O(1)$
> - Accédé au début se fait en $O(1)$

>[!Fail] Désavantage
> - Aucun concept de position d'élément
> - On doit déstacker pour accédé aux éléments suivants

### Implémentation
---
##### constructor

```cpp
#include <stack>
using std;

stack();     \\ Queue vide
```

##### Fonctions