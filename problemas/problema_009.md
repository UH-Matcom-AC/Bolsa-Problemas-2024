# I-ésimo Término de Collatz (Problema 9)

## Descripción

Se define la función $f(n)$ con $n>0$, a la función:
- $f(n) = \frac{n}{2}$ cuando $n$ es par
- $f(n) = 3n + 1$ cuando $n$ es impar

Se define como suceción de Collatz para $n$, a la sucesión $a_i$ definida de la siguiente forma:
- $a_0 = n$
- $a_i = f(a_{i-1})$

Dado un número $n$, halle el $i$-ésimo término de la sucesión de Collatz para $n$

### Salida

Imprima $a_i$ para $n$.

Por ejemplo: Para $n = 10$, y $i = 3$

Debería imprimir:

> 8 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$
- $w_1$ : $i$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$
- `i` : un número de tamaño `dw` que representa $i$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 10
i dw 3
```
