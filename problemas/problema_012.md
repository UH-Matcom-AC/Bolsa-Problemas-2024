# Mínimo Común Múltiplo (Problema 12)

## Descripción

Se dice que $b$ es múltiplo de $a$ (siendo $a$ y $b$ naturales), si existe un natural $n$ tal que $b = n \cdot a$. Dados dos números $a$ y $b$, encuentro el mínimo común múltiplo de $a$ y $b$. Por ejemplo, 12 es múltiplo común de $2$ y $3$, pero no es el mínimo; en este caso su mínimo común múltiplo es 6.

### Salida

Imprimir el mínimo común múltiplo de $a$ y $b$.

Por ejemplo: Para $a=2$ y $b=6$

Debería imprimir:

> 12

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `dw` que representa $a$
- `b` : un número de tamaño `dw` que representa $b$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a dw 2
b dw 3
```

