# Insertar en ABB (Problema 50)

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

Diremos que un Árbol de Búsqueda Balanceado (ABB) es un árbol binario que cumple la siguiente propiedad:  

- Todos los elementos almacenados en un subárbol izquierdo de cualquier nodo $x$, son menores que $x$.

Se puede realizar una analogía con los mayores (e incluso con igualdades), pero para nuestro fin nos limitaremos a la definición dada.

Dado un ABB $T$ en su representación de array, y un valor $x$, se desea insertar $x$ en $T$ manteniendo su condición de ABB. Para simplificar el problema nos basta reemplazarlo por el nodo $v$ que sea el menor de los elementos mayores que $x$. De esta forma determine el índice del nodo que se debe reemplazar para realizar la inserción (índice del array que representa al nodo remplazado).

### Salida

Debe imprimir el índice del nodo que debe reemplazar.

Por ejemplo: Si el nodo que se debe reemplazar tiene el índice $3$ en el *array*

Debería imprimir:

> 3

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$ tamaño que ocupa en array el ABB $T$
- $w_{1:n}$ : ABB $T$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$ tamaño que ocupa en array el ABB $T$
- `T` : un array de números de tamaño `dw` que representa el ABB $T$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dw 3
T dw 2, 1, 3
```
