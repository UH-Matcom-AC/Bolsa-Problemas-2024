# Múltiplicación de Matriz y Vector(Problema 39)

## Descripción

Una matriz de dimensiones $(n,m)$, no es más que un espacio en memoria contiguo de $n \cdot m$ elementos. Sin embargo pudieran existir varias formas de guardar una matriz. Si se ve como una cuadrícula de $n$ filas y $m$ columnas, entonces la matriz se dispone en memoria almacenando desde la primera fila, hasta la última.

Asumiremos que la indización comienza en $0$, es decir, la posición $(1,4)$ corresponde al elemento de la segunda fila y quinta columna.

Sea una matriz $A$ y un vector $V$, se quiere el resultado de la operación $A*V=B$

### Salida

Se imprimir $B$. Para ello cada elemento debe ir separada por saltos de línea.

Por ejemplo: si  $B = (1,2,3,4)$

Debería imprimir:

> 1
> 2
> 3
> 4

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$
- $w_1$ : $m$
- $w_{2:n*m+1}$ : $A$
- $w_{n*m+1,n*m+1+m}$: $V$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `m` : un número de tamaño `dw` que representa $m$
- `A` : un array de números de tamaño `dw` que representa $A$
- `V` : un array de números de tamaño `dw` que representa $V$
Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 2
m dd 2
A dw 0,1,2,3
V dw 4,5
```