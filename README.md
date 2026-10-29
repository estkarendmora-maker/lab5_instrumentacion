# lab5_instrumentacion
### Integrantes
Lina María Cortes Almonacid

Karen Dayanna Mora Segura

Sofia Alejandra Cardona Cruz

### Introduccion
En esta práctica de laboratorio se evaluó el funcionamiento de un sistema de monitoreo de variables cardiovasculares y hemodinámicas mediante el uso de un monitor de signos vitales Mindray uMEC 100 y un simulador de oximetría de pulso Pronk OxSim OX-1. Estos equipos permiten estudiar la respuesta de los sistemas de monitorización ante diferentes valores de saturación periférica de oxígeno (SpO₂) y frecuencia del pulso, así como verificar el funcionamiento de sus alarmas [1], [2].

La monitorización de signos vitales es fundamental en el entorno clínico, ya que facilita la identificación de cambios fisiológicos que pueden requerir atención. Entre las variables evaluadas se encuentra la SpO₂, que estima el porcentaje de hemoglobina arterial saturada de oxígeno, y la frecuencia del pulso, expresada en latidos por minuto. La interpretación de estas variables debe considerar las características del paciente, las condiciones de medición y las especificaciones técnicas del equipo [1], [3].

Para el desarrollo de la práctica se empleó el simulador OxSim OX-1, que genera señales ópticas para probar sistemas de pulsioximetría en diferentes condiciones de saturación, frecuencia del pulso y perfusión. Se utilizaron escenarios que representan una frecuencia cardíaca baja, una saturación reducida, valores elevados de saturación y una condición de baja perfusión. Las señales producidas por el simulador se detectaron mediante el sensor de SpO₂ conectado al monitor uMEC 100, permitiendo observar los valores mostrados y la forma de onda fotopletismográfica [2].

Finalmente, se analizó la respuesta del monitor ante los límites de alarma establecidos y se consideró la diferencia entre los valores de referencia del simulador y las lecturas obtenidas. Esta práctica permitió relacionar los conocimientos de instrumentación biomédica, medición fisiológica y verificación funcional de equipos médicos, reconociendo la importancia de evaluar su desempeño antes de utilizarlos en un entorno asistencial.

Objetivo general
- Evaluar el funcionamiento de un monitor de signos vitales Mindray uMEC 100 mediante la simulación de variables cardiovasculares con el Pronk OxSim OX-1, verificando la medición de SpO₂, la frecuencia del pulso, la forma de onda fotopletismográfica y la respuesta de las alarmas.

Objetivos específicos

- Identificar las características y funciones principales del monitor de signos vitales uMEC 100 y del simulador Pronk OxSim OX-1.
- Configurar el monitor para visualizar las variables fisiológicas y las señales requeridas durante la práctica.
- Simular diferentes valores de saturación de oxígeno, frecuencia del pulso e índice de perfusión mediante el OxSim OX-1.
- Verificar la activación de las alarmas del monitor ante valores de SpO₂ y frecuencia del pulso que superen los límites configurados.
- Calcular los errores absolutos y porcentuales entre los valores de referencia del simulador y los valores indicados por el monitor.
- Observar los cambios de la onda fotopletismográfica en condiciones normales y de baja perfusión.
- Analizar las limitaciones del simulador y la importancia de la verificación técnica de los monitores de signos vitales.
## Metodologia 
### Montaje y prueba inicial 
Para realizar la práctica se dispuso de un monitor de signos vitales Mindray uMEC 100 y un simulador de parámetros de oximetría de pulso Pronk OxSim OX-1. Inicialmente, se verificó el estado general de los equipos y se encendió el monitor para acceder a la pantalla de visualización de las variables fisiológicas.

Posteriormente, se conectó el sensor de pulsioximetría al simulador OxSim OX-1, ubicándolo sobre la sección diseñada para simular el dedo. Se seleccionó el modo de simulación requerido y se verificó la compatibilidad del sensor con el simulador. El OxSim genera señales ópticas que permiten comprobar la respuesta del sistema de pulsioximetría sin necesidad de utilizar un paciente real.

