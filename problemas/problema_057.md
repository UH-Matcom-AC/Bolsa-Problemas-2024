# Rotar Matriz (Problema 57)

## Descripción

Una matriz de dimensiones $(n,m)$, no es más que un espacio en memoria contiguo de $n \cdot m$ elementos. Sin embargo pudieran existir varias formas de guardar una matriz. Si se ve como una cuadrícula de $n$ filas y $m$ columnas, entonces la matriz se dispone en memoria almacenando desde la primera fila, hasta la última.

Asumiremos que la indización comienza en $0$, es decir, la posición $(1,4)$ corresponde al elemento de la segunda fila y quinta columna.

Sea una matriz $A$, se define la operación $r(A, k)$ (Rotar Matriz a la Derecha) como:
- $r(A, 0) = A$
- $r(A, 1) = B$ tal que $A[i,j] = B[j, n-i-1]$ donde $n$ es la cantidad de filas de $A$
- $r(A, k) = r(r(A, k-1), 1)$ con $k>1$.

Dada una matriz $A$ de dimensión $(n,m)$, y $k \ge 0$, halle $B = r(A,k)$.

### Salida

Debe imprimir $B$. Para ello cada fila debe ir separada por saltos de línea, y cada elemento separado por comas.

Por ejemplo: si $A= \begin{bmatrix}
0 & 1 \\
2 & 3 
\end{bmatrix}$ y $k = 2$

Debería imprimir:

> 3 2  
> 1 0

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$
- $w_1$ : $m$
- $w_{2:n*m+1}$ : $A$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `m` : un número de tamaño `dw` que representa $m$
- `A` : un array de números de tamaño `dw` que representa $A$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 2
m dd 2
A dw 0,1,2,3
```
