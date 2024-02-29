# División de Fracciones (Problema 80)

## Descripción

Dado dos fracciones $a/b$ y $c/d$, se desea calcular la división de estas fracciones, y además simplificar el resultado. Para enteder como se debe simplificar una fracción consulte [Problema 13 (Simplificar Fracción)](/problemas/problema_013.md).

### Salida

Imprima el numerador y el denominador del resultado simplificado, separados por un espacio.

Por ejemplo: Para $a=3$, $b=2$, $c=4$ y $d=6$

Debería imprimir:

> 9 4

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$
- $w_2$ : $c$
- $w_3$ : $d$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `dd` que representa $a$
- `b` : un número de tamaño `dd` que representa $b$
- `c` : un número de tamaño `dd` que representa $c$
- `d` : un número de tamaño `dd` que representa $d$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a dd 3
b dd 2
c dd 4
d dd 6
```
