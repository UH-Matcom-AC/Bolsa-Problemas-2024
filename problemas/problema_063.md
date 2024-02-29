# Polinomios (Problema 63)

## Descripción

Dado un polinomio $P$ de grado $n$ y su lista de coeficientes $c_1,c_2,..c_n$ devolver el resultado de evaluar $P(x)$ para un $x \in \mathbb{N}$

### Salida

Para la salida debe imprimir el resultado de evaluar el polinomio $P(x)$ para un $x \in \mathbb{N}$. Cada posición del array de entrada representa el valor en la posición $c_i, 1 \leq i \leq n$.

Por ejemplo: para $L = [1, 4, 2]$ y $x = 2$ debería imprimir:

> 17

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $x$
- $w_1$: $n$ (tamaño de la lista $L$)
- $w_{2:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `x` : un número de tamaño `db` que representa $x$
- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
x db 2
n dd 3
array db 1, 4, 2
```