Una vez preparado el montaje, se observaron en la pantalla del uMEC 100 los valores de SpO₂ y frecuencia del pulso, junto con la forma de onda fotopletismográfica. Se registraron los valores mostrados para compararlos con los valores de referencia establecidos por el simulador.

##  Configuración y verificación de las variables

Se configuraron diferentes escenarios de simulación de acuerdo con la guía de laboratorio: una condición de SpO₂ de 95 % y frecuencia del pulso de 40 bpm; una condición de SpO₂ de 85 % y frecuencia de 80 bpm; una condición de SpO₂ de 99 % con baja perfusión; y una condición de frecuencia del pulso de 140 bpm con SpO₂ de 98 %.

Para verificar las alarmas, se establecieron los límites de SpO₂ indicados en la guía. Primero, se configuró un límite inferior de 90 % y se observó la respuesta del monitor ante una saturación simulada de 85 %. Después, se configuró un límite superior de 97 % y se evaluó la respuesta ante una saturación simulada de 99 % en modo de baja perfusión. Finalmente, se comprobó la respuesta de la alarma de frecuencia elevada ante una frecuencia simulada de 140 bpm.

En cada escenario se registró si la alarma visual y sonora se activó, así como el tiempo transcurrido hasta su aparición. También se observó si la forma de onda fotopletismográfica presentó cambios o distorsiones durante las simulaciones.

## Cálculo de errores

Para comparar los valores indicados por el monitor con los valores de referencia del simulador, se emplearon el error absoluto y el error porcentual. El error absoluto se calculó mediante la diferencia entre el valor medido y el valor de referencia, mientras que el error porcentual se obtuvo al dividir el error absoluto entre el valor de referencia y multiplicar el resultado por 100.

Las expresiones utilizadas fueron:

Error absoluto = |valor mostrado − valor simulado|

Error porcentual = (error absoluto / valor simulado) × 100

Finalmente, se compararon los resultados de cada escenario para analizar el comportamiento del monitor, la respuesta de las alarmas y las posibles diferencias de medición. Los resultados numéricos y los tiempos de activación deben completarse con los datos registrados durante la sesión experimental.




## Parte A
a. ¿Cómo colocar el uMEC 100 en modo “monitor”?

De acuerdo con el manual de operación de Mindray, el término Monitor corresponde a uno de los modos de filtrado de la señal electrocardiográfica (ECG). Este modo está diseñado para condiciones normales de monitorización y suaviza la señal para facilitar su visualización [1]. 
00-uMEC-Main.docx


El procedimiento es el siguiente:
1. Encender el monitor Mindray uMEC 100 y esperar a que finalice la inicialización.
2. Acceder a la pantalla principal de monitorización.
3. Seleccionar el área de parámetros o la forma de onda del ECG para abrir el menú de configuración.
4. Ingresar a ECG Setup (configuración de ECG).
5. Seleccionar la opción Filter (filtro).
6. Elegir Monitor entre las opciones disponibles.
7. Verificar que la forma de onda del ECG se visualice correctamente y que el filtro seleccionado aparezca indicado en pantalla.
Este ajuste no debe confundirse con un modo general de funcionamiento del monitor: modifica el procesamiento de la señal ECG. La guía de laboratorio utiliza la expresión «modo monitor», por lo que conviene confirmar con el docente si se refiere específicamente a este filtro.


b. ¿Qué tipo de parámetros o variables fisiológicas pueden simularse con el Pronk OxSim OX-1? Explique cada uno?
El Pronk OxSim OX-1 es un simulador óptico diseñado para verificar el funcionamiento de los sistemas de pulsioximetría. Permite generar cinco escenarios predefinidos que combinan diferentes valores de saturación de oxígeno, frecuencia del pulso e índice de perfusión [2], [3].
Las variables que permite simular son:

1. Saturación periférica de oxígeno (SpO₂), unidad en (%)

Representa la proporción estimada de hemoglobina arterial saturada de oxígeno. El OxSim OX-1 dispone de escenarios con saturaciones de 85 %, 95 %, 98 % y 99 %. Estos valores permiten comprobar si el monitor responde correctamente a diferentes niveles de saturación, incluidos valores bajos y altos.

