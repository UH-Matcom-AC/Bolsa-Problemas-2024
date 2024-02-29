# Norma de un Vector (Problema 55)

## Descripción

Sea $v \in \mathbb{R}^n$ con $n>0$, se define la **norma** de $v$ como:

$$
||v|| = \sqrt{\sum_{i=1}^n v_i^2}
$$

Dado un vector $v$, se desea calcular su norma al cuadrado, es decir, $||v||^2$.


### Salida

Debe imprimir el valor de $||v||^2$.

Por ejemplo: si $v = (1, 2, 3)$, entonces $||v||^2 = 14$.

Debería imprimir:

> 14  

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$ dimensión del vector $v$
- $w_{1:n}$ : el vector $v$.

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$ la dimensión de $v$
- `v` : un array de números de tamaño `dw` que representa el vector $v$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 3
v dw 1, 2, 3
```
