# En qué lado de la Recta? (Problema 60)

## Descripción

Una recta $r$ puede representarse en muchos casos por la función $y = mx + n$, donde $m$, y $n$ son constantes.

Dadas las constantes $m$ y $n$, y un punto $P$, diga si $P$ está por encima de $r$, o por debajo de $r$

### Salida

Imprima `1` si $P$ está por encima, o `-1` está por debajo. Se le asegura que nunca estará en la propia recta.

Por ejemplo: Para $P=(1,0)$ y $m=1$ y $n=0$.

Debería imprimir:

> 1

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $m$
- $w_1$ : $n$
- $w_2$ : $P_1$
- $w_3$ : $P_2$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `m` : un número de tamaño `dw` que representa $m$
- `n` : un número de tamaño `dw` que representa $m$
- `P` : un array de números de tamaño `dw` que representa $P$

Por ejemplo, un posible encabezado podría ser:

```
section .data
m dw 1
n dw 0
P dw 0,0
```
