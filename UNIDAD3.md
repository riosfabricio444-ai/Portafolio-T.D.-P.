<div align="center">

# [UNIDAD 3](SEMESTRE.md)
</div>

## Modularidad

La modularidad es un principio de la programación estructurada que consiste en dividir un programa grande y complejo en partes más pequeñas, independientes y manejables, llamadas módulos (funciones o procedimientos).
En lugar de escribir todo el código como un bloque único, el programador descompone el problema general en subproblemas más simples —la técnica de "divide y vencerás"— y resuelve cada uno con un módulo separado. Luego, esos módulos se combinan y se comunican entre sí (normalmente mediante el envío de parámetros y valores de retorno) para lograr el funcionamiento completo del programa.

## Ventajas:

**Reutilización de código** — un módulo ya hecho se puede usar varias veces sin reescribirlo.

**Facilidad de mantenimiento** — si hay un error o cambio, solo se toca el módulo afectado, no todo el programa.

**Mayor legibilidad** — el código organizado en módulos con nombres claros es más fácil de entender.

**Depuración simplificada** — es más sencillo encontrar y corregir errores probando cada módulo por separado.

## Tipos de pases de parametros:

**Paso por valor**

Es la forma de enviar parámetros a un módulo (función) en la que se envía una copia del valor de la variable, no la variable original. Dentro de la función se trabaja con esa copia, que ocupa una dirección de memoria distinta a la de la variable original. Por eso, cualquier cambio que se haga dentro de la función NO afecta a la variable que se envió desde el programa principal. Es la forma de paso de parámetros que se usa por defecto en la mayoría de los lenguajes (C, C++, Java, etc.) cuando no se indica lo contrario, y se utiliza cuando la función solo necesita leer o procesar un dato sin la intención de modificarlo.

**Paso por referencia**

Es la forma de enviar parámetros en la que, en lugar de una copia, se envía la dirección de memoria (referencia) de la variable original. Esto hace que la función trabaje directamente sobre la misma variable del programa principal. Por eso, cualquier cambio que se haga dentro de la función SÍ afecta a la variable original. En C++ se implementa colocando el símbolo & antes del nombre del parámetro. Se utiliza cuando la función necesita modificar el dato original o devolver más de un resultado.

## Arreglos

Un arreglo (o array) es una estructura de datos que permite almacenar varios valores del mismo tipo bajo un solo nombre de variable, guardados en posiciones de memoria contiguas (una al lado de la otra). Cada valor dentro del arreglo se llama elemento, y se accede a él mediante un índice (un número que indica su posición), que casi siempre empieza en 0.
Piénsalo como una fila de casilleros numerados: todos los casilleros tienen el mismo nombre de "mueble" (el arreglo), pero cada uno guarda un dato distinto, y para sacar algo de un casillero específico solo necesitas decir su número (índice).

## Ventajas:

**Organización de datos** — permiten almacenar varios valores del mismo tipo bajo un solo nombre de variable.

**Acceso rápido y directo** — se puede acceder a cualquier elemento de inmediato usando su índice.

**Facilidad para recorrer datos** — se pueden recorrer fácilmente con bucles (for, while) para sumar, buscar o comparar.

**Ahorro de código** — evitan crear muchas variables individuales, usando en su lugar una sola estructura para todos los datos.

## Tipos de arreglos:

**Arreglo unidimensional (vector)**

Es el tipo de arreglo más simple. Almacena los elementos en una sola fila o lista, y se necesita un solo índice para acceder a cada elemento. Se puede imaginar como una lista de casilleros numerados uno tras otro. Se usa para guardar datos simples relacionados, como una lista de nombres o de calificaciones.

**Arreglo bidimensional (matriz)**

Almacena los elementos organizados en filas y columnas, formando una tabla. Se necesitan dos índices para acceder a un elemento: uno indica la fila y otro la columna. Se usa para representar datos con dos criterios de organización, como un tablero de juego o una hoja de cálculo.

**Arreglo tridimencional (multidimensional)**

Es una generalización del concepto anterior, donde el arreglo tiene tres o más dimensiones. Se puede imaginar como varias matrices apiladas (capas), y se requieren tantos índices como dimensiones tenga el arreglo. Se usa para representar datos más complejos, con varios criterios de clasificación al mismo tiempo, como capas, filas y columnas.

## Principales dificultades en la aplicación de los contenidos

Al desarrollar este trabajo sobre modularidad y arreglos, una de las principales dificultades que encontré fue comprender con claridad la diferencia entre el paso de parámetros por valor y por referencia. Al inicio me costaba entender por qué, si ambos parecían "enviar" el mismo dato a la función, en un caso el valor original cambiaba y en el otro no. Tuve que revisar varios ejemplos y comparar la ejecución paso a paso para darme cuenta de que la clave está en si se envía una copia del dato o la dirección de memoria donde este se encuentra. Una vez que entendí esa idea, pude ver con más claridad por qué en ciertos programas es necesario usar el símbolo & cuando se quiere que una función modifique realmente la variable original.

En cuanto a los arreglos, la mayor dificultad no estuvo en los arreglos unidimensionales, ya que su lógica es bastante intuitiva (una lista de datos con un solo índice), sino en los arreglos bidimensionales y, sobre todo, en los multidimensionales. Al trabajar con matrices tuve que practicar bastante el uso de bucles anidados, porque al principio me confundía el orden en que debía recorrer las filas y columnas para no dejar datos sin llenar o acceder a posiciones incorrectas. Con los arreglos de tres dimensiones la dificultad aumentó, ya que tuve que imaginar el arreglo como si fueran varias matrices apiladas (capas), lo cual no es tan sencillo de visualizar mentalmente como ocurre con un simple vector o una tabla de dos dimensiones.

## Reflexión crítica 

Como reflexión crítica, considero que estos dos temas —modularidad y arreglos— están estrechamente relacionados y se complementan constantemente en la programación real, ya que es muy común que los módulos reciban arreglos como parámetros. En esos casos, entender bien la diferencia entre paso por valor y por referencia se vuelve fundamental, pues enviar un arreglo completo por valor resultaría poco eficiente en términos de memoria. La experiencia de programar estos ejercicios en clase me permitió confirmar que la teoría por sí sola no es suficiente: es necesario escribir el código, ejecutarlo, cometer errores y corregirlos para realmente interiorizar cómo se comportan los parámetros y cómo se recorren los distintos tipos de arreglos. En definitiva, considero que la práctica constante fue la que marcó la diferencia entre simplemente memorizar los conceptos y llegar a comprenderlos de buena forma.

<div align="center">
  
#### [Clic aquí para regresar📂](SEMESTRE.md)
</div>
