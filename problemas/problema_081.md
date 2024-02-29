# Máximos por intervalos (Problema 81)

## Descripción

Se tiene una lista $L$ de tamaño $n$ con números enteros. Construya la lista $L^\prime$ tal que
$$L^\prime[i]= \max_{j=0}^i L[j]$$
con $i=0,1,...,n-1$.

### Salida

Imprima la lista $L^\prime$ desde el índice $0$ hasta el índice $n-1$, separando con un espacio a cada elemento.

Por ejemplo: Para $L= [3,4,1,2,5,2]$

Debería imprimir:

> 3 4 4 4 5 5

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$ tamaño de $L$
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `L` : un array de números de tamaño `dw` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 12
L dw 3,4,1,2,5,2
```
