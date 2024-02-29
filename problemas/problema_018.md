# Mínimo de un array (Problema 18)

## Descripción

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver el índice del mínimo elemento de $L$.

### Salida

Para la salida debe imprimir el mínimo elemento de $L$.

Por ejemplo: para $L = [4, 3, 5, 6]$ debería imprimir:

> 1

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
n dd 4
array dd 4, 3, 5, 6
```