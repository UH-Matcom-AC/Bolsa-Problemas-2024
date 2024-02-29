# I,J-ésimo Término de Ackermann (Problema 8)

## Descripción

La sucesión recurrente de Ackermann se define por la función $A(m, n)$, con $m, n \ge 0$ donde:
- $A(0, n) = n + 1$
- $A(m, 0) = A(m-1, 1)$ con $m > 0$
- $A(m, n) = A(m-1, A(m, n-1))$

Dados $i$ y $j$, tal que $i, j \ge 0$, hallar el $i,j$-ésimo término de Ackermann

### Salida

Imprimir el valor de $A(i,j)$.

Por ejemplo: Para $i = 1$, y $j = 3$.

Debería imprimir:

> 5

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $i$
- $w_1$ : $j$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `i` : un número de tamaño `dw` que representa $i$
- `j` : un número de tamaño `dw` que representa $i$

Por ejemplo, un posible encabezado podría ser:

```
section .data
i dw 1
j dw 3
```
