# Cajero (Problema 86)

## Descripción

Dados un número $x$ y una lista $L$ representando cantidaddes de billetes de $3, 5, 10, 20$ y $50$ pesos, exactamente en ese orden, halle una distribución de billetes de cada tipo que suman $x$.


### Salida

Para la salida debe imprimir la cantidad de billetes de cada valor necesarios para que sumen $x$. Separar cada elemento de la lista resultante por espacios.

Por ejemplo: para $L = [2, 0, 1, 0, 2]$ y $x=103$ una posible solución sería:

* Billetes de 50 pesos: 2
* Billetes de 20 pesos: 0
* Billetes de 10 pesos: 0
* Billetes de 5 pesos: 0
* Billetes de 3 pesos: 1

Luego, debería imprimir:
> 1 0 0 0 2

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$: $x$
- $w_1$: $n$ (tamaño de la lista $L$)
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `x` : un número de tamaño `db` que representa $x$
- `n` : un número de tamaño `dd` que representa al tamaño de la lista $L$
- `array` : un array de números de tamaño `dd` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
x db 103
n dd 5
array db 2, 0, 1, 0, 2
```