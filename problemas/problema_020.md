# Máximo de un array en intervalo (Problema 20)

## Descripción

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ y un íntervalo $[b,c]$ dentro de esa lista devolver el máximo elemento de ese intervalo.

### Salida

Para la salida debe imprimir el máximo elemento de $L$ en el intervalo $[b,c]$.

Por ejemplo: para $L = [4, 3, 5, 6]$ con el intervalo $[b,c] = [1,3]$ debería imprimir:

> 6

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $b$
- $w_1$ : $c$
- $w_2$: $n$ (tamaño de la lista $L$)
- $w_{3:n+2}$ : $L$


## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `b` : un número de tamaño `db` que representa $b$
- `c` : un número de tamaño `db` que representa $c$
- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
b db 1
c db 3
n dd 4
array db 4, 3, 5, 6
```