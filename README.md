# Bolsa-Problemas-2024

Primer Proyecto de Arquitectura de Computadoras.

*Facultad de Matemática y Computación  
Universidad de La Habana  
Curso 2024*

## Consideraciones Generales

Este proyecto consiste en dar solución a problemas computacionales utilizando Máquinas de Estados Algorítmicas (ASM) empleando circuitos simulados en *Logisim*, y utilizando el Lenguaje Ensamblador *NASM*.

Según el ejercicio indiciado se debe hacer dos implementaciones:

- La primera consistirá en una ASM que se debe implmentar sobre la plantilla [BigASM](./plantilla_logisim/BigASM.circ).

- La segunda implementación consiste en generar un archivo `.asm` con el código en ensamblador *NASM* que dé solución al problema.

Se deben tener en cuenta las consideraciones generales para *Logisim* y *NASM* dadas en este documento, y las consideraciones particulares por cada uno de los problemas.

**IMPORTANTE**: Por cada ejercicio debe entregar la solución en seudocódigo, la solución en Logisim (basado en la plantilla), y la solución en esnamblador (`.asm`). Sin embargo, puede incluir los diagramas de flujo de la Máquina de Estados Algorítmica, e incluso las Tablas de Asignaciones.

## Logisim

Se dispondrá de una plantilla en Logisim para realizar la implemetación de la Máquina de Estados Algorítmica. Queda prohibida la modficación de cualquiera de los circuitos salvo `BIG ASM`, en cuyo caso sí se deben respetar las entradas y salidas dadas. Además NO puede utilizar las componentes `RAM`, ni `ROM`, así como los circuitos `INPUT` y `MEMORY`. Una vez que termine la ejecución del programa debe activar la salida `END` (como se explicará más adelante), y mantener dicho esta persistente hasta que se haga un reinicio manual.

Esta plantilla cuentas con 4 circuitos principales, y 3 secundarios que se explicarán a continuación.

### Circuitos Principales

Los circuitos principales que se usarán para la implementación de la ASM son:

- `INPUT`: Una memoria de solo lectura con los datos de entrada para el circuito. Cada dirección de memoria indiza una palabra de tamaño de 4 bytes (32 bits). Las direcciones de memoria son de 24 bits; por lo tanto se tienen $2^{24}$ datos de 32 bits almacenados.

- `MEMORY`: Una memoria de lectura y escritura. Tiene las mismas características que la memoria `INPUT`, solo que también permite guardar información.  

- `BOARD BIG ASM`: Circuito que integra las componentes `INPUT`, `MEMORY`, y `BIG ASM`, con una pantalla. En esta última se debe proyectar la salida de la Máquina de Estados Algorítmica que se implemente.

- `BIG ASM`: Circuito de la Máquina de Estado Algorítmica que se debe implementar. Solo tiene definida cada una de las entradas y salidas.
    - `DIR INPUT`: Salida de 24 bits. Dirección del dato de la Memoria `INPUT` que se desea leer.
    - `DATA INPUT`: Entrada de 32 bits. Dato en la dirección que indica `DIR INPUT`, almacenado en la Memoria `INPUT`.
    - `DIR MEMORY`: Salida de 24 bits. Dirección en la Memoria `MEMORY`, de la palabra en donde se desea escribir o se desea leer.
    - `Write MEMORY`: Salida de 1 bit. Indica si se desea escribir en `MEMORY` (1), o si se desea leer de `MEMORY` (0).
    - `MEMORY OUT`: Salida de 32 bits. Dato que se desea guardar en la dirección `DIR MEMORY` de `MEMORY`.
    - `MEMORY IN`: Entrada de 32 bits. Dato en la dirección que indica `DIR INPUT`, almacenado en `MEMORY`.
    - `ASCII`: Salida de 7 bits. Caracter del sistema ASCII que se desea imprimir por la pantalla.
    - `Write ASCII`: Salida de 1 bit. Indica si se desea escribir en pantalla en carcater que está en `ASCII` (1), o si no se desea imprimir nada (0).
    - `END`: Salida de 1 bit. Indica si el programa ya terminó (1), o si aún no lo ha hecho (0).
    - `CLR`: Entrada de 1 bit. Clásico *Reset*. Reinicia el sistema. Además mientras se mantenga en (1) no debe empezar la ejecución de la máquina. Cuando cambia a (0) debe comenzar la ejecución.
    - `CLK`: Entrada de 1 bit. Entrada del Reloj.

En `INPUT` siempre se dispondrá de los valores inciales, y se asegura que serán consistentes para cada problema. Debido a la estructura de `INPUT`, se añade la siguiente notación para hacer referencia a cada palabra en dicha memoria.

- $w_i$: indica la palabra (de tamaño 4 bytes), que se encuentra en la dirección $i$ de la memoria `INPUT`.
- $w_{i:j}$: indica el array de palabras que se encuentran desde la direccioón $i$ de `INPUT`, hasta la dirección $j$.

Por simplicidad, tanto `INPUT` como `MEMORY` no necesitan esperar ciclos de reloj para leer un dato particular. En el caso de la escritura en `MEMORY`, solo se necesita de un *Rising Edge* para guardar un dato en una dirección específica.

