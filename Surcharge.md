---
name: Surcharge
type: Matière
---
#GLO-2100 

La surcharge permet de redéfinir certaine fonction préalablement définie.

### Surcharge d'élément c++
---
#### Surcharge d'opérateur
---
##### Surcharge de l'opérateur d'incrémentation
###### Pré-incrémentation
La signature de l'opérateur pré-incrémentation est:
```c++
Class& operator++(Class&);
```
et sont comportement de base resemble à:
```c++
Class& operator++(Class&){
    ++i;
    return(*this); // Permet d'effectuer de opération à la chaine
}
```

> [!Info]
> Cet opérateur est a privilégier à l'opérateur post incrémentation, car celui-ci évite la copie

###### Post-incrémentation
La signature de l'opérateur post-incrémentation est:
```c++
Class operator++(Class&, int);
```
et sont comportement de base resemble à:
```c++
Class& operator++(Class&, int){ //int permet de les différentier
    Class temp = *this; // effectue une copie
    ++i;
    return temp;
}
```