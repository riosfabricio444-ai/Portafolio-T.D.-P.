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
### Ejemplo:
```c
#include <stdio.h>

// Recibe una copia de la energía actual y devuelve el valor tras correr
int gastarEnergia(int energiaActual, int costo) {
    energiaActual = energiaActual - costo;
    return energiaActual; 
}

// Recibe una copia de la energía y la devuelve con el plus de la poción
int usarPocion(int energiaActual) {
    energiaActual = energiaActual + 25;
    return energiaActual;
}

// Módulo para ver el estado actual en pantalla
void mostrarEstado(int energiaFinal) {
    printf("--- ESTADO DEL JUGADOR ---\n");
    printf("Energía restante: %d%%\n", energiaFinal);
    printf("--------------------------\n");
}

int main() {
    int miEnergia = 80; 
    int carrera = 30;   

    // Como es paso por valor, tenemos que guardar el resultado de vuelta en 'miEnergia'
    miEnergia = gastarEnergia(miEnergia, carrera); 
    miEnergia = usarPocion(miEnergia);                 

    mostrarEstado(miEnergia);

    return 0;
}
```

## Paso por referencia

Consiste en enviar la **dirección de memoria** de la variable.

- ✅ La función trabaja directamente sobre la variable original.
- ✅ Los cambios realizados sí se reflejan fuera de la función.
- ✅ En C++ se representa mediante el símbolo **&**.

> 📌 **Resultado:** cualquier modificación realizada dentro de la función **SÍ afecta** a la variable original.

---
### Ejemplo:

```c
#include <stdio.h>

// Módulo que aplica el descuento directamente usando un puntero (*)
void aplicarDescuento(double *precioTotal, double rebaja) {
    *precioTotal = *precioTotal - rebaja; 
}

void aplicarIVA(double *precioTotal) {
    *precioTotal = *precioTotal * 1.15;
}

void mostrarTicket(double precioFinal) {
    printf("--- TICKET DE COMPRA ---\n");
    printf("Total a pagar: $%.2f\n", precioFinal);
    printf("------------------------\n");
}

int main() {
    double miCompra = 100.0; 
    double descuento = 20.0;

    aplicarDescuento(&miCompra, descuento); 
    aplicarIVA(&miCompra);                 

    // Mostramos el resultado final ya modificado
    mostrarTicket(miCompra);

    return 0;
}
```
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
### Ejemplo:
```c
#include <stdio.h>

// Módulo para analizar todas las notas del alumno
void analizarNotas(float notas[6]) {
    float suma = 0.0;
    float maxima = notas[0];
    float minima = notas[0];

    for(int i = 0; i < 6; i++) {
        suma = suma + notas[i]; // Sumamos para el promedio
        
        if(notas[i] > maxima) {
            maxima = notas[i]; // Guardamos la más alta
        }
        if(notas[i] < minima) {
            minima = notas[i]; // Guardamos la más baja
        }
    }

    float promedio = suma / 6.0;

    printf("--- REPORTE DEL SEMESTRE ---\n");
    printf("Nota mas alta: %.1f\n", maxima);
    printf("Nota mas baja: %.1f\n", minima);
    printf("Promedio final: %.1f\n", promedio);
    
    if(promedio >= 7.0) {
        printf("Estado: APROBADO\n");
    } else {
        printf("Estado: REPROBADO\n");
    }
}

int main() {
    // Una sola lista con las 6 notas del estudiante
    float misNotas[6] = {8.5, 9.0, 6.5, 7.0, 10.0, 5.5};

    // Llamamos al módulo enviando el arreglo completo
    analizarNotas(misNotas);

    return 0;
}
```

##  Arreglo bidimensional (Matriz)

Organiza los datos en **filas y columnas**.

- 📌 Requiere dos índices.
- 📌 Representa tablas, tableros o hojas de cálculo.

---
### Ejemplo:
```c
#include <stdio.h>

// Módulo que calcula el total recaudado por cada tipo de producto
void calcularVentasPorProducto(double ventas[3][4]) {
    printf("--- TOTAL DE VENTAS POR PRODUCTO ---\n");
    
    // El primer ciclo recorre cada producto (filas)
    for(int producto = 0; producto < 3; producto++) {
        double totalProducto = 0.0;
        
        // El segundo ciclo recorre los días de la expo (columnas)
        for(int dia = 0; dia < 4; dia++) {
            totalProducto = totalProducto + ventas[producto][dia];
        }
        
        printf("Producto #%d - Recaudado total: $%.2f\n", producto + 1, totalProducto);
    }
}

int main() {
    // Matriz de 3 productos x 4 dias de ventas
    double matrizVentas[3][4] = {
        {120.00, 150.50, 90.00, 200.00},  // Producto 1 (Audífonos)
        {450.00, 300.00, 520.00, 600.00},  // Producto 2 (Teclados)
        {80.25,  95.00,  110.00, 85.50}    // Producto 3 (Mousepads)
    };

    // Enviamos la tabla completa al módulo para que haga las cuentas
    calcularVentasPorProducto(matrizVentas);

    return 0;
}
```
##  Arreglo tridimensional (Multidimensional)

Es una extensión de las matrices.

- 📌 Contiene tres o más dimensiones.
- 📌 Puede imaginarse como varias matrices apiladas.
- 📌 Se utiliza para representar información más compleja.

---
### Ejemplo:
```
#include <stdio.h>

// Módulo que revisa todo el cine para contar los asientos vendidos
void revisarOcupacionCine(int cine[2][3][4]) {
    int totalCine = 0;

    // Recorremos las salas (profundidad)
    for(int sala = 0; sala < 2; sala++) {
        int ocupadosEnSala = 0;

        // Recorremos las filas de esa sala
        for(int fila = 0; fila < 3; fila++) {
            // Recorremos las columnas de esa fila
            for(int columna = 0; columna < 4; columna++) {
                
                // Si encontramos un 1, es un boleto vendido
                if(cine[sala][fila][columna] == 1) {
                    ocupadosEnSala++;
                    totalCine++;
                }
            }
        }
        printf("Sala %d: %d asientos ocupados.\n", sala + 1, ocupadosEnSala);
    }

    printf("----------------------------------\n");
    printf("Total de boletos vendidos en el cine: %d\n", totalCine);
}

int main() {
    // Cubo de datos de [2 salas] x [3 filas] x [4 columnas]
    int mapaCine[2][3][4] = {
        { // SALA 1
            {1, 0, 1, 0}, // Fila 0
            {0, 1, 1, 1}, // Fila 1
            {0, 0, 0, 1}  // Fila 2
        },
        { // SALA 2
            {0, 0, 1, 1}, // Fila 0
            {1, 1, 0, 0}, // Fila 1
            {1, 0, 1, 0}  // Fila 2
        }
    };

    // Mandamos el cubo completo al módulo para analizar la asistencia
    revisarOcupacionCine(mapaCine);

    return 0;
}
```c

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
