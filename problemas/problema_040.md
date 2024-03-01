# Múltiplicación de Vectores(Problema 39)

## Descripción

Una vector de dimensiones $n$, no es más que un espacio en memoria contiguo de $n$ elementos. Una forma común de representar vectores es usando array. 
Sean dos vectores $V_1$ y $V_2$, de dimensiones $n$ y $m$ respectivamente. Se quiere  la matriz $M$ de $(n,m)$ que se obtiene al multiplicar  el vector columna $V_1^{T}$ de dimensión $(n,1)$ por el vector fila $V_2$ de dimensión $(1,m)$. El procedimiento a realizar es el mismo que si se estuvieran multiplicando matrices.

### Salida

Se desea imprimir $B$. Para ello cada elemento debe ir separada por saltos de línea.

Por ejemplo: si es $B= \begin{bmatrix}
0 & 1 \\
2 & 3 
\end{bmatrix}$

Debería imprimir:

> 0 1 
> 2 3


## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$
- $w_{1:n}$ : $V_1$
- $w_{n+1}$ : $m$
- $w_{n+2:n+m+2}$ : $V_2$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `m` : un número de tamaño `dw` que representa $m$
- `V_1` : un array de números de tamaño `dw` que representa $V_1$
- `V_2` : un array de números de tamaño `dw` que representa $V_2$
Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 2
m dd 2
V_1 dw 0,1
V_2 dw 2,3
```