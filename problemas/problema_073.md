# Nacimiento según CI (Problema 73)

Dado un número de CI devolver la fecha de nacimiento.

### Salida

Para la salida debe imprimir día, mes y año, cada valor separado por espacio.

Por ejemplo: para el caso donde $n = 98052833456$ la salida por consola debe tener la siguiente forma:

> 28 05 1998

## Logisim

Se dispondrá en *INPUT* los datos de entrada a partir de la dirección $0$. La entrada se estructura de la siguiente forma:

- $w_0$ : $n$

## SASM

En la sección `.data` se deben definir los valores de entrada de la siguiente forma:

- `n` : un número de tamaño `dw` que representa $n$

Por ejemplo:

```
section .data
n dw 98052833453
```