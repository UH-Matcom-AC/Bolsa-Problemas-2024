# N Primo (Problema 2)

## Descripción

Se dice que un número $k > 1$ es **primo** si no tiene divisores, distintos de $k$ y $1$. Por ejemplo, $7$ es primo, pero $6$ no, ya que tiene los divisores $2$ y $3$. Dado un número $n > 1$ hallar todos los números primos, desde $1$ hasta $n$.

### Salida

Para la salida debe imprimir cada número primo ascendentemente separados por saltos de líneas.

Por ejemplo: para $n=11$ debería imprimir:

> 2  
> 3  
> 5  
> 7  
> 11  

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo, un posible encabezado (para el ejemplo inicial) podría ser:

```
section .data
n dw 11
```
