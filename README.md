# lab5_instrumentacion
### Integrantes
Lina María Cortes Almonacid

Karen Dayanna Mora Segura

Sofia Alejandra Cardona Cruz

### Introduccion
En esta práctica se evaluó el desempeño técnico y funcional de un monitor de signos vitales Mindray uMEC 100 mediante un simulador óptico de pulsioximetría Pronk OxSim OX-1. En el entorno clínico es fundamental que estos monitores midan de forma continua la saturación periférica de oxígeno (SpO₂) y la frecuencia de pulso, y que generen alarmas cuando las variaciones representen un peligro inmediato para el paciente [1], [2]. Como no es posible ni ético inducir hipoxia o arritmias en una persona para verificar estas funciones, se usan simuladores que reproducen condiciones fisiológicas y patológicas conocidas [3].

El OxSim OX-1 se conecta a la pinza del monitor y reproduce cinco combinaciones predefinidas de saturación, frecuencia de pulso e índice de perfusión (PI) [3]. Con estas se puede comprobar si el monitor muestra valores dentro de su exactitud declarada, si dispara las alarmas al cruzar los límites configurados y cómo se comporta la onda fotopletismográfica ante una perfusión baja. La exactitud del uMEC 100 en SpO₂ está especificada por el fabricante [2], y el desempeño de los pulsioxímetros se evalúa bajo la norma ISO 80601-2-61 y las recomendaciones de la FDA [4], [5].

La práctica permitió operar un monitor multiparamétrico, configurar alarmas, calcular errores absolutos y porcentuales, e identificar las limitaciones de un simulador óptico frente a la complejidad de un paciente real.

Objetivo general

*Operar el simulador Pronk OxSim OX-1 y el monitor de signos vitales uMEC 100 para realizar pruebas funcionales de medición y de alarmas.

Objetivos específicos

*Identificar los modos de operación de un simulador de parámetros hemodinámicos (Pronk OxSim OX-1) y poner el uMEC 100 en modo “monitor”.
*Verificar los límites de medición y la activación de alarmas del monitor mediante la simulación de SpO₂ y frecuencia de pulso.
*Calcular los errores absoluto y porcentual de cada variable frente a los valores simulados.
*Interpretar las variaciones de la onda fotopletismográfica y de los parámetros asociadas a estados fisiológicos y patológicos (bradicardia, taquicardia, hipoxia, baja perfusión).

## Metodologia 
### Montaje y prueba inicial 
Se construyó primero una tabla de verificación de alarmas con las columnas límite configurado (alto/bajo), valor simulado, alarma activa (sí/no) y tiempo de respuesta. Luego se encendió el uMEC 100, se seleccionó el modo “monitor” y se conectó la pinza de SpO₂ al OxSim. Con el simulador en cada modo se registraron los valores del monitor y la forma de onda, y se calcularon los errores:

Error absoluto = |valor mostrado − valor simulado|

Error porcentual = (error absoluto / valor simulado) × 100

Las pruebas siguieron este orden:

*Bradicardia (40 lpm, SpO₂ 95 %): comparación de valores y registro de la onda.

*Límite inferior de SpO₂ ajustado a 90 %, luego simulación de 80 lpm y SpO₂ 85 %: se contaron 5 s y se verificó la alarma sonora y visual.

*Límite superior de SpO₂ ajustado a 97 %, luego simulación de SpO₂ 99 % con baja perfusión: se contaron 5 s, se verificó la alarma y se observó si la onda se distorsionaba.

*SpO₂ 98 % con taquicardia (140 lpm): se registró la onda y se verificó si se disparaba la alarma de frecuencia elevada.

*Documentar el procedimiento y los resultados en un repositorio de GitHub con trabajo colaborativo.

## Parte A
a. ¿Cómo colocar el uMEC 100 en modo “monitor”?

El modo de monitoreo es el modo clínico más usado para vigilar pacientes. No requiere ningún comando: el uMEC 100 entra en él automáticamente al encenderse. El manual describe otros tres modos que se deben distinguir de este:
<img width="1062" height="506" alt="image" src="https://github.com/user-attachments/assets/93c52a61-f65a-42f2-a758-c1a7c0eb5c42" />


b. ¿Qué tipo de parámetros o variables fisiológicas pueden simularse con el Pronk OxSim OX-1? Explique cada uno?
El OX-1 es un simulador óptico de SpO₂ con cinco modos fijos (Modo 1: 85 %, 80 lpm, PI ≈ 2,0; Modo 2: 95 %, 40 lpm, PI ≈ 2,0; Modo 3: 98 %, 80 lpm, PI ≈ 2,0; Modo 4: 98 %, 140 lpm, PI ≈ 2,0; Modo 5: 99 %, 80 lpm, PI ≈ 0,2). Simula tres variables: 
medwrench

Saturación de oxígeno (SpO₂): el porcentaje de hemoglobina oxigenada en sangre arterial. Valores de 85 % representan hipoxemia y de 98 a 99 %, un valor normal o alto.
Frecuencia de pulso (PR): los latidos por minuto percibidos ópticamente. Se simula 40 lpm (bradicardia), 80 lpm (normal) y 140 lpm (taquicardia). Es frecuencia de pulso, no ECG, así que el monitor la mostrará como PR derivada de SpO₂.
Índice de perfusión (PI): la relación entre la señal pulsátil y la no pulsátil. En el Modo 5 es ≈ 0,2, que representa baja perfusión.
c. En el ámbito clínico ¿Cuáles son las tolerancias o errores máximos permitidos (EMP) para cada parámetro fisiológico mencionado en la parte (b)?

<img width="1056" height="166" alt="image" src="https://github.com/user-attachments/assets/810076b2-6e86-43d9-9b5f-58ae5159915a" />

El datasheet del uMEC 100 declara que el módulo de SpO₂ cumple la norma ISO 80601-2-61 y tiene una exactitud de ±2 % en adultos y pediátricos y ±3 % en neonatos entre 70 y 100 %. La precisión para pulso es de ±3 lpm entre 20 y 300 lpm cuando proviene de SpO₂. La exactitud de ±1 lpm o ±1 % para frecuencia cardíaca aparece en los datasheets de la familia (±1 lpm o ±1 %, el mayor). Verifícala en la sección ECG del datasheet del uMEC 100, porque yo la leí en documentos de modelos hermanos. 
fd604b9f 5f6f 4df2 970d 70f284a1a772 1784126750597
 +2

La referencia regulatoria para SpO₂ es la guía de la FDA para pulsioxímetros, que recomienda las pruebas de la cláusula 201.12.1 de la norma ISO 80601-2-61. En la práctica los pulsioxímetros recientes autorizados por la FDA tienen una exactitud (Arms) de 2 a 3 % respecto a gasometría arterial. Un artículo en PMC recuerda que un Arms ≤ 3 % en el rango 70–100 % es el criterio aceptado por ISO y FDA. 
GUIDANCE DOCUMENT
 +2

Todos los valores del OX-1 (85 a 99 %) caen dentro del rango especificado (70–100 %), así que los ±2 % son un criterio válido para tus tablas. Dos matices:

Norma ISO. La edición ISO 80601-2-61:2017 aparece como retirada y tiene una nueva edición, ISO 80601-2-61:2026. Menciona ambas si la citas. 
iso
Tolerancia del simulador. No encontré la tolerancia propia del OX-1, y los errores que calcules incluyen la del simulador. Búscala en su manual de operación.


