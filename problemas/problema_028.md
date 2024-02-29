# Suma de n menores que x (Problema 28)

## Descripción

Dada una lista $L$ de $n$ elementos $a_1, a_2, \ldots, a_n$ y un número $x$, la suma de todos los números en $L$ que sean menores que $x$ se denota como:

$
%\begin{equation}
\sum_{a_i \in L, a_i < x} a_i
%\end{equation}
$

Sea una lista no ordenada $L$ de $n$ elementos $a_1,a_2,...,a_n$ y un número $x$, devolver la suma de todos los números en $L$ que sean menores que $x$.

### Salida

Para la salida debe imprimir  la suma de todos los números en $L$ que sean menores que $x$.

Por ejemplo: para $L = [4, 3, 4, 6]$ y $x=5$ debería imprimir:

> 11

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