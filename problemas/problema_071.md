# Daditos (Problema 71)

Dado $n$ dados computar todas las posibles combianciones de los valores de sus tiradas.

### Salida

Para la salida debe imprimir la cantidad de posibles combianciones de los valores de sus tiradas.

Por ejemplo: para el caso donde $n = 2$ la salida por consola debe tener la siguiente forma:

> 36

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo:

```
section .data
n dw 2
```