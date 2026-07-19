<div align="center">

# 📚 [UNIDAD 3](SEMESTRE.md)

### 💻 Modularidad y Arreglos

*"Organizar el código es el primer paso para construir programas claros, eficientes y fáciles de mantener."*

</div>

---

# 🧩 Modularidad

La **modularidad** es un principio de la programación estructurada que consiste en dividir un programa grande y complejo en partes más pequeñas e independientes, llamadas **módulos** (funciones o procedimientos).

En lugar de escribir todo el programa en un solo bloque, el problema se divide en tareas más simples (**"divide y vencerás"**). Cada módulo resuelve una parte específica y, posteriormente, todos trabajan juntos mediante el intercambio de **parámetros** y **valores de retorno**.

> 💡 **Objetivo:** hacer programas más organizados, reutilizables y fáciles de comprender.

---

# ✅ Ventajas de la modularidad

| 🚀 Ventaja | 📖 Descripción |
|------------|----------------|
| ♻️ **Reutilización de código** | Un mismo módulo puede utilizarse varias veces sin volver a escribirlo. |
| 🔧 **Mantenimiento sencillo** | Si existe un error, solo se modifica el módulo correspondiente. |
| 📖 **Mayor legibilidad** | El código organizado es más fácil de leer y comprender. |
| 🐞 **Depuración simplificada** | Permite encontrar errores probando cada módulo por separado. |

---

# 🔄 Tipos de paso de parámetros

## Paso por valor

Consiste en enviar **una copia** del valor de la variable a la función.

- ✅ La función trabaja con una copia.
- ✅ La variable original **no cambia**.
- ✅ Se utiliza cuando únicamente se necesita leer o procesar un dato.

> 📌 **Resultado:** cualquier modificación realizada dentro de la función **NO afecta** al dato original.

---

## Paso por referencia

Consiste en enviar la **dirección de memoria** de la variable.

- ✅ La función trabaja directamente sobre la variable original.
- ✅ Los cambios realizados sí se reflejan fuera de la función.
- ✅ En C++ se representa mediante el símbolo **&**.

> 📌 **Resultado:** cualquier modificación realizada dentro de la función **SÍ afecta** a la variable original.

---

# 📊 Arreglos

Un **arreglo (array)** es una estructura de datos que permite almacenar múltiples valores del mismo tipo bajo un solo nombre de variable.

Cada elemento posee un **índice**, que generalmente comienza en **0**, permitiendo acceder rápidamente a cualquier posición.

> 🗂️ **Ejemplo:** un arreglo puede imaginarse como una fila de casilleros numerados donde cada casillero almacena un dato diferente.

---

# 🌟 Ventajas de los arreglos

| 🚀 Ventaja | 📖 Descripción |
|------------|----------------|
| 📦 Organización | Agrupan varios datos bajo una sola variable. |
| ⚡ Acceso rápido | Permiten acceder inmediatamente mediante índices. |
| 🔄 Recorrido sencillo | Se procesan fácilmente con ciclos como `for` o `while`. |
| 💻 Menos código | Evitan declarar muchas variables individuales. |

---

# 📚 Tipos de arreglos

## Arreglo unidimensional (Vector)

Es el arreglo más sencillo.

- 📌 Se organiza en una sola fila.
- 📌 Utiliza un único índice.
- 📌 Ideal para listas de nombres, edades o calificaciones.

---

##  Arreglo bidimensional (Matriz)

Organiza los datos en **filas y columnas**.

- 📌 Requiere dos índices.
- 📌 Representa tablas, tableros o hojas de cálculo.

---

##  Arreglo tridimensional (Multidimensional)

Es una extensión de las matrices.

- 📌 Contiene tres o más dimensiones.
- 📌 Puede imaginarse como varias matrices apiladas.
- 📌 Se utiliza para representar información más compleja.

---

# ⚠️ Principales dificultades encontradas

Durante el desarrollo de esta unidad encontré diversas dificultades.

### 🔹 Modularidad

La mayor dificultad fue comprender la diferencia entre el **paso por valor** y el **paso por referencia**. Al principio ambos parecían realizar la misma función, pero después de analizar varios ejemplos comprendí que la diferencia está en si se envía una **copia del dato** o su **dirección de memoria**.

---

### 🔹 Arreglos

Con los arreglos unidimensionales no tuve mayores inconvenientes; sin embargo, las matrices y los arreglos multidimensionales resultaron más complejos.

Las principales dificultades fueron:

- 🔸 Utilizar correctamente los bucles anidados.
- 🔸 Recorrer filas y columnas sin cometer errores.
- 🔸 Visualizar mentalmente un arreglo de tres dimensiones como varias matrices superpuestas.

Gracias a la práctica constante logré comprender mejor su funcionamiento.

---

# 💭 Reflexión crítica

Considero que la **modularidad** y los **arreglos** son dos conceptos que trabajan de manera conjunta en prácticamente cualquier programa.

Los módulos suelen recibir arreglos como parámetros, por lo que comprender el paso por valor y por referencia resulta indispensable para escribir programas eficientes.

Más allá de la teoría, comprobé que la mejor forma de aprender fue **programando**, ejecutando los ejercicios, identificando errores y corrigiéndolos.

> 🎯 En conclusión, la práctica constante fue el factor que me permitió transformar los conceptos teóricos en conocimientos realmente comprendidos y aplicables.

---

<div align="center">

## 🌟 Conclusión

> *"Un programa bien organizado no solo funciona mejor, sino que también es más fácil de comprender, mantener y mejorar."* 💻✨

</div>
<div align="center">
  
#### [Clic aquí para regresar📂](SEMESTRE.md)
</div>