2. Frecuencia del pulso, unidad en (bpm)

Indica la cantidad de pulsaciones detectadas por minuto. El simulador genera frecuencias de 40, 80 y 140 bpm en sus modos predefinidos. Estos valores permiten evaluar la respuesta del monitor ante una frecuencia baja, una frecuencia habitual y una frecuencia elevada.

3. Índice de perfusión (PI)

Es un indicador relacionado con la intensidad de la señal pulsátil periférica detectada por el sensor. El OxSim utiliza un índice aproximado de 2,0 en sus modos habituales y de 0,2 en el modo Low Perfusion. Este último permite evaluar el comportamiento del pulsioxímetro cuando la señal óptica pulsátil es débil.

c. En el ámbito clínico ¿Cuáles son las tolerancias o errores máximos permitidos (EMP) para cada parámetro fisiológico mencionado en la parte (b)?

Para responder esta pregunta correctamente, es necesario distinguir entre la tolerancia del simulador, la precisión del sensor de pulsioximetría y la exactitud del monitor. No existe un único error máximo universal que pueda aplicarse a todos los equipos, sensores y condiciones clínicas.
<img width="1068" height="357" alt="image" src="https://github.com/user-attachments/assets/885c9b9a-c829-4757-aa93-0750d3c82218" />
Las tolerancias de SpO₂ y frecuencia del pulso proceden de la documentación técnica del fabricante del OxSim OX-1 [2], [3]
Consideraciones para la interpretación clínica:
- SpO₂: una tolerancia de ±2 puntos porcentuales alrededor de una referencia de 95 % equivale a un intervalo de 93 % a 97 %. Este ejemplo ilustra la tolerancia numérica, pero no significa que todas las lecturas clínicas deban aceptarse automáticamente dentro de ese intervalo. En condiciones de baja saturación o perfusión deficiente, el desempeño puede cambiar.
- Frecuencia del pulso: si se toma como referencia una frecuencia simulada de 40 bpm y se aplica la tolerancia del simulador de menos de 1 bpm, el intervalo de referencia sería aproximadamente de 39 a 41 bpm. Esta comparación evalúa la salida del simulador; la aceptación de la lectura del monitor debe considerar también su propia especificación.
- Índice de perfusión: no se debe asignar un EMP numérico sin una especificación verificable del fabricante para la variable y el equipo que se están evaluando. En esta práctica, la condición de baja perfusión sirve principalmente para comprobar si el monitor mantiene una lectura y una onda fotopletismográfica interpretables.
El manual de Mindray también establece especificaciones propias para las mediciones del monitor. Por ejemplo, para la frecuencia cardíaca obtenida por ECG, especifica una exactitud de ±1 bpm o ±1 %, el valor que resulte mayor [1]. Esa especificación corresponde a la medición por ECG y no debe confundirse directamente con la exactitud del pulso obtenido por el canal de SpO₂.




## Análisis de resultados  
### Análisis 1: Evalúe estadísticamente las diferencias entre los valores de energía de referencia y suministrados por el desfibrilador  
La evaluación de la energía suministrada por el desfibrilador Mindray BeneHeart D30 permite determinar la correspondencia entre los valores seleccionados durante la configuración del equipo y la energía efectivamente entregada durante la descarga. Para realizar esta comparación, es necesario considerar el error absoluto, el error porcentual y, cuando se dispone de mediciones repetidas, la media y la desviación estándar. Estos indicadores permiten identificar posibles desviaciones sistemáticas y variaciones entre descargas, aspectos fundamentales para verificar el desempeño del desfibrilador y su confiabilidad durante procedimientos de reanimación [6], [7].  

El error absoluto se obtiene mediante la diferencia entre la energía medida y la energía de referencia, expresada en julios (J), mientras que el error porcentual permite determinar la magnitud relativa de esta diferencia. Adicionalmente, la desviación estándar permite establecer la dispersión de las mediciones respecto al promedio. De acuerdo con los criterios de exactitud de la norma IEC 60601-2-4, se considera una tolerancia de ±15 % o ±3 J, tomando el valor mayor, respecto a la energía nominal correspondiente a las condiciones de prueba [7]. Por esta razón, no basta con comprobar que el desfibrilador realiza una descarga, sino que también resulta necesario verificar que la energía entregada se encuentre dentro de los límites establecidos.  

