---
name: Manipulation de circuit à domaine de Laplace
type: Matière
---
#GEL-1000 
***
Les calculs dans le domaine de $s$ ([[Transformation de Laplace|Laplace]]) se font comme pour les [[Circuit électrique|circuits]] résistifs dans l'espace temps.
([[Chapitre-6.pdf#page=53&selection=68,0,69,43&color=yellow|Chapitre-6, p.53]])

### Selon les Impédance
---
Si la résolution se fait avec l'[[Impédance|impédance]] des [[Composante transformer en domaine Laplace|composante]] nous suivons les règle [[Résistance électrique|résistive]]:
##### Équivalent série
$$Z_{eq}(s) = Z_{1}(s) + Z_{2}(s) + \dots + Z_{N}(s) $$

##### Équivalent parallèle
$$\frac{1}{Z_{eq}(s)} = \frac{1}{Z_{1}(s)} + \frac{1}{Z_{2}(s)} + \dots + \frac{1}{Z_{N}(s)} $$

##### Diviseur de tension
$$V_{n}(s) = \frac{Z_{n}(s)}{Z_{1}(s)+Z_{2}(s)+ \dots + Z_{N}(s)} V(s) $$
[[Chapitre-6.pdf#page=54&selection=0,37,0,37&color=yellow|Chapitre-6, p.54]]

##### Diviseur de courant
$$I_{n}(s) = \frac{\frac{1}{Z_{n}(s)}}{\frac{1}{Z_{1}(s)}+\frac{1}{Z_{2}(s)}+ \dots + \frac{1}{Z_{N}(s)}} I(s) $$
[[Chapitre-6.pdf#page=55&selection=0,37,0,37&color=yellow|Chapitre-6, p.55]]


### Selon les Admittance
---
Si la résolution se fait avec l'[[Admittance|admittance]] des [[Composante transformer en domaine Laplace|composante]] nous suivons les règle [[Conductance|conductrice]]:
##### Équivalent série
$$\frac{1}{Y_{eq}(s)} = \frac{1}{Y_{1}(s)} + \frac{1}{Y_{2}(s)} + \dots + \frac{1}{Y_{N}(s)} $$

##### Équivalent parallèle
$$Y_{eq}(s) = Y_{1}(s) + Y_{2}(s) + \dots + Y_{N}(s) $$

##### Diviseur de tension
$$V_{n}(s) = \frac{\frac{1}{Y_{n}(s)}}{\frac{1}{Y_{1}(s)}+\frac{1}{Y_{2}(s)}+ \dots + \frac{1}{Y_{N}(s)}} V(s) $$
[[Chapitre-6.pdf#page=54&selection=0,37,0,37&color=yellow|Chapitre-6, p.54]]

##### Diviseur de courant
$$I_{n}(s) = \frac{Y_{n}(s)}{Y_{1}(s)+Y_{2}(s)+ \dots + Y_{N}(s)} I(s) $$
[[Chapitre-6.pdf#page=55&selection=0,37,0,37&color=yellow|Chapitre-6, p.55]]

