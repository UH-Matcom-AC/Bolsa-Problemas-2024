# Dentro de un Triángulo (Problema 58)

## Descripción

Dado tres puntos $A$, $B$ y $C$ en el plano, determinar si un punto $P$ está dentro del triángulo $ABC$.

### Salida

Debe imprimir `T` si $P$ está dentro del triángulo $ABC$ y `F` en caso contrario.

Por ejemplo: si $P = (1, 1)$, $A = (0, 0)$, $B = (2, 0)$ y $C = (1, 2)$.

Debería imprimir:

> T

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_{0:1}$ : $A$ (primero la componente $A_1$, y luego $A_2$).
- $w_{2:3}$ : $B$ (Idem)
- $w_{4:5}$ : $C$ (Idem)
- $w_{6:7}$ : $P$ (Idem)

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `A` : un array de números de tamaño `dw` que representa $A$
- `B` : un array de números de tamaño `dw` que representa $B$
- `C` : un array de números de tamaño `dw` que representa $C$
- `P` : un array de números de tamaño `dw` que representa $P$

Por ejemplo, un posible encabezado podría ser:

```
section .data
A dw 0,0
B dw 2,0
C dw 1,2
P dw 1,1
```
