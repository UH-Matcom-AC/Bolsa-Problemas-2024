# Contando Bits y Paridad (Problema 69)

Dado un número de 32 bits decir si la cantidad de bits que son 1 es par.

### Salida

Para la salida debe imprimir T en caso de que la cantidad de bits que son 1 es par, F en caso contrario.

Por ejemplo: para el caso donde $n = 2$ la salida por consola debe tener la siguiente forma:

> F

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