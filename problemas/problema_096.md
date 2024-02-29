# Array en Array (Problema 99)

## Descripción

Dados dos patrones de bits $L,L^{'}$ y una posición $i$, halle $L^{''}$ que será el resultado de insertar la cadena $L^{'}$ en la $i$-ésima posición de $L$.

### Salida

Para la salida debe devolver la cadena de mayor tamaño $L^{''}$ que sea substring de las dos.

Por ejemplo: para $L = [1, 0, 1, 1]$, $L^{'} = [1, 0]$ e $i = 1$ debería imprimir:

> 1 1 0 0 1 1

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $i$ 
- $w_1$: $n$ (tamaño de la lista $L$)
- $w_{2:n+2}$ : $L$
- $w_{n+3}$ (tamaño de la lista $L^{'}$)
- $w_{n+4:n+n^{'}+4}$ : $L^{'}$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `i` : un número de tamaño `dw` que representa $i$
- `n_1` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array_1` : un array de números de tamaño `dd` que representa $L$
- `n_2` : un número de tamaño `dd` que representa al tamaño de la lista $L^{'}$
- `array_2` : un array de números de tamaño `dd` que representa $L^{'}$

Por ejemplo, un posible encabezado podría ser:

```
section .data
i 1
n_1 dd 4
array_1 dd 1, 0, 1, 1
n_2 dd 2
array_2 dd 1, 0
```