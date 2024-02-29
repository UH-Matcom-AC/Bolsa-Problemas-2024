# Factorial (Problema 61)

## Descripción

El factorial de un número $n$, denotado como $n!$, es el producto de todos los números enteros positivos menores o iguales a $n$. Es decir:

$
n! = n \times (n-1) \times (n-2) \times \cdots \times  2 \times  1
$

Para $n =  0$, $0! =  1$.

Dado un número $n$ devolver $n!$

### Salida

Para la salida debe imprimir el factorial de $n$.

Por ejemplo: para $n=3$ debería imprimir:

> 6 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 3
```
