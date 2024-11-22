---
name: Récursivité
type: Matière
---
#GLO-2100 

La [[Récursivité|récursivité]] est l'action en programmation d'appeler la fonction dans elle-même. Cela permet d'effectuer des [[Algorithme|algorithme]] à nature recursive plus facilement.

### Avantage et désavantage
---
#### Avantage
- Le code est compacte et clair
- Execution naturel de l'[[Algorithme|algorithme]] récursif.

#### Désavantage
- Utilise une grande quantité de mémoire
- Longue execution
- Difficile d’estimer les impacte

### Implémentation typique
---
```cpp
voif recursif() {
    if(runaway){
        throw error;
    }
    if(done){
        return answer;
    }
    recursif();
}
```

>[!Attention]
>Jamais dupliquer le travail dans un appel. Ex: (Fibo)