# N Perfectos (Problema 1)

Se dice que un número $k > 0$ es **perfecto** si la suma de sus divisores, distintos de $k$, es igual a $k$. Por ejemplo, $6$ es perfecto porque $1 + 2 + 3 = 6$. Dado un número $n > 0$ hallar todos los números perfectos, desde $1$ hasta $n$.

### Salida

Para la salida debe imprimir los valores separados por saltos de líneas. En el caso que no hayan números perfectos no imprima nada.

Por ejemplo: para el caso donde $n = 30$ la salida por consola debe tener la siguiente forma:

> 6  
> 28 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo:

```
section .data
n dw 12
```

 

