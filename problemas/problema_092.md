# Pirámide (Problema 91)

## Descripción

Dada una pirámide con base de área $B$ y altura $h$, hallar el volumen de la misma.

### Salida

Para la salida debe imprimir el valor del volumen del pirámide en $cm^{3}$.

Por ejemplo: para $B = 4$ y $h = 3$ debería imprimir:

> 4

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $B$
- $w_1$ : $h$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `B` : un número de tamaño `dw` que representa $B$
- `h` : un número de tamaño `dw` que representa $h$

Por ejemplo, un posible encabezado (para el ejemplo inicial) podría ser:

```
section .data
B dw 4
h dw 3
```