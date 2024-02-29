# Divisibilidad (Problema 17)

## Descripción

Un número $B$ se dice que divide a otro número $A$ si el resultado de dividir $A$ por $B$ es un número entero sin dejar residuo. Esto se expresa como $A = B \times k$, donde $k$ es un número entero. Esto significa que $A$ puede ser exactamente dividido por $B$ $k$ veces sin dejar ningún resto.
Sean $a$ y $b$ dos números enteros tal que $a, b > 0$, diga si $b$ divide a $a$. No se permite utilizar la división implementada en Logisim o en SASM.

### Salida

Imprimir T si $b$ divide a $a$ y F en caso contrario

Por ejemplo: Para $a = 11$ y $b = 3$

Debería imprimir:

> F

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `db` que representa $a$
- `b` : un número de tamaño `db` que representa $b$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a db 11
b db 3
```