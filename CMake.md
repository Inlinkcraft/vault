---
name: CMake
type: wiki
---
#GLO-2100 

### Setup initial
---
Pour initialiser un project avec cmake.
1. Créé un fichier nommer exactement `CMakeLists.txt`
2. Écrire ce qui suit dans le fichier
```c
# CMakeLists.txt

cmake_minimum_require(VERSION 3.10)

project(nom_du_projet)

add_executable(nom_executable main.cpp autre_fichier.cpp)

```