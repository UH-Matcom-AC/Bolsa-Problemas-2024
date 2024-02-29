# Substring (Problema 65)

## Descripción

Dado dos patrones de bits $L,L^{'}$ determinar si uno es subcadena del otro.

### Salida

Para la salida debe imprimir T en caso de que $L$ sea subcadena de $L^{'}$ o $L^{'}$ sea subcadena de $L$. Imprimir F en caso contrario.

Por ejemplo: para $L = [1, 0, 1, 1]$ y $L^{'} = [1, 0]$ debería imprimir:

> T

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $n$ (tamaño de la lista $L$)
- $w_{1:n}$ : $L$
- $w_n+1$: $n^{'}$ (tamaño de la lista $L^{'}$)
- $w_{n+1:n+n^{'}}$ : $L^{'}$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n_1` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array_1` : un array de números de tamaño `dd` que representa $L$
- `n_2` : un número de tamaño `dd` que representa al tamaño de la lista $L^{'}$
- `array_2` : un array de números de tamaño `dd` que representa $L^{'}$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n_1 dd 4
array_1 dd 1, 0, 1, 1
n_2 dd 2
array_2 dd 1, 0
```