Las diferencias que puedan presentarse entre la energía seleccionada y la medida pueden relacionarse con la impedancia de la carga de prueba, las características de la forma de onda bifásica y las tolerancias propias del sistema de medición. El BeneHeart D30 emplea una forma de onda bifásica truncada exponencial con compensación de impedancia, por lo que las condiciones eléctricas de la prueba deben considerarse al interpretar los resultados [8]. En consecuencia, la evaluación estadística permite establecer la exactitud y repetibilidad del equipo, aunque la determinación de su conformidad requiere comparar los resultados experimentales con las especificaciones del fabricante.  


### Análisis 2: Describa la relación entre la forma de onda que se visualiza en el  D30 y la frecuencia cardíaca/saturación periférica de oxígeno   
La visualización de las señales fisiológicas en el desfibrilador Mindray BeneHeart D30 permite relacionar las características temporales de las ondas con los parámetros de frecuencia cardíaca (FC) y saturación periférica de oxígeno (SpO₂). En el caso del electrocardiograma, la frecuencia cardíaca se determina principalmente a partir del intervalo entre complejos QRS consecutivos. Cuando la frecuencia aumenta, los intervalos R-R disminuyen y los complejos aparecen más próximos entre sí; por el contrario, cuando la frecuencia disminuye, aumenta la separación temporal entre los latidos. Esta relación facilita la identificación de condiciones como bradicardia y taquicardia durante la monitorización [8].  

Por otra parte, la onda fotopletismográfica asociada a la medición de SpO₂ representa las variaciones de volumen sanguíneo periférico producidas por cada pulsación arterial. La frecuencia de repetición de sus pulsos permite estimar la frecuencia del pulso, mientras que la saturación de oxígeno se calcula mediante el análisis de la absorción de luz roja e infrarroja por la hemoglobina. Por lo tanto, la SpO₂ no se obtiene directamente de la altura de la onda, sino del procesamiento de las señales ópticas captadas por el sensor [9].  

En condiciones de baja perfusión, la amplitud de la señal fotopletismográfica puede disminuir, dificultando la identificación de los pulsos y generando fluctuaciones en las mediciones. Asimismo, factores como el movimiento, la circulación periférica reducida y la colocación inadecuada del sensor pueden afectar la estabilidad de la señal y la confiabilidad de los valores mostrados [9]. De esta manera, la observación conjunta de las ondas de ECG y pletismografía permite complementar la interpretación de la frecuencia cardíaca y la saturación de oxígeno, así como reconocer posibles alteraciones o interferencias durante el monitoreo.  



## Discusión  
**• Pregunta 1: ¿Cuál es el principio de operación del Pronk OxSim OX-1 para simular una onda pulsátil?**  

El simulador Pronk OxSim OX-1 funciona mediante un principio de simulación óptica que permite reproducir las señales luminosas asociadas al flujo sanguíneo pulsátil, con el propósito de evaluar el funcionamiento de los sistemas de pulsioximetría. Su operación consiste en detectar los pulsos de luz roja e infrarroja emitidos por el sensor de SpO₂, bloquearlos y generar nuevas señales ópticas controladas que representan las variaciones de absorción de luz producidas por la sangre arterial durante cada ciclo cardíaco [10].

El dispositivo utiliza una combinación de mecanismos electrónicos, ópticos y mecánicos para reproducir diferentes condiciones fisiológicas mediante la modificación de la frecuencia de pulsación, la saturación de oxígeno y el índice de perfusión. De esta manera, el monitor interpreta las señales generadas por el simulador como si provinieran del tejido de un paciente. Este principio se fundamenta en la relación entre los componentes pulsátiles (AC) y no pulsátiles (DC) de las señales roja e infrarroja, cuya comparación permite estimar la saturación periférica de oxígeno [10].

