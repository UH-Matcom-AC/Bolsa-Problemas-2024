# Raíz de N (Problema 56)

## Descripción

Dado un número entero $n$, halle $r = \lfloor \sqrt{n} \rfloor$.


### Salida

Debe imprimir el valor de $r$.

Por ejemplo: si $n = 5$

Debería imprimir:

> 2

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 5
```
