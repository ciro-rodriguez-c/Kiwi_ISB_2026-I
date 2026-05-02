## Introducción

En este laboratorio se realizó la adquisición y análisis de señales ECG bajo diferentes condiciones fisiológicas, con el objetivo de evaluar cómo varía la actividad cardíaca frente a cambios en la respiración y la actividad física. Se registraron señales en estado basal, durante ciclos controlados de respiración (incluyendo hiperventilación e hipoventilación), y posterior a la realización de ejercicio físico (en nuestro caso, burpees).
Adicionalmente, se analizaron la primera, segunda y tercera derivada de la señal ECG (I, II y III), con el fin de resaltar características relevantes de la señal. Este enfoque permite una mejor identificación de patrones fisiológicos en la dinámica cardíaca.

---

## Análisis de resultados
### Señal basal

Los resultados muestran que el filtrado aplicado logra limpiar la señal EKG y conservar sus componentes principales. En los tres registros se identifican complejos QRS claros y una concentración de energía principalmente en bajas frecuencias, lo cual es coherente con una señal electrocardiográfica en condición basal.

Además, es importante considerar que la señal fue registrada en una persona sentada, relajada, sin actividad física previa y medida mediante un sistema BITalino. Por ello, se esperaba observar una señal relativamente estable, con un ritmo cardíaco sin grandes variaciones bruscas asociadas al esfuerzo físico. En este contexto, D1 presenta menor amplitud y menor energía, mientras que D2 y D3 muestran picos QRS más pronunciados y mayor potencia en el rango aproximado de 5 a 20 Hz. D3 parece ser el registro más regular visualmente, mientras que D2 muestra mayor variabilidad y algunos picos más intensos.

### Ciclo de inhalacion-contencion-exhalacion

Los resultados muestran que las señales EKG registradas durante hiperventilación conservan complejos QRS identificables después del filtrado, pero presentan mayor variabilidad que una señal basal. Esto es esperable porque, durante la hiperventilación, la respiración se vuelve más rápida y profunda, generando movimiento torácico, cambios en la línea base y posibles alteraciones en el contacto de los electrodos del BITalino.

Entre los tres registros, HV D2_1 presenta una señal relativamente clara con artefactos puntuales, HV D2_2 muestra la mayor variabilidad y una fuerte presencia de componentes de baja frecuencia, mientras que HV D2_3 tiene una señal más estable y con complejos QRS bien definidos. En conjunto, los resultados reflejan una condición respiratoria activa, diferente al reposo basal.

### Segunda señal basal

c

### Actividad física (Burpees)

Los resultados muestran que las señales EKG registradas después de realizar burpees presentan una respuesta compatible con actividad física intensa: mayor frecuencia de complejos QRS, mayor amplitud en algunos registros y mayor contenido frecuencial en comparación con una condición basal de reposo. Esto es esperable porque, luego del ejercicio, el sistema cardiovascular incrementa su actividad para responder a la mayor demanda de oxígeno del cuerpo.

En los tres registros se observa que el filtrado aplicado permitió mejorar la visualización de la señal y conservar los componentes principales del EKG. Burpees D1 muestra una señal clara y con frecuencias dominantes identificables alrededor de 2.5, 5, 10 y 16 Hz. Burpees D2 presenta mayor variabilidad y posibles artefactos, mientras que Burpees D3 muestra picos QRS bastante marcados y regulares. En conjunto, los resultados reflejan adecuadamente una señal cardíaca posterior al ejercicio, medida con BITalino, donde la persona ya no se encontraba en reposo sino bajo los efectos fisiológicos de una actividad física previa.

### Contención de respiración
e

---
## Homeguide
### Q1. What are the most typical types of noise sources affecting ECG?

* **Interferencia de la red eléctrica:**  
  Proviene de la corriente eléctrica del ambiente, normalmente es de 60 Hz en el Perú. Puede aparecer por cables, equipos eléctricos cercanos o una mala conexión a tierra.

* **Ruido por movimiento del paciente:**  
  Ocurre cuando el paciente se mueve durante el registro. Esto puede alterar el contacto entre los electrodos y la piel, generando cambios bruscos o distorsiones en la señal ECG.

