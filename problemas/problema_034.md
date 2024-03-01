# Subcojuntos (Problema 34)

## Descripción
Dado una lista $A$ con elementos $a_1,a_2,...,a_{n_a}$ y una lista $B$ con elementos $b_1,b_2,...,b_{n_b}$. Ambas listas representan conjuntos, se quiere saber si $A \subseteq B$. Se debe recordar que si $A \subseteq B$ se cumple que $\forall x \in A \rightarrow  x \in B$

### Salida

La salida es 1 si son iguales, 0 en caso contrario

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n_a$ La cantidad de elementos que tiene el primer conjunto
- $w_{1:n_{a}}$ : $a_1, a_2,...,a_{n_a}$ los elementos que conforman el conjunto $A$
- $w_{n_{a} + 1}$ : $n_b$ La cantidad de elementos que tiene el segundo conjunto
- $w_{n_{a} + 2:n_{a}+n_{b}+ 2}$ : $b_1, b_2,...,b_{n_b}$ los elementos que conforman el conjunto $B$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n_a` : un número de tamaño `dd` que representa  $n_a$
- `array_A` : un array de números de tamaño `dw` que representa el conjunto $A$
- `n_b` un número de tamaño `dd` que representa  $n_b$
- `array_B` : un array de números de tamaño `dw` que representa el conjunto $B$
Por ejemplo, un posible encabezado podría ser:

```
section .data
n_a dd 4
array_A dw 23, 56, 98, 14
n_b dd 5
array_B dd 23,56,98,14,7
```
