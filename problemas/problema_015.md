# Decimal a Base A (Problema 15)

## Descripción

Sea $m$ un número con $n$ cifras, se entiende por $i$-ésima cifra a $c_i$ (donde $c_0$ es la cifra menos significativa y $c_{n-1}$ es la más significativa). Si $m$ es un número en base $A$, entonces cada cifra $0 \le c_i < A$. Además $m$ se puede descomponer de la siguiente forma:

$$m = \sum_{i=0}^{n-1} c_i \cdot A^i$$

Dado un número $m$ en base decimal, y un número $0 < A$, halle su representación en base $A$.

### Salida

Debe imprimir el número en su nueva base, colocando sus cifras de derecha a izquierda, desde la cifra menos significativa hasta la más significativa. Considere como caracteres los valores desde `0` hasta `9` para las bases menores que $11$, y los valores desde `A`...`Z` del alfabeto inglés para el resto. Por ejemplo, para base $A=16$ se debe usar los caracteres `0`,...,`9`,`A`,...,`F`.

Por ejemplo: Para $m = 29$ y $A = 16$

Debería imprimir:

> 1D

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $m$
- $w_1$ : $A$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `m` : un número de tamaño `dd` que representa $m$
- `A` : un número de tamaño `db` que representa $A$

Por ejemplo, un posible encabezado podría ser:

```
section .data
m dd 29
A db 16
```
