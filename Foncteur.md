---
name: Foncteur
type: Matière
---
#GLO-2100 

Un foncteur est une [[Class|class]] qui englobe une [[Fonction|fonction]]. Cela permet d'ajouter des attribue a la [[Fonction|fonction]].

+ Maintenable

### Syntaxe
---
>[!code-family]- C++
>```cpp
>class Foncteur {
>public:
>    int operator()(int a, int b)
>    {
>        return a < b;
>    }
>}
>```
> Il suffit d'écrasé la déclaration de l'opérateur `()`.

### Utilisation du foncteur sort
---
Le foncteur sort fonctionne comme suit:
>[!code-family]- C++
>```c++
>std::sort(begin(v), end(v)); //foncteur par default
>std::sort(begin(v), end(v), foncteur); //foncteur personnalisé
>```
