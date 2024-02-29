# Moda de un array (Problema 26)

## Descripción

La moda es el número que aparece con mayor frecuencia en un conjunto de datos. En el caso de una lista de números, si hay más de un número que aparece con la misma frecuencia máxima, entonces la lista no tiene una moda única y se asume que cualquiera de estos números puede ser la moda.

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver la moda de $L$.

### Salida

Para la salida debe imprimir la moda de $L$.

Por ejemplo: para $L = [4, 3, 4, 6]$ debería imprimir:

> 4

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
array db 4, 3, 4, 6
```