<div align="center">

# [UNIDAD 2](SEMESTRE.md)
</div>

# 1. ESTRUCTURAS CONDICIONALES

* ## Condicional Simple (if):
​Es una estructura de decisión de una sola vía. Se utiliza para ejecutar un bloque de código únicamente si se cumple un requisito específico. Si la condición no se cumple, el programa no hace nada y continúa con su curso normal sin ejecutar ninguna acción alternativa.

**Diagrama de flujo:**

<img width="841" height="481" alt="image" src="https://github.com/user-attachments/assets/7489770a-5255-4dd1-bb1d-910a571c9cab" />


**Pseudocodigo:**

<img width="837" height="469" alt="image" src="https://github.com/user-attachments/assets/0be5f1c3-f3f7-47e3-8537-6deda17306b3" />


* ## ​Condicional Doble (if - else):
​Es una estructura de exclusión mutua que divide el flujo del programa en dos caminos posibles y obligatorios. Si la condición es verdadera, se ejecuta el primer bloque de código; si es falsa, se ejecuta automáticamente el bloque alternativo. Garantiza que se hará una acción u otra, pero nunca ambas a la vez.

**Diagrama de flujo:**

<img width="833" height="519" alt="image" src="https://github.com/user-attachments/assets/ff00ddb9-34b3-408d-8ebc-1fc423397343" />


**Pseudocodigo:**

<img width="841" height="527" alt="image" src="https://github.com/user-attachments/assets/98bafed1-80eb-4e7a-858d-c6b26824845e" />


* ## Condicional Múltiple (switch):
​Es una estructura de selección de caminos múltiples. Evalúa el valor de una sola variable y lo compara directamente con una lista de opciones fijas llamadas casos (case). Al encontrar la opción idéntica, ejecuta el bloque correspondiente. Se usa para evitar acumular demasiados if seguidos cuando se crean menús.

**Diagrama de flujo:**

<img width="836" height="445" alt="image" src="https://github.com/user-attachments/assets/136d171b-f68f-4c9e-ab4b-9225d135544b" />


**Pseudocodigo:**

<img width="849" height="517" alt="image" src="https://github.com/user-attachments/assets/935ce272-6584-41d5-8b88-7a89f9eac303" />


# 2. ESTRUCTURAS REPETITIVAS

* ## Estructura (while):
​Es un ciclo cuya duración es indeterminada porque depende de factores externos. Su característica principal es que evalúa la condición antes de entrar al bucle (filtro de entrada). Si la condición es falsa desde el inicio, el bloque de código interno no se ejecuta ninguna vez.

**Diagrama de flujo:**

<img width="800" height="576" alt="image" src="https://github.com/user-attachments/assets/450722cd-f80a-44fa-b178-fe7ad22c5a3b" />


**Pseudocodigo:**

<img width="801" height="461" alt="image" src="https://github.com/user-attachments/assets/55a3f03a-8eab-4828-8d3e-5ff008199176" />


* ## Estructura (do - while):
Es un ciclo que realiza la evaluación de la condición al final (filtro de salida). Esto garantiza que el bloque de código se ejecutará al menos una vez, sin importar si la condición es verdadera o falsa al comenzar. Se utiliza mucho para obligar al usuario a ingresar datos válidos.

**Diagrama de flujo:**

<img width="818" height="552" alt="image" src="https://github.com/user-attachments/assets/ee974e3d-d121-4505-ab1c-0fd684d8ae27" />


**Pseudocodigo:**

<img width="807" height="428" alt="image" src="https://github.com/user-attachments/assets/23967ae6-5af7-47e2-8a67-e2089110fb8c" />


* ## Estructura (for): 
Es una estructura repetitiva determinada. Se utiliza exclusivamente cuando el programador conoce con total exactitud cuántas vueltas va a dar el ciclo antes de que este comience. Utiliza una variable contadora interna que controla de forma automática el inicio, el límite y el incremento en cada vuelta.

**Diagrama de flujo:**

<img width="808" height="478" alt="image" src="https://github.com/user-attachments/assets/92b607e2-7098-4c42-a545-99a2dc6025fd" />


**Pseudocodigo:**

<img width="798" height="464" alt="image" src="https://github.com/user-attachments/assets/2002095d-de76-4262-bf1f-38c734afa7a8" />


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

| **DATOS DE ENTRADA** | **PROCESO** | **SALIDA** |
| :--- | :---| :--- |
|Ingresar la canditad de vehículos que los visitaron. Después elegir el tipo de combustible: ingresar 1 = Extra o 2 = Súper y tambien la cantidad de galones que va a comprar, esto lo realizara para cada vehiculo que los visitó | Calcular el valor a pagar del combustible, que se lo hace multiplicando el número de galones (dependiendo del tipo de combustible que eligió) por el precio que es: Extra = 2.50 o Super = 4.00, si el cliente compra mas de 15 galones hacerle el descuento del 10%, además calcular todo el dinero de las ventas y el total de galones súper |Mostrar el descuento y el total a pagar de cada vehículo, además el programa debe mostrarme todo el dinero recaudado de las ventas y la candidad de galones súper que se vendieron.|

* ## Diseño del algoritmo (diagrama de flujo):

<img width="871" height="1349" alt="image" src="https://github.com/user-attachments/assets/9bb552ae-83fd-49ad-91ea-c932a699cfe7" />


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
        }else{
            Pago = b *  4;
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

    printf("--------------------------------------\n");
    printf("El total de dinero recaudado es : %.2f\n", Recaudado);
    printf("Cantidad de galones Super vendidos en el dia es: %2.f\n", Super);

    return 0;
}
```
* ## Validación (prueba de escritorio):

**Prueba de escritorio:**

<img width="865" height="680" alt="image" src="https://github.com/user-attachments/assets/d9ab3316-e12a-404f-8a9f-052cb24da6f4" />


**Prueba en el terminal:**

<img width="860" height="631" alt="image" src="https://github.com/user-attachments/assets/52772f62-88c7-41de-8af5-285759ad911b" />


# 4. PRINCIPALES DIFICULTADES Y REFLEXIÓN CRÍTICA EN LA APLICACIÓN DE LOS CONTENIDOS

### Principales Dificultades:

- **Errores de sintaxis en C:** Al principio me costó adaptarme a las reglas estrictas del lenguaje, como olvidar el punto y coma (;) al final de las líneas, no cerrar correctamente las llaves ({}) o confundir los formatos en el scanf (usar %d en vez de %f).

- **Confundir = con ==:** Me pasaba mucho que ponía un solo signo igual dentro del if (ej. if(tipo = 1)). Tardé en asimilar que para comparar se usa obligatoriamente el doble igual (==), y que un solo igual altera el valor de la variable.

- **Control de acumuladores y bucles:** A veces olvidaba inicializar los acumuladores en cero (total = 0.0) antes de empezar el ciclo, lo que hacía que el programa arrastrara datos basura de la memoria. También llegué a generar bucles infinitos por no actualizar bien los contadores.

### Reflexión Crítica:

- Esta unidad me enseñó que programar no es memorizar código, sino desarrollar lógica para resolver problemas. Antes de esto, mis programas eran planos y lineales; ahora entiendo cómo darle autonomía al software para que tome decisiones y repita tareas de forma eficiente.

- Aprender a elegir el ciclo correcto (como el for cuando conozco el límite o el while cuando es indeterminado) me ayudó a entender cómo optimizar los recursos de la computadora y a ser mucho más ordenado al estructurar un algoritmo.

 <div align="center">
	 
#### [Clic aquí para regresar📂](SEMESTRE.md)
