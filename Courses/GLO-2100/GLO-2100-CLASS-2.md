---
name: Cours-2
type: Class
course: GLO-2100
date: 2024-09-06T10:30
status: "Compléter"
---
#school/GLO-2100 
***

# Introduction à la compilation
Pour compiler des fichier c++ en version longue il suffit de faire les étape suivante
```
c++ fichier.cpp -E fichier.i        # Préprocessing
c++ fichier.i -S fichier.s          # Compilation
c++ fichier.s -c fichier.o          # Objet
c++ fichier.o -o nomDuProgram.exe   # Executable
```

Version "plus rapide"
```
c++ fichier.cpp -o nomDuProgram.exe   # Executable
```

## Flag de compilation
Lors de la compilation il est possible de spécifier des [[Flag de compilation|flag de compilation]] qui aide a optimiser le code et le rendre plus rapide.

# CMAKE
![[CMake]]