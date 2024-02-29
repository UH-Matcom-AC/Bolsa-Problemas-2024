# Potencias de 2 en Intervalo (Problema 5)

## Descripción

Dado un número $n$ devolver todas las potencias de $2$ en el intervalo $[a, b]$.

### Salida

Si no hay potencias de $2$ en ese intervalo no imprima nada

Por ejemplo: Para $a = 5$, y $b = 70$

Debería imprimir:

> 8  
> 16  
> 32  
> 64  

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
a dd 5
b dd 70
```
