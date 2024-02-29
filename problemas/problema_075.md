# Fecha Válida (Problema 75)

## Descripción

Dados tres números $d,m,a$ determinar si forman una fecha válida.

### Salida

Para la salida debe imprimir T en caso de ser una fecha válida, F en caso contrario.

Por ejemplo: para $d = 28$, $m = 05$ y $a = 1998$ debería imprimir:

> T

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $d$
- $w_1$ : $m$
- $w_2$ : $a$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `d` : un número de tamaño `db` que representa el dia $d$
- `m` : un número de tamaño `db` que representa el mes $m$
- `a` : un número de tamaño `dd` que representa el anno $a$


Por ejemplo, un posible encabezado podría ser:

```
section .data
d db 28
m db 05
a dd 1998
```