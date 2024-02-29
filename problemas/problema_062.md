# Moda de un array (Problema 62)

## Descripción

Dada una lista $L$ ordenada de $n$ elementos $a_1,a_2,...,a_n$ determinar si está ordenada en orden creciente o decreciente.

### Salida

Para la salida debe imprimir la C si está ordenada en orden creciente o D lo está en orden decreciente.

Por ejemplo: para $L = [3, 4, 6]$ debería imprimir:

> C

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $n$ (tamaño de la lista $L$)
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 3
array db 3, 4, 6
```