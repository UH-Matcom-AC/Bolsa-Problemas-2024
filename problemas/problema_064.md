# Palíndromos (Problema 64)

## Descripción

Un palíndromo es una palabra, frase, número o secuencia que se lee igual hacia adelante que hacia atrás, sin importar la dirección en la que se lea. Los palíndromos pueden ser de una sola palabra, como "11011" o "12321".

Dado un patrón en forma de bits. Devolver el menor sufijo que habría que agregarle a dicho patrón para que fuera palindromo.

### Salida

Para la salida debe imprimir el menor sufijo, separando cada dígito por un espacio.

Por ejemplo: para $L = [1, 0, 1, 1]$ debería imprimir:

> 0 1

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
n dd 4
array dd 1, 0, 1, 1
```