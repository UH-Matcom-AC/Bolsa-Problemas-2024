# Varianza de un array (Problema 25)

## Descripción

La varianza es una medida de dispersión que indica cuánto se alejan los números de su media. Se calcula restando la media de cada número en el conjunto, elevando el resultado al cuadrado, sumando todos estos cuadrados y luego dividiendo por la cantidad de números en el conjunto menos uno. Sean $n$ la cantidad de números y $x_1, x_2, \ldots, x_n$ los números en el conjunto, la varianza se calcula como:

$
%\begin{equation}
\text{Varianza} = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \text{Media})^2
%\end{equation}
$

Donde $\text{Media}$ es la media aritmética de los números en el conjunto.

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver la varianza de $L$.

### Salida

Para la salida debe imprimir la varianza de $L$.

Por ejemplo: para $L = [4, 3, 5, 6]$ debería imprimir:

> 2.0

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
array db 4, 3, 5, 6
```