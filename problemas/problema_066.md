# Merge Sort (Problema 66)

## Descripción
Merge Sort es un algoritmo de ordenamiento basado en la técnica de divide y vencerás. Funciona dividiendo la lista de entrada en dos mitades, ordenando cada mitad de forma recursiva y luego fusionando las dos mitades ordenadas. Este proceso se repite hasta que la lista completa esté ordenada.

$\textbf{Pasos del Algoritmo}$:

* $\textbf{División}$: Si la lista tiene más de un elemento, se divide en dos mitades.
* $\textbf{Ordenamiento Recursivo}$: Cada mitad se ordena recursivamente utilizando Merge Sort.
* $\textbf{Fusión}$: Las dos mitades ordenadas se fusionan para formar una lista completa ordenada.

```
Función MergeSort(A)
    Si longitud(A) > 1 entonces
        medio = longitud(A) / 2
        L = A[0, medio]
        R = A[medio, longitud(A)]
        MergeSort(L)
        MergeSort(R)
        Merge(A, L, R)
    Fin Si
Fin Función

Función Merge(A, L, R)
    i = 0
    j = 0
    k = 0
    Mientras i < longitud(L) y j < longitud(R) hacer
        Si L[i] <= R[j] entonces
            A[k] = L[i]
            i = i + 1
        Sino
            A[k] = R[j]
            j = j + 1
        Fin Si
        k = k + 1
    Fin Mientras
    Mientras i < longitud(L) hacer
        A[k] = L[i]
        i = i + 1
        k = k + 1
    Fin Mientras
    Mientras j < longitud(R) hacer
        A[k] = R[j]
        j = j + 1
        k = k + 1
    Fin Mientras
Fin Función
```

Dado dos arrays ordenados $A_1,A_2$ devolver el arreglo ordenado $A_3$ obtenido haciendo una mezcla ordenada de $A_1$ y $A_2$.

### Salida

Para la salida debe imprimir la lista ordenada de menor a mayor, separando cada elemento por un espacio en blanco.

Por ejemplo: para $L = [1, 3, 5, 7]$ y $L^{'} = [2, 4, 6, 8]$ debería imprimir:

> 1 2 3 4 5 6 7 8

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
array_1 dd 1, 3, 5, 7
n_2 dd 4
array_2 dd 2, 4, 6, 8
```