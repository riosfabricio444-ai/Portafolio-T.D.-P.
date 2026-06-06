<div align="center">

# [UNIDAD 1](PORTAFOLIO.md)
</div>

# Contenidos
* ## Algoritmo:
Es un conjunto de instrucciones o reglas definidas, no ambiguas, ordenadas y finitas que permiten solucionar un problema, realizar un cómputo o procesar datos.
- Características: Debe ser finito (tener un fin), preciso (orden de pasos claro) y definido (si se sigue dos veces con los mismos datos, se obtiene el mismo resultado).
- Fases: Todo algoritmo consta de una Entrada (datos iniciales), un Proceso (operaciones lógicas) y una Salida (resultados finales).
* ## Pseudocódigo (PSeInt):
Es una descripción de alto nivel de un algoritmo que emplea una mezcla de lenguaje natural con algunas convenciones sintácticas propias de lenguajes de programación.
- Utilidad: Facilita la transición de la idea lógica al código real (como C o Java). Es una herramienta clave para el programador porque permite concentrarse en la solución lógica sin preocuparse por los errores de sintaxis del compilador.
* ## Diagrama de Flujo:
Representación gráfica de un algoritmo mediante una serie de símbolos estandarizados que se conectan a través de flechas (líneas de flujo).

Simbología Técnica: 
- Óvalos: Inicio y Fin del programa.
- Paralelogramos: Entrada y Salida de datos (Lectura/Escritura).
- Rectángulos: Procesos, cálculos o asignación de variables.
- Rombos: Toma de decisiones o estructuras de control.
* ## Prueba de escritorio:
Es una técnica de validación manual para verificar la fidelidad de un algoritmo. Consiste en simular la ejecución del programa en papel, asignando valores a las variables y siguiendo el flujo de las instrucciones para comprobar si los resultados de salida coinciden con lo esperado según el planteamiento del problema.
* ## Lenguaje de Programación (Lenguaje C):
Es un lenguaje de programación de propósito general, considerado de "medio nivel" porque combina elementos de lenguajes de alto nivel con la funcionalidad del lenguaje ensamblador.
- Importancia: Es el lenguaje base de la computación moderna. Requiere una gestión manual de tipos de datos (int, float, char) y una estructura de bloques definida por llaves { } y finalización de instrucciones con punto y coma ;.

* ## Programación por Bloques:
La programación por bloques es una metodología visual que permite estructurar algoritmos mediante el uso de piezas gráficas interconectadas. Este enfoque elimina las barreras de la sintaxis compleja (como puntos y comas o llaves) para centrarse exclusivamente en la lógica de control y el flujo secuencial de la solución.

Importancia en el aprendizaje:
- Abstracción: Permite visualizar los procesos lógicos como unidades funcionales.
- Estructura: Facilita la comprensión de cómo se encadenan las instrucciones: Entrada -> Proceso -> Salida.
- Prevención de errores: Al ser piezas que encajan entre sí, se reducen los errores de estructura lógica.

Un ejemplo de una app es Scratch:
<img width="1903" height="1029" alt="image" src="https://github.com/user-attachments/assets/fdb7f735-d8ac-4ceb-9292-321f9a8c84db" />

# Ejercicio con estructura secuencial

## 1. Planteamiento del Problema
Una tienda ofrece un descuento del 15% sobre el valor total de la compra. Realizar un programa que reciba el monto de la compra y muestre el valor del descuento y el precio final a pagar.
## 2. Análisis del Problema 
*  Datos de entrada:
   - Monto de la compra
*  Proceso:
   - Descuento = (Compra * 15) /100
   - Precio_final = Compra - Descuento
* Salida:
   - Total del Descuento
   - Precio final a pagar
   
## 3. Diseño del algoritmo
* ## Pseudocódigo:
```
Algoritmo Descuento_de_compra
	// Variables
	Definir Compra, Descuento, Precio_Final Como Real;
	// Datos de entrada
	Escribir "Ingrese el monto total de la compra: ";
	Leer Compra;
	// Proceso
	Descuento = (Compra*15)/100;
	Precio_Final = Compra-Descuento;
	// salida
	Escribir "El valor de descuento es de: ", Descuento;
	Escribir "El precio final a pagar es de: ", Precio_Final;
FinAlgoritmo
```
* ## Diagrama de flujo:
<img width="565" height="678" alt="image" src="https://github.com/user-attachments/assets/8ea1f994-0908-4fb8-84f1-68a8b73d5e14" />

## 4. Codificación (Lenguaje C) 
```c
#include <stdio.h>

int main(){
    //Variables
    float Compra, Descuento, Total_Pagar;
    //Datos de entrada
    printf("Ingrese el monto total de la compra: ");
    scanf("%f",&Compra);
    //Proceso
    Descuento = (Compra * 15)/100;
    Total_Pagar = Compra - Descuento;
    //Salida
    printf("El valor de descuento es de: %.2f\n", Descuento);
    printf("el valor final a pagar es de: %.2f\n ",Total_Pagar);

    return 0;
}
```
## 5. Validación (prueba  de escritorio)
* Lenguaje C:
<img width="715" height="114" alt="image" src="https://github.com/user-attachments/assets/ba925093-88d5-43b8-8c5c-27075ea4b491" />


*  PSeInt
<img width="610" height="442" alt="image" src="https://github.com/user-attachments/assets/ab29a1f7-62eb-4029-865d-25550c264f8a" />


*  Escrito
<img width="868" height="197" alt="image" src="https://github.com/user-attachments/assets/6b5b938a-5414-4d6d-85c6-d63e79d325f1" />

# Principales dificultades y reflexión crítica en la aplicación de los contenidos. 
* ## Dificultades:
  - El manejo inicial de la plataforma GitHub y la sintaxis Markdown representó un reto técnico para lograr una correcta visualización y organización de la carátula y los contenidos.
  - Se presentó dificultad al modelar el problema del descuento, asegurando que la jerarquía de las operaciones fuera la correcta para garantizar resultados precisos.
* ## Reflexión crítica:
  - El estudio de esta unidad me ha permitido entender que la programación es un proceso metódico de análisis y no solo escritura de código. Aprender a diseñar algoritmos y diagramas de flujo antes de programar es fundamental para reducir errores de lógica. Considero que dominar las estructuras secuenciales es la base crítica para desarrollar un pensamiento computacional sólido y eficiente, habilidades clave para mi formación en la carrera de Computación.