### Circuitos Secundarios

Como es necesario imprimir en la pantalla proporcionada se brindan dos circuitos que facilitan la escritura de números enteros con signo (`PRINT DEC`) o sin signo (`PRINT UDEC`).

Estos circuitos son *ASMs* que reciben el número que se desea imprimir, y se activan con la entrada `start`. Cuando ambos inician se debe esperar a que termine la escritura en pantalla, que no es más que esperar a que la salida `END` de estos circuitos, se active. Se debe tener en cuenta que ambos circuitos están diseñados para mostrar su estado de finalización durante solamente un ciclo del reloj; por lo tanto preste atención a dicha salida.

Adicionalmente se dispone del circuito `TEST PRINT` para que pruebe y se familiarice con el funcionamiento de los circuitos `PRINT DEC` y `PRINT UDEC`.

## NASM

Solo se permitirá utilizar las subrutinas y macros externas definidas en `io.inc`. Cualquier subrutina que emplee, debe ser implementada. En la section `.data` se pueden definir tantos valores constantes como se desee, pero debe agregar los nombres de constantes que se especifican en cada problema, ya que la entrada se dispondrá de dicha forma. Por lo tanto si un problema exige las entradas `A` (número) y el array `lista`, debe definir estas en dicha sección con dicho nombre.

En la sección `.bss` puede definir el espacio en memoria que necesite con algún fin específico. Sin embargo, se prefiere utilizar más la *Pila*, y solo cuando sea necesario, la sección `.bss`.

El código de la implementación se debe desarrollar en la sección `.text`. Para los llamados de subrutina se recomienda utilizar la convención de llamada *cdecl* (C declaration). Lo esencial de este convenio es que la función que realiza el llamado a la subrutina es la encargada de pasar los parámetros a la pila, y limpiarla al retorno. Implementar bien este convenio permite el llamado directo desde el lenguaje C y C++. Si lo desea puede implementar otro convenio como *stdcall*; pero debe saber explicar el convenio implementado.

## Lista de Problemas

001. [Problema 1 (N Perfectos)](./problemas/problema_001.md)
002. [Problema 2 (N Primos)](./problemas/problema_002.md)
003. [Problema 3 (I-ésimo Primo)](./problemas/problema_003.md)
004. [Problema 4 (I-ésimo Perfecto)](./problemas/problema_004.md)
005. [Problema 5 (Potencias de 2 en Intervalo)](./problemas/problema_005.md)
006. [Problema 6 (I-ésimo Término de Fibonacci)](./problemas/problema_006.md)
007. [Problema 7 (I-ésimo Término de Tribonacci)](./problemas/problema_007.md)
008. [Problema 8 (I,J-ésimo Término de Ackermann)](./problemas/problema_008.md)
009. [Problema 9 (I-ésimo Término de Collatz)](./problemas/problema_009.md)
010. [Problema 10 (Divisores Primos)](./problemas/problema_010.md)
011. [Problema 11 (Máximo Común Divisor)](./problemas/problema_011.md)
012. [Problema 12 (Mínimo Común Múltiplo)](./problemas/problema_012.md)
013. [Problema 13 (Simplificar Fracción)](./problemas/problema_013.md)
014. [Problema 14 (Suma de Fracciones)](./problemas/problema_014.md)
015. [Problema 15 (Decimal a Base A)](./problemas/problema_015.md)
016. [Problema 16 (Base A a Decimal)](./problemas/problema_016.md)

017. [Problema 17 (Divisibilidad)](./problemas/problema_017.md)
018. [Problema 18 (Mínimo de un array)](./problemas/problema_018.md)
019. [Problema 19 (Máximo de un array)](./problemas/problema_019.md)
020. [Problema 20 (Máximo de un array en intervalo)](./problemas/problema_020.md)
021. [Problema 21 (Mínimo de un array en intervalo)](./problemas/problema_021.md)
022. [Problema 22 (Insertion Sort A-Z)](./problemas/problema_022.md)
023. [Problema 23 (Bubble Sort A-Z)](./problemas/problema_023.md)
024. [Problema 24 (Media de un array)](./problemas/problema_024.md)
025. [Problema 25 (Varianza de un array)](./problemas/problema_025.md)
026. [Problema 26 (Moda de un array)](./problemas/problema_026.md)
027. [Problema 27 (Repeticiones en Array)](./problemas/problema_027.md)
028. [Problema 28 (Suma de n menores que x)](./problemas/problema_028.md)
029. [Problema 29 (Sumando y obteniendo x)](./problemas/problema_029.md)
030. [Problema 30 (Suma de nodos en arbol)](./problemas/problema_030.md)

