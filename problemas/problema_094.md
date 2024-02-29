# Ortoedro (Problema 94)

## Descripción

Dado un ortoedro con lados de longitud $l$, hallar el volumen del mismo

### Salida

Para la salida debe imprimir el valor del volumen del ortoedro en $cm^{3}$.

Por ejemplo: para $l=3$ debería imprimir:

> 27

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $l$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `l` : un número de tamaño `dw` que representa $l$

Por ejemplo, un posible encabezado (para el ejemplo inicial) podría ser:

```
section .data
l dw 3
```