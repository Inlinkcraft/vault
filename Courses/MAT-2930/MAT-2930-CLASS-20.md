---
name: Cours-20
type: Class
course: MAT-2930
date: 2024-11-25T11:30
status: "Cette semaine"
---
#school/MAT-2930
***
# Avant le cour
## Plan de cours
- [[MAT-2930-CHAPITER-5]]: Factorisation $QR$

## Todo
- 

---
# Matière abordée

- 

## Notes supplémentaire

##### Atelier
- Traitement d'Image
	- Loader un image `im1 = imageio.imread(path)`
	- Une image en python est une array
		- [width, height, color]
		- `plt.imshow(img)` Pour afficher une Image
			- `cmap= "Couleur"` Pour changer la couleur
			- `cmap="hsv"` permet de voir l'image avec une saturation/value max
		- `plt.axis('off')` Pour enlever les axe
	- $\begin{bmatrix}C \\ M \\ Y\end{bmatrix} = \begin{bmatrix}1 \\ 1 \\ 1{}\end{bmatrix} - \begin{bmatrix}R \\ G \\B\end{bmatrix}$
	- `hsv = cv2.cvtColor(im, cv2.COLOR_RGB2HSV)` convertie la couleur en nouveau codage
		- `COLOR_RGB2GRAY`
		- `COLOR_RGB2RGBA`
	- `im = cv2.resize(img, (0, 0), fx=1/4, fy=1/4)` Change la taille de l'image


---
# En retrospective