031. [Problema 31 ()](./problemas/problema_031.md)
032. [Problema 32 ()](./problemas/problema_032.md)
033. [Problema 33 ()](./problemas/problema_033.md)
034. [Problema 34 ()](./problemas/problema_034.md)
035. [Problema 35 ()](./problemas/problema_035.md)
036. [Problema 36 ()](./problemas/problema_036.md)
037. [Problema 37 ()](./problemas/problema_037.md)
038. [Problema 38 ()](./problemas/problema_038.md)
039. [Problema 39 ()](./problemas/problema_039.md)
040. [Problema 40 ()](./problemas/problema_040.md)
041. [Problema 41 ()](./problemas/problema_041.md)
042. [Problema 42 ()](./problemas/problema_042.md)
043. [Problema 43 ()](./problemas/problema_043.md)
044. [Problema 44 ()](./problemas/problema_044.md)
045. [Problema 45 ()](./problemas/problema_045.md)

046. [Problema 46 (Recorrido en Preorden)](./problemas/problema_046.md)
047. [Problema 47 (Recorrido en Inorden)](./problemas/problema_047.md)
048. [Problema 48 (Recorrido en Postorden)](./problemas/problema_048.md)
049. [Problema 49 (Build Heap)](./problemas/problema_049.md)
050. [Problema 50 (Insertar en ABB)](./problemas/problema_050.md)
051. [Problema 51 (Intersección de Conjuntos)](./problemas/problema_051.md)
052. [Problema 52 (Unión de Conjuntos)](./problemas/problema_052.md)
053. [Problema 53 (Diferencia de Conjuntos)](./problemas/problema_053.md)
054. [Problema 54 (Producto Vectorial)](./problemas/problema_054.md)
055. [Problema 55 (Norma de un Vector)](./problemas/problema_055.md)
056. [Problema 56 (Raíz de N)](./problemas/problema_056.md)
057. [Problema 57 (Rotar Matriz)](./problemas/problema_057.md)
058. [Problema 58 (Dentro de un Triángulo)](./problemas/problema_058.md)
059. [Problema 59 (Pertenece a la Recta)](./problemas/problema_059.md)
060. [Problema 60 (En qué lado de la Recta?)](./problemas/problema_060.md)

061. [Problema 61 (Factorial)](./problemas/problema_061.md)  
062. [Problema 62 (Moda de un array)](./problemas/problema_062.md)  
063. [Problema 63 (Polinomios)](./problemas/problema_063.md)  
064. [Problema 64 (Palíndromos)](./problemas/problema_064.md)  
065. [Problema 65 (Substring)](./problemas/problema_065.md)  
066. [Problema 66 (Merge Sort)](./problemas/problema_066.md)  
067. [Problema 67 (Ordenacion)](./problemas/problema_067.md)  
068. [Problema 68 (Contando Bits)](./problemas/problema_068.md)  
069. [Problema 69 (Contando Bits y Paridad)](./problemas/problema_069.md)  
070. [Problema 70 (Alternando Bits)](./problemas/problema_070.md)  
071. [Problema 71 (Daditos)](./problemas/problema_071.md)  
072. [Problema 72 (Colitas)](./problemas/problema_072.md)  
073. [Problema 73 (Nacimiento según CI)](./problemas/problema_073.md)  
074. [Problema 74 (Género según CI)](./problemas/problema_074.md)  
075. [Problema 75 (Fecha Válida)](./problemas/problema_075.md)  
076. [Problema 76 (Altura Máxima)](./problemas/problema_076.md)  
077. [Problema 77 (Suma y Resta en Árbol)](./problemas/problema_077.md)  
078. [Problema 78 (Producto de Fracciones)](./problemas/problema_078.md)  
079. [Problema 79 (Resta de Fracciones)](./problemas/problema_079.md)  
080. [Problema 80 (División de Fracciones)](./problemas/problema_080.md)  
081. [Problema 81 (Máximos por intervalos)](./problemas/problema_081.md)  
082. [Problema 82 (Altura Mínima)](./problemas/problema_082.md)  
083. [Problema 83 (Cantidad de Nodos)](./problemas/problema_083.md)  
084. [Problema 84 (Ramita Fuerte)](./problemas/problema_084.md)  
085. [Problema 85 (Triángulo Rectángulo)](./problemas/problema_085.md)  
086. [Problema 86 (Cajero)](./problemas/problema_086.md)  
087. [Problema 87 (Rectas que se cortan)](./problemas/problema_087.md)  
088. [Problema 88 (Rectas que son paralelas)](./problemas/problema_088.md)  
089. [Problema 89 (Circunferencia)](./problemas/problema_089.md)  
090. [Problema 90 (Cubo)](./problemas/problema_090.md)  
091. [Problema 91 (Cilindro)](./problemas/problema_091.md)  
092. [Problema 92 (Pirámide)](./problemas/problema_092.md)  
093. [Problema 93 (Esfera)](./problemas/problema_093.md)  
094. [Problema 94 (Ortoedro)](./problemas/problema_094.md)  
095. [Problema 95 (Insertion Sort++ Z-A)](./problemas/problema_095.md)  
096. [Problema 96 (Mayor Substring)](./problemas/problema_096.md)  
097. [Problema 97 (Paridad en un array)](./problemas/problema_097.md)  
098. [Problema 98 (Bubble Sort++ Z-A)](./problemas/problema_098.md)  
099. [Problema 99 (Array en Array)](./problemas/problema_099.md)  
100. [Problema 100 (Mínima Transformación)](./problemas/problema_100.md)  

