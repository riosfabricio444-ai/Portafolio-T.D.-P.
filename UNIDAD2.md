<div align="center">

# [UNIDAD 2](SEMESTRE.md)
</div>

# 1. ESTRUCTURAS CONDICIONALES

* ## Condicional Simple (if):
​Es una estructura de decisión de una sola vía. Se utiliza para ejecutar un bloque de código únicamente si se cumple un requisito específico. Si la condición no se cumple, el programa no hace nada y continúa con su curso normal sin ejecutar ninguna acción alternativa.

**Diagrama de flujo:**

<img width="593" height="365" alt="image" src="https://github.com/user-attachments/assets/5eed1619-0cda-43f3-8e99-568fc50d3a8a" />


**Pseudocodigo:**

* ## ​Condicional Doble (if - else):
​Es una estructura de exclusión mutua que divide el flujo del programa en dos caminos posibles y obligatorios. Si la condición es verdadera, se ejecuta el primer bloque de código; si es falsa, se ejecuta automáticamente el bloque alternativo. Garantiza que se hará una acción u otra, pero nunca ambas a la vez.

**Diagrama de flujo:**

<img width="642" height="376" alt="image" src="https://github.com/user-attachments/assets/a835d2a5-3294-4a56-b017-795b51f21020" />


**Pseudocodigo:**

* ## Condicional Múltiple (switch):
​Es una estructura de selección de caminos múltiples. Evalúa el valor de una sola variable y lo compara directamente con una lista de opciones fijas llamadas casos (case). Al encontrar la opción idéntica, ejecuta el bloque correspondiente. Se usa para evitar acumular demasiados if seguidos cuando se crean menús.

**Diagrama de flujo:**

<img width="1143" height="530" alt="image" src="https://github.com/user-attachments/assets/64396f81-098c-4e58-8d41-6a730fcb5cd9" />



**Pseudocodigo:**

# 2. ESTRUCTURAS REPETITIVAS

* ## Estructura (while):
​Es un ciclo cuya duración es indeterminada porque depende de factores externos. Su característica principal es que evalúa la condición antes de entrar al bucle (filtro de entrada). Si la condición es falsa desde el inicio, el bloque de código interno no se ejecuta ninguna vez.

**Diagrama de flujo:**

<img width="506" height="398" alt="image" src="https://github.com/user-attachments/assets/1f05f702-3216-44fb-84b0-d6b2ccea616f" />


**Pseudocodigo:**

* ## Estructura (do - while):
Es un ciclo que realiza la evaluación de la condición al final (filtro de salida). Esto garantiza que el bloque de código se ejecutará al menos una vez, sin importar si la condición es verdadera o falsa al comenzar. Se utiliza mucho para obligar al usuario a ingresar datos válidos.

**Diagrama de flujo:**

<img width="441" height="387" alt="image" src="https://github.com/user-attachments/assets/f4ad02b0-1211-4ae4-94a9-3a34211ee6a6" />


**Pseudocodigo:**

* ## Estructura (for): 
Es una estructura repetitiva determinada. Se utiliza exclusivamente cuando el programador conoce con total exactitud cuántas vueltas va a dar el ciclo antes de que este comience. Utiliza una variable contadora interna que controla de forma automática el inicio, el límite y el incremento en cada vuelta.

**Diagrama de flujo:**

<img width="379" height="267" alt="image" src="https://github.com/user-attachments/assets/cd7e796f-a25e-46be-893e-1e16b5cff3dd" />


**Pseudocodigo:**


# 3. EJERCICIO CON ESTRUCTURA CONDICIONAL Y REPETITIVA

* ## Planteamiento de problema:

Una gasolinera desea automatizar el control de sus ventas diarias. El operario de la estación debe registrar las cargas de N cantidad de vehículos que visitan la estación en un turno.

Para cada vehículo, se debe ingresar:

- El tipo de combustible que va a tanquear (usando un número: 1 para Extra, 2 para Súper).
- La cantidad de galones que desea comprar.

Los precios por galón son los siguientes:

- Gasolina Extra (Tipo 1): $2.50 por galón.
- Gasolina Súper (Tipo 2): $4.00 por galón.
- 
Además, la gasolinera tiene una promoción: si el cliente compra más de 15 galones (de cualquier combustible), se le otorga un descuento del 10% sobre el valor total de su compra; si compra 15 galones o menos, paga el valor total neto.

