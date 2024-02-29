# Máximo Común Divisor (Problema 11)

## Descripción

Sean $a$ y $b$ dos números enteros tal que $a, b > 0$. Se dice que si $c > 0$, divide a $a$, y a $b$, entonces $c$ es común divisor de $a$ y $b$. Dados dos números $a,b > 0$ halle $c$ tal que este sea el mayor de los comunes divisores de $a$ y $b$. Por ejemplo, $48$ y $60$ tienen a $6$ como común divisor, sin embargo, no es el mayor; en este caso el máximo común divisor es $12$.

### Salida

Imprimir el máximo común divisor de $a$ y $b$

Por ejemplo: Para $a = 48$ y $b = 60$

Debería imprimir:

> 12

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $a$
- $w_1$ : $b$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `a` : un número de tamaño `dw` que representa $a$
- `b` : un número de tamaño `dw` que representa $b$

Por ejemplo, un posible encabezado podría ser:

```
section .data
a dw 48
b dw 60
```
