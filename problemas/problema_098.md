# Bubble Sort++ Z-A (Problema 98)

## Descripción

El algoritmo $\textbf{Bubble Sort}$ es un método simple de ordenamiento de listas que funciona intercambiando repetidamente los elementos adyacentes si están en el orden incorrecto. Este proceso se repite hasta que no se requieren más intercambios, lo que indica que la lista está ordenada.


El objetivo del algoritmo $\textbf{Bubble Sort}$ es ordenar una lista de números en orden ascendente o descendente.

El algoritmo $\textbf{Bubble Sort}$ se realiza de la siguiente manera:

*  Comienza recorriendo la lista desde el primer elemento hasta el penúltimo.
* Compara cada par de elementos adyacentes y los intercambia si están en el orden incorrecto.
* Continúa este proceso hasta que no se requieran más intercambios.
* Si la lista está ordenada, el algoritmo termina. De lo contrario, repite el proceso desde el principio.

Pseudocodigo:
```
Algoritmo BubbleSort(A, n)
    // n = longitud(A)
    Para i desde  0 hasta n-1 hacer
        Para j desde  0 hasta n-i-1 hacer
            Si A[j] < A[j+1] entonces
                intercambiar A[j] y A[j+1]
            Fin Si
        Fin Para
    Fin Para
Fin Algoritmo
```

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver la lista ordenada de mayor a menor utilizando el algoritmo de Bubble Sort.

### Salida

Para la salida debe imprimir la lista $L$ ordenada de mayor a menor, separando cada elemento por un espacio en blanco.

Por ejemplo: para $L = [4, 3, 5, 6]$ debería imprimir:

> 6 5 4 3

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
array dd 4, 3, 5, 6
```