* **Ruido por mal contacto de los electrodos:**  
  Se produce cuando los electrodos no están bien colocados, la piel no fue preparada adecuadamente o hay sudor, vello o grasa. Esto puede causar una señal inestable o con artefactos.

* **Interferencia muscular o electromiográfica:**  
  Aparece cuando los músculos del paciente se contraen, por ejemplo, si está tenso, temblando o hablando. Esta actividad eléctrica muscular puede mezclarse con la señal cardíaca.

* **Deriva de la línea base:**  
  Es una variación lenta de la señal ECG. Generalmente se debe a la respiración, movimientos del cuerpo o cambios en la impedancia entre la piel y el electrodo.

* **Ruido del equipo o ruido electrónico interno:**  
  Puede originarse en los componentes del sistema de adquisición, como amplificadores, cables, sensores o conversores analógico-digitales. Aunque suele ser menor, también puede afectar la calidad de la señal.

### Q2. Why does the change of the positioning of the sensors (lead I-III) change the ECG signal components? How do the components change?

Cambiar la posición de los sensores en las derivaciones **I, II y III** cambia los componentes de la señal ECG porque cada derivación observa la actividad eléctrica del corazón desde un ángulo diferente.

El corazón genera señales eléctricas durante la despolarización y repolarización. Sin embargo, cada derivación no registra toda la actividad eléctrica de la misma forma, sino que registra la proyección de esa actividad eléctrica en una dirección específica, según la ubicación del electrodo positivo y del electrodo negativo. Por eso, al cambiar de una derivación a otra, también cambia la forma en que se observan las ondas del ECG.

Generalmente, la derivación II suele mostrar una señal más clara y de mayor amplitud, porque su dirección se parece más al eje eléctrico normal del corazón, especialmente durante la despolarización ventricular.

| Componente | ¿Cómo puede cambiar? |
|---|---|
| Onda P | Puede verse más grande, más pequeña o menos clara. |
| Complejo QRS | Puede aumentar o disminuir su amplitud, o incluso verse más negativo. |
| Onda T | Puede cambiar su tamaño o su polaridad. |
| Línea base | Puede variar si cambia el contacto del electrodo o hay movimiento. |

La idea principal es que si la actividad eléctrica se dirige hacia el electrodo positivo, la onda se ve positiva. Si se aleja del electrodo positivo, la onda se ve negativa. Y si la actividad eléctrica va casi perpendicular a la derivación, la amplitud de la onda se reduce.

En conclusión, las  derivaciones **I, II y III** registran la misma actividad cardíaca, pero desde diferentes puntos de vista. Por eso, al cambiar la posición de los sensores, cambian principalmente la **amplitud**, la **polaridad** y la **forma** de las ondas **P**, **QRS** y **T**.


### Q3. Describe if there are major differences in the signal when acquiring the signal from different body locations (e.g., wrist / collarbone/ chest). What could be the cause? Did you expect such changes in the signal? Store a signal segment of each to visualize the differences
c
### Q4. The cardiac and the respiratory systems are well interconnected as is well known. Do you expect that different types of breathing (e.g. faster, deeper) to influence the ECG signals? Show screenshots of ECG signals in different respiratory circumstances and described the variations if there are any.
En los segmentos identificados como HV (hiperventilación), se observa que la respiración rápida y profunda altera significativamente los intervalos R-R. Este fenómeno se conoce como Arritmia Sinusal Respiratoria. Durante la fase de inhalación, la frecuencia cardíaca tiende a aumentar, lo que resulta en intervalos R-R más cortos. Por el contrario, durante la exhalación, la frecuencia disminuye y los intervalos se alargan. Adicionalmente, el movimiento mecánico del tórax durante la respiración profunda introduce un balanceo en la línea base (baseline wander) debido a las variaciones en la impedancia entre el electrodo y la piel.
### Q5. In Home-Guide #1 you have seen that different amounts of force produced in the muscle generated signals with different amplitudes. How does movement influence your ECG signal?
e
### Q6. To the best of your knowledge, how can you detect bradycardia and tachycardia in the ECG signal?
f

