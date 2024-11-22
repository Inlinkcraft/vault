---
name: Class
type: Matière
---
#GLO-2100

Une classe est un regroupement de valeur et fonction afin de décrire un objet qui seras utilisé a différent hessian dans le code.

#TODO ajouter la matière connue

### Constructeur de base
---
Le constructeur de base permet de créé l'objet basé sur les différent paramètre donné à l'objet
```cpp
Class(int a, int b, ...);
```

### La règle des 3 copilien
---
#### Constructeur de copie
Le constructeur copie permet comme sont nom l'indique de copier l'objet en profondeur. Sa syntax resemble à:
```c++
Class( const Class& );
```

#### Surcharge de l'oppérateur copie
L'opérateur copie permet comme le constructeur copies de créé un objet identique complétement indépendant. Sa syntaxe resemble à:
```cpp
Class& operator=(const Class& x);
```

#### Destructeur
Le destructeur permet de libéré la mémoire que l'objet utilise. C'est à dire qu'il doit s'assuré d'éliminer tous les objet qui était utilisé seulement pas celui-ci. Sa syntaxe resemble à:
```cpp
~Class();
```

#### La règle des 5 copilien
La règle des 3 copilien peut être développer en ajoutant 2 copilien supplémentaire:
##### Constructeur déplacement
Le constructeur de déplacement permet de déplacer un objet d'une adresse à l'autre sans être copier. De plus l'opjet initial doit rester valide mais dans un état indéfinie. Sa syntaxe ressemble à:
```cpp
Class(Class&& other);
```

##### Surcharge de l'opérateur déplacement
L'opérateur de déplacement permet de déplacer un objet d'une adresse à l'autre comme le constructeur de déplacement. Sa syntaxe ressemble à:
```cpp
Class& operator=(Class&& other);
```