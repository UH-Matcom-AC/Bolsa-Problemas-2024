# I-ésimo Perfecto (Problema 4)

## Descripción

Se dice que un número $k > 0$ es **perfecto** si la suma de sus divisores, distintos de $k$, es igual a $k$. Por ejemplo, $6$ es perfecto porque $1 + 2 + 3 = 6$. Dado un número $i \ge 0$ hallar el $i$-ésimo perfecto. Se considera que el $0$-ésimo perfecto es el primero.

### Salida

Para la salida debe imprimir el $i$-ésimo perfecto.

Por ejemplo: para $i=2$ debería imprimir:

> 496  

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $i$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `i` : un número de tamaño `dw` que representa $i$

Por ejemplo, un posible encabezado podría ser:

```
section .data
i dw 2
```
