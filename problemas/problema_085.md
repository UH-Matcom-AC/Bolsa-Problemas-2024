# Triángulo Rectángulo (Problema 85)

## Descripción

Dados los puntos $A$, $B$ y $C$, determine si el triángulo formado por ellos es rectángulo.

### Salida

Imprima `T` si el triángulo es rectángulo, `F` en caso contrario.

Por ejemplo: Para $A=(0,0)$, $B=(0,1)$ y $C=(1,0)$.

Debería imprimir:

> T

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_{0:1}$ : $A$
- $w_{2:3}$ : $B$
- $w_{4:5}$ : $C$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `A` : un array de números de tamaño `dw` que representa $A$
- `B` : un array de números de tamaño `dw` que representa $B$
- `C` : un array de números de tamaño `dw` que representa $C$

Por ejemplo, un posible encabezado podría ser:

```
section .data
A dw 0,0
B dw 0,1
C dw 1,0
```
