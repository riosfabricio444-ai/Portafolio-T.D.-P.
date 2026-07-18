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

## Principales dificultades y reflexión crítica en la aplicación de los contenidos.

<div align="center">
  
#### [Clic aquí para regresar📂](SEMESTRE.md)
</div>
