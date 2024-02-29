# I-ésimo Término de Fibonacci (Problema 6)

## Descripción

La sucesión recurrente de Fibonacci se define por la función $F(n)$, con $n \ge 0$ donde:
- $F(0) = 0$
- $F(1) = 1$
- $F(n) = F(n-1) + F(n-2)$

Dado un número $i$, hallar el $i$-ésimo término de la sucesión Fibonacci.

### Salida

Imprimir el $i$-ésimo término de Fibonacci, es decir, $F(i)$.

Por ejemplo: Para $i=3$

Debería imprimir:

> 2 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $i$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `i` : un número de tamaño `dw` que representa $i$

Por ejemplo, un posible encabezado podría ser:

```
section .data
i dw 3
```
