# Ordenacion (Problema 67)

## Descripción

Dada una lista $L$ devolver la lista $L^{'}$ que se obtiene al ordenar sus elementos, utilizando un método de ordenación $O(n)$.

### Salida

Para la salida debe imprimir la lista $L$ ordenada de menor a mayor, separando cada elemento por un espacio en blanco.

Por ejemplo: para $L = [4, 3, 5, 6]$ debería imprimir:

> 3 4 5 6

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