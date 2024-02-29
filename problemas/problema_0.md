# Nombre (Problema 0)

## Descripción

< Descripción del Problema >

### Salida

< Consideraciones Finales >

Por ejemplo: < EJEMPLO >

Debería imprimir:

> valor 1 impreso  
> valor 2 impreso  

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $param$
- $w_{k:l}$ : $param_array$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dd` que representa $param$
- `array` : un array de números de tamaño `dw` que representa $param_array$

Por ejemplo, un posible encabezado podría ser:

```
section .data
n dd 12
array dw 23, 56, 98, 14
```
