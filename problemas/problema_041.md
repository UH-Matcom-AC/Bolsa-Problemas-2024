# Suma de matrices (Problema 41)

## Descripción

Una matriz de dimensiones $(n,m)$, no es más que un espacio en memoria contiguo de $n \cdot m$ elementos. Sin embargo pudieran existir varias formas de guardar una matriz. Si se ve como una cuadrícula de $n$ filas y $m$ columnas, entonces la matriz se dispone en memoria almacenando desde la primera fila, hasta la última.

Asumiremos que la indización comienza en $0$, es decir, la posición $(1,4)$ corresponde al elemento de la segunda fila y quinta columna.

Dada dos matrice $A_1$ y $A_2$ de dimensiones $(n,m)$, halle $B = A_1 + A_2 $.

### Salida

Debe imprimir $B$. Para ello cada fila debe ir separada por saltos de línea, y cada elemento separado por comas.

Por ejemplo: si $B= \begin{bmatrix}
0 & 1 \\
2 & 3 
\end{bmatrix}$ y $k = 2$

Debería imprimir:

> 0 2  
> 4 6

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$
- $w_1$ : $m$
- $w_{2:n*m+1}$ : $A_1$
- $w_{n*m+2: 2n*m+2}$: $A_2$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `m` : un número de tamaño `dw` que representa $m$
- `A_1` : un array de números de tamaño `dw` que representa $A$
- `A_2` : un array de números de tamaño `dw` que representa $A_2$


Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 2
m dd 2
A_1 dw 0,1,2,3
A_2 dw 4,5,6,7
```