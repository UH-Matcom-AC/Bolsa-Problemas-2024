# Producto Vectorial (Problema 54)

## Descripción

Sean $v, w \in \mathbb{R}^3$, se define como producto vectorial de $v$ y $w$ al número real $v \times w$ que se obtiene:
$$ \begin{bmatrix}
i & j & k \\
v_1 & v_2 & v_3 \\
w_1 & w_2 & w_3 
\end{bmatrix} $$
siendo $i, j, k$ los vectores unitarios de $\mathbb{R}^3$.

Dado $v, w \in \mathbb{R}^3$, calcule $v \times w$.

### Salida

Debe imprimir cada componente del producto vectorial de $v$ y $w$, separada por comas.

Por ejemplo: Si $v = (2,0,1)$ y $w = (1,-1,3)$

Debería imprimir:

> 1,-5,-2 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $v_1$
- $w_1$ : $v_2$
- $w_2$ : $v_3$
- $w_3$ : $w_1$
- $w_4$ : $w_2$
- $w_5$ : $w_3$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `v` : un array de 3 números de tamaño `dw` que representan las componentes de $v$
- `w` : un array de 3 números de tamaño `dw` que representan las componentes de $w$

Por ejemplo, un posible encabezado podría ser:

```
section .data
v dw 2, 0, 1
w dw 1, -1, 3
```
