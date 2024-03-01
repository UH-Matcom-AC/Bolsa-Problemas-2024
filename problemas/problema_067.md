# Ordenación (Problema 67)

## Descripción

Dada una lista $L$ devolver la lista $L^{'}$ que se obtiene al ordenar sus elementos, utilizando un método de ordenación $O(n)$. Se conoce que todos los elementos de la lista están en un itervalo desde $a$ a $b$ (ambos enteros); es decir, si el intervalo es de $3$ a $6$, la lista contiene a $3$, $4$, $5$ y $6$, pero no necesariamente ordenados. Note que el tamaño de la lista depende siempre del intervalo.

Dado una lista $L$, de tamaño $n$, que contiene todos los elementos de un intervalo desde algún $a$ a un $b$ (ambos desconocidos a priori), ordene la lista $L$.

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
