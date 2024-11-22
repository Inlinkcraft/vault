---
name: Queue
type: wiki
---
#wiki/cpp 

Application du principe de "First in, First out" sur une [[List]].

> [!Success] Avantage
> - Suppression à la fin se fait en $O(1)$
> - Inséré aux début se fait en $O(1)$
> - Accédé à la fin se fait en $O(1)$

>[!Fail] Désavantage
> - Aucun concept de position d'élément
> - On doit défiler pour accédé aux éléments suivants

### Implémentation
---
##### constructor

```cpp
#include <queue>
using std;

queue();     \\ Queue vide
```

##### Fonctions