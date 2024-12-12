---
name: Tp5
type: Evaluation
course: GEL-1000
date: 2024-12-13T23:59
ponderation: 2
note:
status: En cours
---
#school/GEL-1000  

```circuitjs
$ 1 0.000005 1.3241202019156522 67 5 50 5e-11
a 656 320 816 320 8 15 -15 1000000 0.0000053447376156734696 0 100000
r 544 224 544 304 0 10000
r 656 304 544 304 0 20000
r 544 304 448 304 0 10000
c 656 304 656 224 4 1e-8 0.5344791063049626 0.001 0
c 544 304 544 400 4 5e-7 -0.09823166664547447 0.001 0
g 448 400 448 416 0 0
g 544 400 544 416 0 0
g 656 400 656 416 0 0
g 816 400 816 416 0 0
w 544 224 656 224 0
w 656 224 816 224 0
w 816 224 816 320 0
w 656 336 656 400 0
r 816 320 816 400 0 1000000000
v 448 400 448 304 0 1 500 5 0 0 0.5
o 14 2 0 4099 2.5 0.00009765625 0 2 14 3
```
$$V_{out1}\left(t\right)=\frac{\left(-15e^{250t}+\sqrt{15}\sin\left(250\sqrt{15}t\right)+15\cos\left(250\sqrt{15}t\right)\right)e^{-250t}}{3}u(t)$$
$$V_{out2}\left(t\right)=\frac{2\left(-\sqrt{15}\pi\left(-7\sin\left(250\sqrt{15}t\right)+8\pi^{2}\sin\left(250\sqrt{15}t\right)+\sqrt{15}\cos\left(250\sqrt{15}t\right)\right)+15\left(-2\sin\left(1000\pi t\right)+2\pi^{2}\sin\left(1000\pi t\right)+\pi\cos\left(1000\pi t\right)\right)e^{250t}\right)e^{-250t}}{3\left(-7\pi^{2}+4+4\pi^{4}\right)}u(t)$$