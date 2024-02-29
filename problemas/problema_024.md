# Media de un array (Problema 24)

## Descripción

La media aritmética, o promedio, de una cantidad de números se calcula sumando todos los números en el conjunto y luego dividiendo el resultado por la cantidad de números en el conjunto. Sean $n$ la cantidad de números en el conjunto y $x_i$ el $i$-ésimo número, la media se calcula como:

$
%\begin{equation}
\frac{1}{n} \sum_{i=1}^{n} x_i
%\end{equation}
$

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver la media de $L$.

### Salida

Para la salida debe imprimir la media de $L$.

Por ejemplo: para $L = [4, 3, 5, 6]$ debería imprimir:

> 4.5

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