# Divisores Primos (Problema 10)

## Descripción

Se dice que un número $k > 1$ es **primo** si no tiene divisores, distintos de $k$ y $1$. Por ejemplo, $7$ es primo, pero $6$ no, ya que tiene los divisores $2$ y $3$. Dado un número $n>1$, hallar todos sus divisores primos.

### Salida

Debe imprimir cada divior primo de forma ascendente, y separados por un espacio de línea. Si $n$ fuera primo, imprime solo $n$.

Por ejemplo: Para $n=6$

Debería imprimir:

> 2  
> 3  

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dd` que representa $n$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 6
```
