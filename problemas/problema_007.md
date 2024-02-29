# I-ésimo Término de Tribonacci (Problema 7)

## Descripción

La sucesión recurrente de Tribonacci se define por la función $T(n)$, con $n \ge 0$ donde:
- $F(0) = 0$
- $F(1) = 0$
- $F(2) = 1$
- $F(n) = F(n-1) + F(n-2) + F(n-3)$

Dado un número $i$, hallar el $i$-ésimo término de la sucesión Tribonacci.

### Salida

Imprimir el $i$-ésimo término de Tribonacci, es decir, $T(i)$.

Por ejemplo: Para $i=6$

Debería imprimir:

> 7 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $i$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `i` : un número de tamaño `dw` que representa $i$

Por ejemplo, un posible encabezado podría ser:

```
section .data
i dw 6
```
