# Cilindro (Problema 91)

## Descripción

Hallar el volumen de un cilindro, si se sabe el diámetro $d$ de su base, y su altura $h$.

### Salida

Para la salida debe imprimir el valor del volumen del cilindro en $cm^{3}$.

Por ejemplo: para $d = 2$ y $h = 3$ debería imprimir:

> 9

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $d$
- $w_1$ : $h$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `d` : un número de tamaño `dw` que representa $d$
- `h` : un número de tamaño `dw` que representa $h$

Por ejemplo, un posible encabezado (para el ejemplo inicial) podría ser:

```
section .data
d dw 2
h dw 3
```