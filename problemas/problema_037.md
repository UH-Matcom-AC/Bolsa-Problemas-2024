# Nombre Partición de un Conjunto II(Problema 37)

## Descripción
Dado un conjunto $A$ y un número $n$. Particionar a $A$ en dos conjuntos $A_1$ y $A_2$, donde en $A_1$ estén todos los elementos de $A$ que son divisibles por $n$, o sea $ \braket{A_1 |a_i \in A, a_i \, mod\,  n = 0}$ y en $A_2$ esten todos los elementos de $A$  que no son divisibles por $n$ $ \braket{A_2 |a_i \in A, a_i \, mod\,  n \ne 0}$

### Salida
Para la salida debe imprimir los valores separados por saltos de líneas en el caso de los elementos de un mismo conjunto. Ambos conjnuntos serán separados por una línea en blanco
#### Ejemplo
Si $A_1 =\{ 2,4,6\} $ y $A_2 =\{ 13,15,27\} $. La salida sería
> 2
> 4
> 6
>
> 13
> 15
> 27

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n_a$ La cantidad de elementos que tiene el conjunto $A$
- $w_{1:n_a}$ : $a_1,a_2,...a_{n_a}$ Los elementos que conforman al conjunto $A$
- $w_{n_{a}+ 1}$: $n$ El término por el que se va a separar $A$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `na` : un número de tamaño `dd` que representa $n_a$
- `array` : un array de números de tamaño `dw` que representa $A$
- `n`: : un número de tamaño `dd` que representa $n$

Por ejemplo, un posible encabezado podría ser:

```
section .data
na dd 12
array dw 23, 56, 98, 14
n dd 60
```
