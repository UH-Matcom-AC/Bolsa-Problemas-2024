# Build Heap (Problema 49)

## Descripción

Un árbol binario se puede definir en un array de la siguiente forma:

- La raíz del árbol se encuentra en la posición $0$
- Los hijos del nodo en la posición $i$ se encuentran en las posiciones:
    - $2 \cdot i + 1$ izquierdo
    - $2 \cdot i + 2$ derecho
- El padre de un nodo en la posición $i$ se encuentra en la posisción $\lfloor\frac{i + 1}{n}\rfloor - 1$
- Si ambos *hijos* de un nodo $X$ son vacíos ($-1$), entonces el nodo $X$ se dice que es una hoja, y no se considera que tenga hijos.

Por ejemplo, el siguiente árbol en un array tendría la estructura indicada:  

![Problema 60 ()](/img/arbol.svg)  

Un *Heap*, es un árbol binario parcialmente ordenado, que cumple las siguientes condiciones:  

- Todos los niveles están llenos, excepto, quizás el último.
- Los niveles se van llenando de izquierda a derecha.
- Cada nodo tiene una prioridad que es menor o igual (*Heap* de mínimo) que la de sus hijos. También pudiera ser mayor o igual (*Heap* de máximo).

Note que la estructura en *array* de un Heap es más eficiente que la de un árbol binario desbalanceado según lo explicado al inicio, ya que se asegura que todos los nodos están contiguos en memoria.

Dado un *array* $L$, con $n>0$ elementos, construya un *Heap* de mínimos a apartir de $L$ utilizando el algoritmo *BuildHeap*. Se denotará al *array* resultante como $L^\prime$

### Salida

Debe imprimir los elementos del array $L^\prime$ separados por espacios

Por ejemplo: Si $L= [8, 5, 20, 4, 6, 3, 10, 2, 5, 4, 1]$

Debería imprimir:

> 1 2 3 4 4 20 10 8 5 5 6

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$ tamaño del array $L$
- $w_{1:n}$ : $L$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$ la cantidad de elementos del array $L$
- `L` : un array de números de tamaño `dw` que representa $L$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 11
L dw 8, 5, 20, 4, 6, 3, 10, 2, 5, 4, 1
```
