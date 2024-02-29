# Alternando Bits (Problema 70)

## Descripción

Dado un número de 32 bits $m$ (con su representacion en decimal) y una lista $L$ de  $n$ números $a_1,a_2,...a_n$ con $a_i \in [0,31]$. Devolver el número  $m^{'}$ que se obtiene al alternar los valores de los bits de $m$ según los elementos de $L$.

### Salida

Para la salida debe imprimir $m^{'}$ en binario, con cada digito separado por un espacio.

Por ejemplo: si $m$ fuera $209 = 11001001$ (convertido a binario) y $L$ fuera $[1,4]$ se  $11011011$ debería imprimir:

> 1 1 0 1 1 0 1 1

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $x$
- $w_1$: $n$ (tamaño de la lista $L$)
- $w_{2:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `x` : un número de tamaño `dd` que representa $x$
- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
x dd 209
n dd 2
array dd 1, 4
```