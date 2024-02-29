# Ramita Fuerte (Problema 84)

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

Dado un árbol binario $T$ y un número $s$, encuentre el subárbol que la suma de sus nodos sea menor que $k$ pero a la vez sea la suma más grande que cumpla esta condición. 

### Salida

Imprima el resultado de la suma de los nodos del subarbol encontrado.

Por ejemplo: Para el ejemplo anterior y tomando $k=9$

Debería imprimir:

> 8

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $k$
- $w_1$ : $n$, cantidad de palabras (*words*) que ocupa el árbol $T$.
- $w_{2:n}$ : Árbol $T$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `k` : un número de tamaño `dw` que representa $k$
- `n` : un número de tamaño `dw` que representa la cantidad de palabras (*words*) que ocupa el árbol $T$
- `T` : un array de números de tamaño `dw` que representa el árbol $T$

Por ejemplo, un posible encabezado podría ser:

```
section .data
k dw 9
n dw 15
array dw 1,2,6,-1,3,-1,-1,-1,-1,4,5,-1,-1,-1,-1
```
