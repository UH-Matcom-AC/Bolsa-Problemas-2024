# Base A a Decimal (Problema 0)

## Descripción

Sea $m$ un número con $n$ cifras, se entiende por $i$-ésima cifra a $c_i$ (donde $c_0$ es la cifra menos significativa y $c_{n-1}$ es la más significativa). Si $m$ es un número en base $A$, entonces cada cifra $0 \le c_i < A$. Además $m$ se puede descomponer de la siguiente forma:

$$m = \sum_{i=0}^{n-1} c_i \cdot A^i$$

Dado un número $m$ en base $0 < A$, halle su representación en base decimal. Considere como caracteres los valores desde `0` hasta `9` para las bases menores que $11$, y los valores desde `A`...`Z` del alfabeto inglés para el resto.

### Salida

Debe imprimir el número en base decimal, colocando sus cifras de derecha a izquierda, desde la cifra menos significativo hasta la más significativa.

Por ejemplo: Para $m = 1D$ y $A = 16$

Debería imprimir:

> 29 

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $A$
- $w_1$ : $n$ (cantidad de cifras del número $m$)
- $w_{2:n+1}$ : Las cifras de $m$ en orden ascendente de caracter menos significativo a más significativo.

Para el ejemplo anterior la disposición de la entrada por palabra sería:

- $w_0$ : 16
- $w_1$ : 2
- $w_2$ : 13
- $w_3$ : 1

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `A` : un número de tamaño `db` que representa $A$
- `n` : un número de tamaño `db` que representa la cantidad de cifras $n$ del número $m$.
- `m` : un array de números de tamaño `db` que representa $m$ dado por los caracteres ASCII que lo conforman. Se disponen ascendentemente de derecha a izquerda.

Por ejemplo, un posible encabezado (para el ejemplo anterior) podría ser:

```
section .data
A db 10
n db 2
m db "1D" ;
; Tambien es valido para m:
; m db "1","D"
; E incluso:
; m db 49, 68
```
