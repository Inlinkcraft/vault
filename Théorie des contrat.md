---
name: Théorie des contrat
type: Matière
---
#GLO-2100 

La théorie des contrat est la pratique qui consiste à écrire des contrat..

### En programmation
---
En programmation la théorie des contrat consiste à s'assuré que les donné entré dans une fonction sont valide et le résultat de la fonction est valide. C'est à dire que le programmeur d'un module a le contrat de retourner des valeur valide dans le cas que le client respecte sont contrat qui est de donnée des valeurs valide.

```c++
void func(par a, par b){
    PRECONDITION(a.valide); // Validation de a
    PRECONDITION(b.valide); // Validation de b
    
    // Code
    
    POSTCONDITION(a.valide); // Validation de a
    POSTCONDITION(b.valide); // Validation de b
    POSTCONDITION(resultat.valide) // Validation du resultat
}
```