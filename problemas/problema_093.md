# Esfera (Problema 93)

## Descripción

Dado un radio $r$ de una esfera hallar el volumen de la misma.

### Salida

Para la salida debe imprimir el valor del volumen de la esfera en $cm^{2}$. Asuma que $PI = 3, PI$ es un entero.

Por ejemplo: para $r=2$ debería imprimir:

> 26

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $r$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `r` : un número de tamaño `dw` que representa $r$

Por ejemplo, un posible encabezado (para el ejemplo inicial) podría ser:

```
section .data
r dw 2
```