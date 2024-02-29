# Simplificar Fracción (Problema 13)

## Descripción

Un número racional positivo puede ser definido mediante dos naturales $a$ y $b$ de la forma $\frac{a}{b}$ con $b>0$. Cuando se multiplica al denominador y al numerador por una constante $k > 0$, se obtiene el mismo número aunque la fracción desea distinta: $\frac{n \cdot a}{n \cdot b} = \frac{a}{b}$. Dado $a$ y $b$ naturales con $b>0$, encontrar $c$ y $d$ naturales tal que $\frac{a}{b} = \frac{c}{d}$, y no exitan otros naturales $e$ y $f$ tal que $c > e$, $d > f$, y $\frac{a}{b} = \frac{c}{d} = \frac{e}{f}$.

Por ejemplo: Dada la fracción $\frac{12}{16}$, se cumple que $\frac{6}{8}$ es equivalente pero no la que tiene menor numerador y denominador; en este caso la fracción irreducible es $\frac{3}{4}$.

### Salida

Imprimir $c$ y $d$ separados por un salto de línea.

Por ejemplo: Para $a = 12$ y $b = 16$

Debería imprimir:

> 3  
> 4

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `dd` que representa $a$
- `b` : un número de tamaño `dd` que representa $b$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a dd 12
b dd 16
```
