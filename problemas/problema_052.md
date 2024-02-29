# Unión de Conjuntos (Problema 52)

## Descripción

Dado dos conjuntos de números $A$ y $B$, determinar el conjunto $C = A \cup B$

### Salida

Debe imprimir todos los elementos de $C$ separados por espacio. Recuerde que un conjunto NO tiene elementos repetidos.

Por ejemplo: Si $A=\{1,3,4\}$ y $B==\{1,2,3\}$

Debería imprimir:

> 1 2 3 4

También sería válido otra permutación como:

> 3 1 2 4

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $c_a$ cantidad de elementos de $A$
- $w_{1:c_1}$ : array con elementos de $A$
- $w_{c_1+1}$ : $c_b$ cantidad de elementos de $B$
- $w_{c_1+2:c_1+c_2+2}$ : array con elementos de $B$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `c_a` : un número de tamaño `dw` que representa $c_a$ cantidad de elementos de $A$
- `A` : un array de números de tamaño `dw` que representa $A$
- `c_b` : un número de tamaño `dw` que representa $c_b$ cantidad de elementos de $B$
- `B` : un array de números de tamaño `dw` que representa $B$

Por ejemplo, un posible encabezado podría ser:

```
section .data
c_a dw 3
A dw 1,3,4
c_b dw 3
B dw 1,2,3
```