# Insertion Sort++ Z-A (Problema 95)

## Descripción

El algoritmo Insertion Sort es un método de ordenamiento que funciona de manera similar a cómo las personas ordenan las cartas en un juego de póker. Este algoritmo divide la lista en una parte ordenada y otra desordenada. Inicialmente, la parte ordenada contiene un solo elemento, el primer elemento de la lista. Luego, el algoritmo toma el siguiente elemento de la lista desordenada y lo inserta en la posición correcta dentro de la parte ordenada. Este proceso se repite hasta que toda la lista esté ordenada.

El objetivo del algoritmo Insertion Sort es ordenar una lista de números en orden ascendente o descendente.

El algoritmo Insertion Sort se realiza de la siguiente manera:

    * Comienza con el segundo elemento de la lista.
    * Compara este elemento con el elemento anterior.
    * Si el elemento actual es menor que el elemento anterior, se intercambian.
    * Este proceso se repite para cada elemento de la lista, moviéndose hacia la derecha.
    * Una vez que se ha recorrido toda la lista, el algoritmo termina.


Pseudocodigo:
```
Algoritmo InsertionSort(A)
    Para i desde   1 hasta longitud(A) -   1 hacer
        clave = A[i]
        j = i -   1
        Mientras j >=   0 y A[j] < clave hacer
            A[j +   1] = A[j]
            j = j -   1
        Fin Mientras
        A[j +   1] = clave
    Fin Para
Fin Algoritmo
```

Dada una lista $L$ de $n$ elementos $a_1,a_2,...,a_n$ devolver la lista ordenada de mayor a menor utilizando el algoritmo de Insertion Sort.

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