# I-ésimo Primo (Problema 3)

## Descripción

Se dice que un número $k > 1$ es **primo** si no tiene divisores, distintos de $k$ y $1$. Por ejemplo, $7$ es primo, pero $6$ no, ya que tiene los divisores $2$ y $3$. Dado un número $i \ge 0$ hallar el $i$-ésimo primo. Se considera que el $0$-ésimo primo es el primero.

### Salida

Para la salida debe imprimir el $i$-ésimo primo.

Por ejemplo: para $i=2$ debería imprimir:

> 5  

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
