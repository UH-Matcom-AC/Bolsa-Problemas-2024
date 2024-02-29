# Suma de Fracciones (Problema 14)

## Descripción

Sean dos fracciones $\frac{a}{b}$ y $\frac{c}{d}$, donde $a$, $b$, $c$ y $d$ son naturales con $b, d > 0$. Para sumar ambas fracciones se debe hallar primero las fracciones $\frac{x}{z}$ y $\frac{y}{z}$ tal que sean equivalentes a $\frac{a}{b}$ y $\frac{c}{d}$ respectivamente, y a su vez $z$ tenga el menor valor posible. Dadas las fracciones $\frac{a}{b}$ y $\frac{c}{d}$, hallar $\frac{x}{z}$ y $\frac{y}{z}$ tal que cumplan la condición anterior. Por ejemplo para $\frac{2}{6}$ y $\frac{3}{15}$, las fracciones buscadas son $\frac{10}{30}$ y $\frac{6}{30}$.

### Salida

Debe imprimir los valores de $x$, $y$, y $z$, separados por saltos de líneas

Por ejemplo: Para $a= 2$, $b = 6$, $c= 3$, y $d = 15$.

Debería imprimir:

> 10  
> 6  
> 30

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$
- $w_2$ : $c$
- $w_3$ : $d$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `dw` que representa $a$
- `b` : un número de tamaño `dw` que representa $b$
- `c` : un número de tamaño `dw` que representa $c$
- `d` : un número de tamaño `dw` que representa $d$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a dw 2
b dw 6
c dw 3
d dw 15
```