El programa debe calcular y mostrar cuánto paga cada vehículo. Al finalizar el turno (cuando se hayan procesado los N vehículos), el sistema debe mostrar el total de dinero recaudado por la gasolinera y la cantidad total de galones de gasolina Súper que se vendieron en el día.

* ## Análisis del problema:

| **DATOS DE ENTRADA** | **PROCESO** | SALIDA |
| :--- | :---| :--- |
|  Elegir el tipo de combustible,1=Extra o 2 = Super, y tambien la cantidad de galones que va a comprar.| Calcular el valor a pagar del combustible, que se lo hace multiplicando rl numero de galones por el precio dependiendo del tipo de combustible que eligió|Mostar el total a pagar de cada vehículo  |
|  | | |

* ## Diseño del algoritmo (diagrama de flujo):


<img width="610" height="804" alt="image" src="https://github.com/user-attachments/assets/854fbda8-7caa-4e07-b948-2dc0b721ba75" />


* ## Codificación (código C):

```
#include <stdio.h>

int main (){

    int N, i, a, b;
    float Pago, Descuento, Total_a_Pagar, Recaudado = 0, Super = 0;

    printf("Ingrese el numero total de vehiculos que ingresaron en el dia:");
    scanf("%i", &N);


    for(i=1; i<=N; i++){
        printf("vehiculo %i:\n",i);

        do{
            printf("Tipo de combustible: 1 = Extra o 2 = Super:");
            scanf("%i", &a);
        }while(a < 1 || a > 2);

        do{
            printf("Cantidad de galones a comprar:");
            scanf("%i", &b);
        }while(b<1);

        if(a == 1){
            Pago = b * 2.50;
            printf("El precio total de galones extras a pagar es:%.2f\n", Pago);
        }else{
            Pago = b *  4;
            printf("El precio total de galones Super a pagar es:%.2f\n", Pago);
        }

        if(b>15){
            Descuento = Pago * 0.10;
        }else{
            Descuento = 0;
        }


        Total_a_Pagar = Pago - Descuento;
        Recaudado = Recaudado + Total_a_Pagar;

        printf("Descuento aplicado: %.2f\n",Descuento);
        printf("Total a pagar por vehiculo: %.2f\n", Total_a_Pagar);


        if(a == 2){
            Super = Super + b;
        }
    }

    printf("El total de dinero recaudado es : %.2f\n", Recaudado);
    printf("Cantidad de galones Super vendidos en el dia es: %2.f\n", Super);

    return 0;
}
```
* ## Validación (prueba de escritorio):

# 4. PRINCIPALES DIFICULTADES Y REFLEXIÓN CRÍTICA EN LA APLICACIÓN DE LOS CONTENIDOS

### Principales Dificultades:

​**Errores de sintaxis en C:** Al principio me costó adaptarme a las reglas estrictas del lenguaje, como olvidar el punto y coma (;) al final de las líneas, no cerrar correctamente las llaves ({}) o confundir los formatos en el scanf (usar %d en vez de %f).

​**Confundir = con ==:** Me pasaba mucho que ponía un solo signo igual dentro del if (ej. if(tipo = 1)). Tardé en asimilar que para comparar se usa obligatoriamente el doble igual (==), y que un solo igual altera el valor de la variable.

​**Control de acumuladores y bucles:** A veces olvidaba inicializar los acumuladores en cero (total = 0.0) antes de empezar el ciclo, lo que hacía que el programa arrastrara datos basura de la memoria. También llegué a generar bucles infinitos por no actualizar bien los contadores.

### Reflexión Crítica:

​Esta unidad me enseñó que programar no es memorizar código, sino desarrollar lógica para resolver problemas. Antes de esto, mis programas eran planos y lineales; ahora entiendo cómo darle autonomía al software para que tome decisiones y repita tareas de forma eficiente.

​Aprender a elegir el ciclo correcto (como el for cuando conozco el límite o el while cuando es indeterminado) me ayudó a entender cómo optimizar los recursos de la computadora y a ser mucho más ordenado al estructurar un algoritmo.

 <div align="center">
	 
#### [Clic aquí para regresar📂](SEMESTRE.md)
