# Sumando y obteniendo x (Problema 29)

## Descripción

Dada una lista $L$ ordenada con $n$ elementos $a_1, a_2, \ldots, a_n$ y un número $x$. De existir $a_i > 0$ y $a_j > 0$ tal que $a_i + a_j = x$ devolver los índices $i,j$ en caso contrario devolver $|L|+1$

### Salida

Para la salida debe imprimir los índices $i$ y $j$ separados por espacio o $|L| + 1$.

Por ejemplo: para $L = [3, 4, 4, 6]$ y $x=9$ debería imprimir:

> 0 3

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $x$
- $w_1$: $n$ (tamaño de la lista $L$)
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `x` : un número de tamaño `db` que representa $x$
- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
x db 5
n dd 4
array db 4, 3, 4, 6
```