# Rectas que se cortan (Problema 87)

## Descripción

Dadas 2 rectas en el plano $<R_1, R_2>$ y $<P_1, P_2>$ decir si se cortan.

### Salida

Para la salida debe imprimir T si se cortan o F en caso contrario.

Por ejemplo: Dadas las rectas $<R_1, R_2>$ y $<P_1, P_2>$, donde:

$<R_1, R_2>$ es la recta (y = 2x + 3)
$<P_1, P_2>$ es la recta (y = -x + 1), obtenemos:

> T

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_{0:1}$ : $R_1$ (Array con Punto $R1$ perteneciente a recta $<R_1, R_2>$)
- $w_{2:3}$ : $R_2$ (Array con Punto $R2$ perteneciente a recta $<R_1, R_2>$)
- $w_{4:5}$ : $P_1$ (Array con Punto $P_1$ perteneciente a recta $<P_1, P_2>$)
- $w_{6:7}$ : $P_2$ (Array con Punto $P_2$ perteneciente a recta $<P_1, P_2>$)


## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `R1` : un array de números de tamaño `db` que representa $R1$
- `R2` : un array de números de tamaño `db` que representa $R2$
- `P1` : un array de números de tamaño `db` que representa $P1$
- `P2` : un array de números de tamaño `db` que representa $P2$

Por ejemplo, un posible encabezado podría ser:

```
section .data
R1 db 0, 3
R2 db 2, 7
P1 db 0, 1
P2 db 1, 0
```