# Repeticiones en Array (Problema 27)

## Descripción

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver una lista $L'$ con la cantidad de repeticiones de cada elemento en dicha lista.

### Salida

Para la salida debe imprimir las repeticiones de cada elemento de $L$ en el mismo orden en que aparecen en $L$.

Por ejemplo: para $L = [1, 1, 2, 3, 1, 2, 2, 2, 3]$ debería imprimir:

> 3 3 4 2 3 4 4 4 2

Porque 1 aparece 3 veces, 2 se repite 4 y 3 se repite 2 veces.
## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $n$ (tamaño de la lista $L$)
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 9
array db 1, 1, 2, 3, 1, 2, 2, 2, 3
```