El OxSim OX-1 dispone de cinco modos de simulación preestablecidos que permiten representar diferentes condiciones fisiológicas, incluyendo bradicardia, taquicardia, disminución de la saturación y baja perfusión. Estos escenarios facilitan la verificación de la precisión de las mediciones y del funcionamiento de las alarmas de los monitores de signos vitales [11].

**• Pregunta 2: ¿Por qué la SpO2 baja puede ser un falso positivo (falsa alarma) en una situación de mala perfusión?**  

Una lectura baja de SpO₂ puede generar una falsa alarma durante una situación de mala perfusión debido a que la pulsioximetría depende de la detección de las variaciones de volumen sanguíneo arterial en el tejido periférico. Cuando existe una reducción del flujo sanguíneo, como puede ocurrir durante hipotensión, vasoconstricción o disminución de la circulación periférica, la amplitud de la señal fotopletismográfica disminuye, dificultando la identificación de su componente pulsátil [12].

En estas condiciones, la señal detectada por el sensor puede presentar una menor relación señal-ruido, lo que aumenta la posibilidad de interferencias y errores en el cálculo de la saturación de oxígeno. Como consecuencia, el monitor puede mostrar valores inferiores a los reales, generar lecturas inestables o activar una alarma de desaturación, aunque la oxigenación arterial del paciente no haya disminuido verdaderamente. Sin embargo, una lectura baja durante la mala perfusión no siempre constituye una falsa alarma, ya que también puede corresponder a una hipoxemia real [12].

En el caso del Pronk OxSim OX-1, el modo Low Perfusion permite evaluar este comportamiento mediante la simulación de una saturación de oxígeno del 99 %, una frecuencia de pulso de 80 bpm y un índice de perfusión aproximado de 0,2. Este último valor representa una señal pulsátil de baja intensidad, que puede dificultar la medición de algunos oxímetros. Por lo tanto, las diferencias observadas entre el valor programado y el registrado por el monitor pueden relacionarse con la capacidad del equipo y del sensor para procesar señales de baja amplitud [10], [11].



## Conclusión


## Bibliografia
[1] Shenzhen Mindray Bio-Medical Electronics Co., Ltd., uMEC10/uMEC12/uMEC15 Patient Monitor Operator’s Manual, ene. 2016. [En línea]. 

[2] Pronk Technologies, OxSim SpO₂ Simulator: Operator’s Manual, Rev. O, 18 jul. 2017. [En línea]. 

[3] Pronk Technologies, “OX-1 OxSim® Optical SpO₂ Pulse Oximeter Simulator,” ficha técnica del fabricante. [En línea]. 

[4] International Organization for Standardization (ISO), ISO 80601-2-61:2026: Medical electrical equipment—Part 2-61: Particular requirements for basic safety and essential performance of pulse oximeter equipment, 3.ª ed., abr. 2026. [En línea]. 

[5] U.S. Food and Drug Administration (FDA), “Pulse Oximeters,” información sobre el uso, la precisión y las limitaciones de los pulsioxímetros. [En línea].

[6] Fluke Biomedical. (s. f.). Impulse 7000DP defibrillator analyzer. Fluke Biomedical. https://www.flukebiomedical.com/products/defibrillator-analyzers/impulse-7000dp-defibrillator-analyzer

[7] International Electrotechnical Commission. (2010). Medical electrical equipment—Part 2-4: Particular requirements for the basic safety and essential performance of cardiac defibrillators (IEC 60601-2-4:2010). IEC. https://www.chamber.org.il/media/159674/%D7%98%D7%99%D7%95%D7%98%D7%94-%D7%9C%D7%AA%D7%A7%D7%9F-60601-24.pdf

[8] Shenzhen Mindray Bio-Medical Electronics Co., Ltd. (2025). BeneHeart D30 series defibrillator/monitor: Service manual (Rev. 7.0). https://www.mindray.com/content/dam/xpace/en_gb/resources/downloads/education/education-d30-d60/0656B_International%20Mindray%20%28Non-FDA%29%20Service%20Manual_Full%201.pdf

[9] U.S. Food and Drug Administration. (2025). Pulse oximeters. https://www.fda.gov/medical-devices/products-and-medical-procedures/pulse-oximeters


