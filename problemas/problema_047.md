# Recorrido en Inorden (Problema 46)

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

El recorrido en *inorden* de un árbol binario consiste en recorrer el árbol a partir de su raíz aplicando las siguientes operaciones recursivas en el orden indicado:  

- Recorrer el subárbol izquierdo
- Extraer llave del nodo  
- Recorrer el subárbol derecho

Dado un árbol binario $T$ cuyas llaves son caracteres del alfabeto inglés en código ASCII, halle el recorrido en ineorden.

### Salida

Imprima separado por espacio cada nodo del árbol $T$

Por ejemplo: Para el árbol:  
![Problema 60 ()](/img/350px-Sorted_binary_tree.svg.png)  

Debería imprimir:

> A, B, C, D, E, F, G, H, I

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$, cantidad de palabras (*words*) que ocupa el árbol $T$.
- $w_{1:n}$ : Árbol $T$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dd` que representa la cantidad de palabras (*words*) que ocupa el árbol $T$
- `T` : un array de números de tamaño `dw` que representa el árbol $T$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 15
array dw 1,2,6,-1,3,-1,-1,-1,-1,4,5,-1,-1,-1,-1
```
