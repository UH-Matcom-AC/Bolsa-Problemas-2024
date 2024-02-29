# Colitas (Problema 72)

Dado $n$ personas computar todas las formas posibles de organizar una cola.

### Salida

Para la salida debe imprimir la cantidad de posibles formas de organizar una cola.

Por ejemplo: para el caso donde $n = 2$ la salida por consola debe tener la siguiente forma:

> 2

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